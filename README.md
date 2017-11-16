# JCenter
A tool for upload to jcenter.

## Usage: *NEW!*
in your library module build.gradle..
```java
ext {
    repoOrg = ''// organization name
    repoGroup = 'maven'// repository name
    repoPkg = 'OpenLib'// repository package name
    devName = 'shenhuanet'// developer name
    devMail = 'shenhuanet@126.com'// developer email
    libGroup = 'com.shenhua.libs'// lib group
    libArtifact = 'open'// lib artifact
    libDesc = ''// lib Description
    web = 'https://github.com/shenhuanet/'// git url
}
apply from: 'https://raw.githubusercontent.com/shenhuanet/JCenter/master/bintray_release.gradle'
```
local.properties
``` java
bintray.apikey=********************
bintray.user=****
bintray.gpg.password=shenhua
```
Terminal
```java
gradlew install
    
gradlew bintrayUpload
```

## Usage: *Deprecated*

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
    libraryName = '' // libraryName must same as module library..
    libraryVersion = '1.0.0'
    libraryDescription = ''
    siteUrl = 'https://github.com/shenhuanet/'
    gitUrl = 'https://github.com/shenhuanet/.git'

    bintrayRepo = 'maven'
    bintrayGroupName = 'shenhuanetos'
    publishedGroupId = 'com.shenhua.libs'
    developerId = 'shenhua'
    developerName = 'shenhua'
    developerEmail = 'shenhuanet@126.com'
}
apply from: 'https://raw.githubusercontent.com/shenhuanet/JCenter/master/install.gradle'
apply from: 'https://raw.githubusercontent.com/shenhuanet/JCenter/master/bintray.gradle'
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
    

