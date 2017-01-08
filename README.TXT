========================
BUILD OUTPUT DESCRIPTION
========================

When you build an Java application project that has a main class, the IDE
automatically copies all of the JAR
files on the projects classpath to your projects dist/lib folder. The IDE
also adds each of the JAR files to the Class-Path element in the application
JAR files manifest file (MANIFEST.MF).

To run the project from the command line, go to the dist folder and
type the following:

java -jar "SuperSimpleStock.jar" 

To distribute this project, zip up the dist folder (including the lib folder)
and distribute the ZIP file.

Trade is a class that contains a POJO representing a Trade.

Stock is a class managing Operations, calculations on Stocks {e.g. Dividend (on COMMON/PREFFERED), PERatio } 
and GBCE All Share Index.

SuperSimpleStock is a class that contains the main() and uses Trade and Stock classes.
It calculates Stock Price based on Summation Formula given on the Exercise sheet,
using Trades recorded past 15' minutes.
{ Stock_Price = SUM ( Trade_Price(i) * Quantuty(i) ) / SUM (Quantity(i) ) }
It also calls calculation GBCE All Share Index from Stock using 
Geometric Mean of Prices for all Stock {Math.Pow(p1*p2*p3*...*pn, 1/(n))}


Notes:

* If two JAR files on the project classpath have the same name, only the first
JAR file is copied to the lib folder.
* Only JAR files are copied to the lib folder.
If the classpath contains other types of files or folders, these files (folders)
are not copied.
* If a library on the projects classpath also has a Class-Path element
specified in the manifest,the content of the Class-Path element has to be on
the projects runtime path.
* To set a main class in a standard Java project, right-click the project node
in the Projects window and choose Properties. Then click Run and enter the
class name in the Main Class field. Alternatively, you can manually type the
class name in the manifest Main-Class element.
