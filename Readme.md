# Coding conventions at LIF

In order to ensure clean and uniform coding practices, all LIF projects follow
a modified version of the
[Google Java Style Guide](https://google.github.io/styleguide/javaguide.html).
The LIF style guide differs in a handful of elements:

- Curly braces should be alone on their line in block statements
- Member fields should start with `m_` and be written in CamelCase
- Static fields should start with `s_` and be written in CamelCase
- Local variables and method arguments should be written
  `with_a_syntax_like_this`

Otherwise, the Google rules are applied almost as is.

## The Checkstyle plugin in Eclipse

To help you make sure the code you produce follows the LIF guidelines, we
highly recommend that you use the [Checkstyle](http://checkstyle.sf.net/) tool,
and especially its Eclipse plugin. Checkstyle can verify all these coding
guidelines automatically, and give you warnings when your code violates one of
those rules. It is a quick way to make sure you write standards-compliant code
right from the start, which will mix well with the LIF's existing codebase.

### Installing Checkstyle

1. Go to Help / Eclipse Marketplace. Find and install the "Checkstyle Plugin".
2. Once CS is installed, go to Window / Preferences. In the Checkstyle tab,
   locate the "Global Check Configurations" box.
3. Select *New...*, choose "External Configuration File".
4. Click *Browse...*, and choose the file `LIF Checkstyle Coding Rules.xml`.
   Give some name to your style configuration.
5. Back in the "Global Check Configurations" box, click on your new
   configuration and set it as default.
6. Click "Apply and close". Eclipse will ask you to rebuild your workspace;
   click Yes.

### Using Checkstyle

Once Checkstyle is installed, it should give you warnings as you type. You can
also force the re-checking of the rules by right-clicking on a resource, and
selecting Checkstyle / Check code with Checkstyle.

## The Checkstyle plugin in IntelliJ

There are similar instructions for [using Checkstyle in IntelliJ](https://stackoverflow.com/a/26957047).

## The Eclipse formatter configuration

Eclipse can also help you format your code according to the rules. To install
the LIF formatting rules:

1. Go to Project / Properties and locate the Java Code Style / Formatter tab.
2. Click on "Configure Workspace settings".
3. In the *Formatter* window, click on *Import* and select the file
   `LIF Eclipse Coding Style.xml`.
4. Click on Apply to close all the windows.

From then on, the new code that you will produce will be formatted according to
some of the LIF style rules. In addition, you can auto-clean-up your code by
right-clicking on a resource and selecting Source / Format or Source / Clean up.

## The IntelliJ formatter configuration

To install the LIF formatting rules in IntelliJ IDEA:

1. Press Ctrl+Alt+S to open IDE settings and select Editor / Code style, then
   go to the Java section.
2. Click on the Gear icon next to the "Scheme" drop-down, select
   *Import scheme* / *Eclipse XML profile*.
3. Select the file `LIF Eclipse Coding Style.xml`. Give a name to these
   settings and click OK.
4. Click on Apply to close all the windows.

From then on, the new code that you will produce will be formatted according to
some of the LIF style rules. In addition, you can auto-clean-up your code by
right-clicking on a resource and selecting *Reformat code*.

## Other steps

Here are a few other steps you may want to follow to make sure your code
is consistent with all projects developed at LIF.

### Use Java 6 syntax

Make sure that your code complies with the
[Java 6 standard](https://en.wikipedia.org/wiki/Java_version_history#Java_SE_6).
This means you must avoid constructs that have been introduced in later
versions of Java, such as: the `java.nio` package, the "diamond" operator,
lambda expressions, etc.

If your project uses the default [AntRun](https://github.com/sylvainhalle/AntRun)
build script, it will automatically compile against Java 6 syntax. However, your
IDE is probably not configured by default to use this syntax. You can change
this in Eclipse by going into *Preferences*, *Java Compiler*, and select `1.6`
as the Java version for your whole workspace. From then on, Eclipse will warn
you whenever you write code that is not 1.6-compliant.

Happy programming!
