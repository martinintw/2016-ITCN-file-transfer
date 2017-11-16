# File-transfer
## Today's mission

You will need to write simple file transfer client and server in language `C`.  
Please modify the sample code to achieve this goal.  
Fill in your own code by following the **TODO Hint** in the code.  

```c
/**
  TODO:
  print something here.
**/
```

## Install
### With simple browser

You can click `Download ZIP` to download a zip file directly

![](https://raw.githubusercontent.com/HSNL-TAs/2016-ITCN-file-transfer/master/download_zip.png)

### With Git
1. Install `Git` on your system
	```shell
	$ sudo apt-get install git
	```
2. Open command prompt
3. Input `git clone https://github.com/HSNL-TAs/2016-ITCN-file-transfer.git`

## Compile and Run
### Compile with makefile
What in makefile
```makefile
all: server.c client.c
	gcc server.c -o server
	gcc client.c -o client

clean:
	rm -rf server
	rm -rf client
```

### compile  
```sh
$ make
```

### run
```sh
$ ./server 8888
```
Open another termial.
```sh
$ ./client 127.0.0.1 8888
```

## Requirement
### Server
- User can assign **port** to server
- Returns files list to client when the client connects immediately to the server. (We have provided this function which scans all the file under the same directory.)  

	```sh
	# Client side
	$ ./client 127.0.0.1 8888
	[✓] Connect to server.
	[✓] Server reply!
	-----------
	Files on server:
	lab3_2_spec.pdf
	test.png
	test.txt
	-----------
	Enter the filename:
	```

- Returns files which client wants to download.

	```sh
	# Client side
	Enter the filename: test.txt
	[-] Downloading `test.txt` ...
	[✓] Download successfully!
	-----------
	Enter the filename: # user can continue to send download request.
	```

### Client
- User can assign **ip address** and **port** to connect the server with command line argument.
- Support user inputs the file name to download file from server, per file per input.
- Input `.exit` to disconnect from server.

**NOTE:** Server and client should keep connected unless user inputs `.exit`

## Example
![](https://raw.githubusercontent.com/HSNL-TAs/2016-ITCN-file-transfer/master/example_screenshot.png)

## Deadline
Please also uplaod **your code** and **a screenshot of your result** to ilms system.
( Package them as `.zip` format and name after your **student ID**)

- Deadline: 100%, before 2017/12/08 23:59 (Fri.)
- Deadline: 80%, before 2017/12/15 23:59 (Fri.)
- Deadline: 60%, before 2017/12/22 23:59 (Fri.)

After 2016/12/22, your submission is not accepted.

## Question
Please feel free to ask questions at
- [Here](https://github.com/HSNL-TAs/2016-ITCN-file-transfer/issues), or
- On the iLms forum, or
- Come at Office Hour (15:30 ~ 17:20 on Wednesday, 綜二 705)
