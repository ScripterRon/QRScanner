QRScanner
=========

QRScanner will scan a QR code using an attached webcam and display the text.  The scanned text can then be copied to the system clipboard for use with another application.

Webcam-Capture and Zxing are used to scan the QR codes.

Simple Logging Facade (SLF4J) is used for console and file logging.  I'm using the JDK logger implementation which is controlled by the logging.properties file located in the application data directory.  If no logging.properties file is found, the system logging.properties file will be used (which defaults to logging to the console only).


Build
=====

I use the Netbeans IDE but any build environment with Maven and the Java compiler available should work.  The documentation is generated from the source code using javadoc.

Here are the steps for a manual build.  You will need to install Maven 3 and Java SE Development Kit 8 if you don't already have them.

  - Create the executable: mvn clean package
  - [Optional] Create the documentation: mvn javadoc:javadoc
  - [Optional] Copy target/QRScanner-v.r.jar and target/lib/* to wherever you want to store the executables.
  - Create a shortcut to start QRScanner using java.exe for a command window or javaw.exe for GUI only. 

Sample Windows shortcut:	

	javaw.exe -Xmx256m -jar \Bitcoin\QRScanner\QRScanner-1.0.0.jar PROD
