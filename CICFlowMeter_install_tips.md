# CICFlowMeter Install Guide. <br> !! Attention Not Official !!

### This is for ***Windows.***


## CICFlowMeter github
https://github.com/ahlashkari/CICFlowMeter


## First of all
### Make sure your Java environment param. and JAVA_HOME is exist.
[Download JDK Link (Personal suggest jdk version 1.8.X)](https://www.oracle.com/tw/java/technologies/javase/javase8-archive-downloads.html)


## Step Preview
* Maven 
* WinPcap
* CICFlowMeter


## Maven
* Download
* Please make sure where your folder! 
[Maven official download page link](https://maven.apache.org/download.cgi)
* Setup your in environment param.
* Open cmd or Powershell. Make sure maven be installed and setup successed. 
```
mvn -version
```
 If you see ***Apache Maven X.X.X***. &ensp; That's right.

## WinPcap
* Download 
[WinPcap official download page link](https://www.winpcap.org/install/)

---

## Download CICFlowMeter
* Any way you can use
* Please make sure where your folder! 
https://github.com/ahlashkari/CICFlowMeter

### 1. Edit setup file XXX\CICflowMeter-master\build.gradle at line 20
_from_
```
compile group: 'org.jnetpcap', name: 'jnetpcap', version:'1.4.1'
```
_to_

```
compile group: 'org.jnetpcap', name: 'jnetpcap', version:'1.4.r1425'
```
### 2. Open Cmd or Powershell and go to XXX\CICflowMeter-master
* Copy All of this.

```
mvn install:install-file -Dfile=jnetpcap.jar -DgroupId=org.jnetpcap -DartifactId=jnetpcap -Dversion=1.4.1 -Dpackaging=jar
```
#### ___Tips: Some Error will be print. That's normal.___

### 3. Create folder and copy file to there.
* Create folder *jnetpcap* in 
```
C:\Users\Xyour_user_nameX\.m2\repository\org
```
* Create folder *jnetpcap* in 
```
C:\Users\Xyour_user_nameX\.m2\repository\org\jnetpcap
```
* Create folder *1.4.r1425* in 
```
C:\Users\Xyour_user_nameX\.m2\repository\org\jnetpcap\jnetpcap
```
* Copy file 
```
XXX\CICflowMeter-master\jnetpcap\win\jnetpcap-1.4.r1425\jnetpcap.jar 
```
to 
```
C:\Users\Xyour_user_nameX\.m2\repository\org\jnetpcap\jnetpcap\1.4.r1425
```
* Go to 
```
C:\Users\Xyour_user_nameX\.m2\repository\org\jnetpcap\jnetpcap\1.4.r1425 
```
Change .jar file name from _jnetpcap.jar_ to _jnetpcap-1.4.r1425.jar_


### 4. Open Cmd or Powershell and go to XXX\CICflowMeter-master
```
 ...\XXX\CICflowMeter-master>
```
### 5. Start !
```
 ...\XXX\CICFlowMeter-master> gradlew execute
```



### References
https://www.cnblogs.com/KoiC/p/17458131.html
