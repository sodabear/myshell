# myshell
toy shell design to confirm POSIX (IEEE Std 1003.1-2017) Shell and Utilities

Detail description could be found from [OpenGroup: Shell & Utilities](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/contents.html)

## Platform
POSIX

## Software stack
GNU software stack will be use because it itself has already provided many handy libraries and C extensions.

## Road map
1. sh utility with single command_string except interactive

1. frequently used utilities like cd, pwd, chmod, etc. 

1. pipe, redirection, background, etc. which require more than one process exec

1. interactive
