# Maven JAR Library Skeleton Template
Clean Maven JAR library template skeleton project. Creates **JAR** file, which may be included in the project as a dependency. The JAR itself does not includes any dependency by default POM configuration.

Grab and use this template to quickly create the empty maven JAR lib project.

**Commands**:

Build JAR: `mvn clean package`

**Hot to use your new library**:

Newly created library may be placed into maven repository, if needed, or used directly from GitHub like this:


1) Add **jitpack.io** repository to your POM file:
```xml
    <repositories>
        <repository>
            <id>jitpack.io</id>
            <url>https://jitpack.io</url>
        </repository>
    </repositories>
```

2) Add dependency to POM:

```xml
        <dependency>
            <groupId>com.github.divlv</groupId> <!-- Your GitHub login (divlv) -->
            <artifactId>mavenjarlibskeleton</artifactId> <!-- Your GitHub repo name (of library) -->
            <version>1.0</version> <!-- GitHub lib release version -->
        </dependency>
```

3) Access the **CurrentTimeClass** in your code like this:
```java
final CurrentTimeClass currentTimeClass = new CurrentTimeClass();
System.out.println(currentTimeClass.getCurrentTime());

// Should be something like: "Wed Nov 23 09:59:44 EET 2016"
```