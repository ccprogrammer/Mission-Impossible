# Mission-Impossible

### #gradle problem
1. +org.gradle.java.home=C:/Program Files/Java/jdk-16.0.2

### #google_maps_flutter 
I fixed it by downgrading jdk 17 to jdk 16 and correcting jdk path in my project `gradle.properties` and environment.

<details>
<summary>Steps</summary>

```
  Web that i found to fixed it https://www.happycoders.eu/java/how-to-switch-multiple-java-versions-windows/
  
  1. The top list ("User variables") should not contain any Java-related entries.
  
  2. The lower list ("System variables") should contain an entry "JAVA_HOME = C:\Program Files\Java\jdk-17". If this entry does not exist, you can add it with "New…". If it 
  
  exists but points to another directory, you can change it with Edit….
  
  3. Delete the following entries under "Path":
  
    C:\ProgramData\Oracle\Java\javapath
  
    C:\Program Files (x86)\Common Files\Oracle\Java\javapath
  
  4. Insert the following entry instead:
  
     %JAVA_HOME%\bin
```

</details>

<details>
<summary>Steps</summary>

```
  FAILURE: Build failed with an exception.

* Where:
Build file 'C:\flutter\.pub-cache\hosted\pub.dartlang.org\google_maps_flutter-2.1.2\android\build.gradle'

* What went wrong:
Could not compile build file 'C:\flutter\.pub-cache\hosted\pub.dartlang.org\google_maps_flutter-2.1.2\android\build.gradle'.
> startup failed:
  General error during conversion: Unsupported class file major version 61

  java.lang.IllegalArgumentException: Unsupported class file major version 61
```

</details>
