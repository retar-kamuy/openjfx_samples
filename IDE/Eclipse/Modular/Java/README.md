## Modular samples for Eclipse

JavaFX 13 samples to run from Eclipse with different options and build tools

Version Eclipse: 2019-03 (4.11.0)

Download [JDK 11 or later](http://jdk.java.net/) for your operating system.
Make sure `JAVA_HOME` is properly set to the JDK installation directory.

**N.B**: If you use JDK 12, install this patch from MarketPlace: `Java 12 support for Eclipse 2019-03 (4.11)`.

### Java

- Download [JavaFX jmods](https://gluonhq.com/products/javafx/) for your operating 
system and unzip to a desired location.

Clone the sample and open the project with Eclipse. 

Run with `Run configurations -> Java Application -> modHelloFX`

To create and run a custom JRE, from terminal:

On Linux or Mac run:

    cd IDE/Eclipse/Modular/Java/HelloFX
    export PATH_TO_FX_MODS=path/to/javafx-jmods-13
    $JAVA_HOME/bin/jlink --module-path $PATH_TO_FX_MODS:bin/hellofx --add-modules=hellofx --output jre
    jre/bin/java -m hellofx/org.openjfx.MainApp

On Windows run:

    cd IDE\Eclipse\Modular\Java\HelloFX
    set PATH_TO_FX_MODS="path\to\javafx-jmods-13"
    jlink --module-path "%PATH_TO_FX_MODS%;bin\hellofx" --add-modules=hellofx --output jre
    jre\bin\java -m hellofx/org.openjfx.MainApp
