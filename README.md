# java-version-switcher
Scripts that simplify the life of a java developer. Switching between java versions using one command

original source is [here](https://www.happycoders.eu/java/how-to-switch-multiple-java-versions-windows/)

![](../pic1.png)

If you have many versions of jdk between which you need to switch these scripts will help you

## Step 1: Set two environment variables:

    JAVA_HOME – many start scripts use this variable.
    Path – is used when running a Java binary (such as java and javac) from the console.

## Step 2: Install scripts

- `java<version>`: Activates the Java version in the current command line.
- `java<version>-user`: Sets the Java version as the default version for your user account.
- `java<version>-system`: Sets the Java version as the default version for the entire system-

Scrip for `java<version>` as follows:

    @echo off
    set JAVA_HOME=C:\Program Files\Java\jdk-18
    set Path=%JAVA_HOME%\bin;%Path%
    echo Java 18 activated.

Scrip for `java<version>-user` as follows:

    @echo off
    set JAVA_HOME=C:\Program Files\Java\jdk-18
    setx JAVA_HOME "%JAVA_HOME%"
    set Path=%JAVA_HOME%\bin;%Path%
    echo Java 18 activated as user default.

Scrip for `java<version>-system` as follows:

    @echo off
    set JAVA_HOME=C:\Program Files\Java\jdk-18
    setx JAVA_HOME "%JAVA_HOME%" /M
    set Path=%JAVA_HOME%\bin;%Path%
    echo Java 18 activated as system-wide default.

Put scripts somewhere. For instance `C:\Program Files\Java\scripts`
and save them in `.bat` extension


## Step 3: Add the Script Directory to the Path

