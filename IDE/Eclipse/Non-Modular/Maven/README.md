## Non-modular samples for Eclipse

JavaFX 13 samples to run from Eclipse with different options and build tools

Version Eclipse: 2019-03 (4.11.0)

Download [JDK 11 or later](http://jdk.java.net/) for your operating system.
Make sure `JAVA_HOME` is properly set to the JDK installation directory.

**N.B**: If you use JDK 12, install this patch from MarketPlace: `Java 12 support for Eclipse 2019-03 (4.11)`.

### Maven

For the first time only:

- Make sure you have the Maven Integration for Eclipse m2e plugin installed.

- Add the JavaFX Maven archetypes `org.openjfx:javafx-archetype-simple:0.0.1` and `org.openjfx:javafx-archetype-fxml:0.0.1`

Clone the sample, open it with Eclipse and import the Maven changes. 

Run with `Run configurations -> Maven Build -> hellofx`.

Note: on Windows, under Eclipse running Oracle JDK 1.8, you need to add `-Djava.library.path=C:\` 
to the JavaFX maven plugin:

    <configuration>
        <executable>/path/to/JDK/bin/java</executable>
        <options>
            <option>-Djava.library.path=C:\tmp</option>
        </options>
        <mainClass>org.openjfx.hellofx.App</mainClass>
    </configuration>