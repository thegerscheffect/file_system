# Operating Systems (COP 4610) Final Project - File System Implementation

The objective of this project was to understand how a file system works, specifically the directory hierarchy and storage management. Also, to understand some of the performance issues file systems must deal with.

In this project, we built a user-level library, libFS, that implements a file system. Our file system will be built inside of a library that applications can link with to access files and directories. The library links with a layer that implements a "disk"; the library is provided, LibDisk. The only modified file in this project is LibFS.c.

## Running the tests

The successfully implemented commands for this project do the following: 
* Create a file 
* Remove a file
* Create a directory 
* Remove a directory
* List all the items in the disk, or given path

### To compile the code, type the following commands into your terminal
```
make
```
This should compile the all the files and create the necessary executables for all the required tests.

### Before running tests
Set up a shared library link path:
```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:.
```
and remove any previous testing output:
```
make reset
```
NOTE: It's important to note that the tests cannot be run on an old disk. Creation of duplicated files/directory will not occur, it will result in an error.

### To run the tests, type the following commands into your terminal

Perform simple test:
```
./simple-test.exe test 
```
List the file system:
```
./slow-ls.exe test / 
```
Touch a file to the file system:
```
./slow-touch.exe test /testfile 
```
Check if the new created file is showing:
```
./slow-ls.exe test / 
```
Remove file:
```
./slow-rm.exe test /testfile
```
Check the remove result:
```
./slow-ls.exe test /
```
Create directory:
```
./slow-mkdir.exe test /dirnew 
```
```
./slow-ls.exe test / 
```
Remove directory:
```
./slow-rmdir.exe test /dirnew 
```
```
./slow-ls.exe test / 
```

## Contributors:
* Sheila Alemany 
* Andy Pujol
