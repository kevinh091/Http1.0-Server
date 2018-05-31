Build and Run:
	Compile myhttpd from source. Simply call make on the directory the source files are in.
	
		$ make
		
	Now you can run the program with different options. Example:
	
		$ ./myhttpd -p 8080
	
	−d         : Enter debugging mode. That is, do not daemonize, only accept one connection at a time and enable logging to stdout. Without this option, the web server should run as a daemon process in the background. 
 
	−h         : Print a usage summary with all options and exit. 
 
	−l file        : Log all requests to the given file. See LOGGING for details. 
 
	−p port : Listen on the given port. If not provided, myhttpd will listen on port 8080. 
 
	−r dir  : Set the root directory for the http server to dir. 
 
	−t time  : Set the queuing time to time seconds. The default should be 60 seconds. 
 
	−n threadnum: Set number of threads waiting ready in the execution thread pool to threadnum. The default should be 4 execution threads. 
 
	−s sched : Set the scheduling policy. It can be either FCFS or SJF. The default will be FCFS. 
	
	
Things you cannot do:
	- Send another request before the previous request has come back to you.
	- Make a request to a file other than the type of .txt .html or image/gif.
	- Protocol type other than HTTP/1.0
	- Send special characters, ^D, ^C, ^Z.. ETC
	
Directory and not found files are treated as 0 byte.