Thinking in Java, 4th Edition: Downloading, Installing and Testing the Code
---------------------------------------------------------------------------

Note that this book covers Java 5/6. The recent book [On Java 8](http://www.onjava8.com/)
covers Java 8.

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>.

1.  Download the code by pressing the green button you see towards the top if this page. After pressing the button,
    select "Download Zip."

2.  Create a directory in which to install the code. For these
    instructions, we'll refer to this directory as `C:\TIJ4\code`.

3.  Using Winzip or some other zip utility, extract the zip file into
    the `C:\TIJ4\code` directory. When you're done, you should see
    several levels of directories, and in the `C:\TIJ4\code`
    directory, you'll see, among other things, subdirectories
    corresponding to the chapters in the book.

4.  Install the Java JDK SE5 or later from the [download site at
    Sun](http://java.sun.com/javase/downloads/index.jsp). You'll also
    eventually want the documentation, which is available further down
    on that page. You may also choose to install Java SE6; the code
    will work with that as well. Note that the most reliable approach
    is to install to the default directories.

5.  Add the `bin` directory of your JDK to your path.

6.  Set the CLASSPATH in your computer's environment. For Windows
    machines, right-click on the "My Computer" icon and select
    "Properties." Then select the "Advanced" tab and click the
    "Environment Variables" button at the bottom. Under "System
    Variables," look to see if there's already a "CLASSPATH" variable.
    If there is, double click and add
    ```
    ;.;..;C:\TIJ4\code;
    ```
    to the end of the current entry. If there is no "CLASSPATH"
    variable, click the "New" button and enter
    ```
    CLASSPATH
    ```
    In the "Variable name" box, and
    ```
    .;..;C:\TIJ4\code;
    ```
    In the "Variable value" box, then click "OK". To verify that your
    classpath has been set, start a command prompt (see below), then
    enter `set` and look for the `CLASSPATH` information in the
    output.

7.  Install the `Ant` build tool by following the instructions you
    will find in the [Ant download](http://ant.apache.org/). Note:
    `Ant` is not required in order to compile the examples in the
    book. It is used to automate the process, but you can also compile
    each example individually (once you have the CLASSPATH set, as
    described above) using the `javac` command-line compiler that
    was installed when you completed the previous step (note that you
    may have to set the Windows PATH to point to `javac.exe`). To
    compile a file called `MyProgram.java`, you type `javac
    MyProgram.java`.

8.  Start a command prompt in the `C:\TIJ4\code` directory. To do
    this in Windows, press the "Start" button, then select "Run" and
    type "cmd" and press "OK." then type
    ```
    cd C:\TIJ4\code
    ```
    into the resulting command window.

9.  At this point you should be able to start a command prompt in
    `C:\TIJ4\code` and type `ant build`, and the build should
    successfully compile all the chapters up to the `io` chapter,
    where it will fail with an error message about a missing library.
    If you only need to work with chapters before `io` for now, this
    will suffice for awhile.

10. You can also move into individual chapters and type `ant` (to
    compile and execute the code in that chapter) or `ant build` (to
    compile the code only).

11. To build the entire code base, you'll need to install the
    additional libraries. These include:
    -   [XOM](http://www.xom.nu)
    -   [Javassist](http://sourceforge.net/project/showfiles.php?group_id=22866)
    -   The `javaws.jar` library, which comes with the standard Java
        installation, but which you must explicitly place in your
        classpath (described below).
    -   [The Eclipse SWT
        library](http://download.eclipse.org/eclipse/downloads/).
        Click on the most recent build number, then scroll down to
        "SWT Binary and Source" and select the file corresponding to
        your platform. Further details about finding the jar file are
        in the book under the heading "Installing SWT."

    In general, you can install the above Jar files by placing them in
    the `jre/lib/ext` directory that is part of the "Java Runtime"
    that will be set up when you install the Java SE5 or Java SE6
    development kit. You may have to hunt around for the JRE, but it
    can often be found under your "Program Files" directory, under
    "Java."

12. Alternatively, you can explicitly install each of the Jar files.
    To do this, you must add each one to your CLASSPATH, following the
    directions shown earlier on this page. However, *you must also
    include the name of the Jar file in the CLASSPATH entry*. For
    example, if you put the `xom.jar` file in a directory called
    `C:\TIJ4\libraries\`, then the associated CLASSPATH entry
    would be `C:\TIJ4\libraries\xom.jar;`.

13. This code is designed to work outside of IDEs. Because packages
    are not introduced until later chapters, and some of the fancier
    IDEs like Eclipse require all code to be in packages, if you want
    to use the code inside those IDEs you will have to make some
    adjustments (however, see the `Eclipse.py` program in the
    download package for some help). Different IDEs have different
    requirements and it may be more trouble than it's worth while
    you're getting started; instead, you may want to begin with a more
    basic editor like [JEdit](http://www.jedit.org/).

