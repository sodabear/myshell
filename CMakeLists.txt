cmake_minimum_required(VERSION 3.10)
project(myshell C)

set(MYSHELL_SOURCE_DIR "${CMAKE_CURRENT_SOURCE_DIR}")

file(GLOB_RECURSE MYSHELL_HEADERS "${MYSHELL_SOURCE_DIR}/include/*.h")
file(GLOB_RECURSE MYSHELL_SOURCES "${MYSHELL_SOURCE_DIR}/source/*c")

add_executable(myshell ${MYSHELL_HEADERS} ${MYSHELL_SOURCES})
target_compile_features(myshell PUBLIC c_std_99 c_restrict c_static_assert
                                       c_variadic_macros)
target_include_directories(myshell PUBLIC ${MYSHELL_SOURCE_DIR}/include)

install(
  TARGETS myshell
  CONFIGURATIONS Debug
  RUNTIME DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/Debug/bin")
install(
  TARGETS myshell
  CONFIGURATIONS Release
  RUNTIME DESTINATION bin")
