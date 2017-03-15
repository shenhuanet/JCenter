# JCenter
A tool for upload to jcenter.

## Usage:

 1. Project build.gradle
 
```java
dependencies {
        classpath 'com.android.tools.build:gradle:2.2.2'
        classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.7'
        classpath 'com.github.dcendents:android-maven-gradle-plugin:1.5'
        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
```
 2. library build.gradle
```java
ext {
    bintrayRepo = 'maven'
    bintrayName = ''//bintrayName
    bintrayGroupName = 'shenhuanetos'
    publishedGroupId = 'com.shenhua.libs'
    libraryName = ''// libraryName Corresponding compile 'shenhua.lib:xxxxx:1.0' In xxxxx
    artifact = ''// artifact = libraryName
    libraryDescription = ''// libraryDescription
    versionDescription = ''// versionDescription
    siteUrl = 'https://github.com/shenhuanet/xxxx'
    gitUrl = 'https://github.com/shenhuanet/xxxx.git'
    issueUrl =''// issueUrl
    libraryVersion = '1.0'
    developerId = 'shenhua'
    developerName = 'shenhua'
    developerEmail = 'shenhuanet@126.com'
    licenseName = 'The Apache Software License, Version 2.0'
    licenseUrl = 'http://www.apache.org/licenses/LICENSE-2.0.txt'
    allLicenses = ["Apache-2.0"]
}
```

 3. local.properties
``` java
bintray.apikey=********************
bintray.user=****
```
 
 4. Terminal
 
```java
gradlew install
    
gradlew bintrayUpload
```
(if *javadoc FAILED* ,Please make sure that the comment is in English and then replace it in Chinese)  OR **gradlew javadocJar** OR **gradlew sourcesJar**

 5. if added to maven, add to jcenter and the library will Checked in at
    12:30 midnight.
    

