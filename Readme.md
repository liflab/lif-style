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

Happy programming!