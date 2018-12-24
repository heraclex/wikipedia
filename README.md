# Wikipedia Assignment:

- Step1: Download the assignment: wikipedia.zip. For this assignment, you also need to download the data (133 MB):

http://alaska.epfl.ch/~dockermoocs/bigdata/wikipedia.dat

and place it in the folder: src/main/resources/wikipedia in your project directory.

In this assignment, you will get to know Spark by exploring full-text Wikipedia articles.

Gauging how popular a programming language is important for companies judging whether or not they should adopt an emerging programming language. For that reason, industry analyst firm RedMonk has bi-annually computed a ranking of programming language popularity using a variety of data sources, typically from websites like GitHub and StackOverflow. See their top-20 ranking for June 2016 as an example.



## spark command:
### windows
- spark command : `spark-submit --class wikipedia.WikipediaRanking --master local[4] .\target\scala-2.11\bigdata-wikipedia_2.11-0.1-SNAPSHOT.jar`


### macos
- spark command : `spark-submit --class wikipedia.WikipediaRanking --master local[6] \target/scala-2.11/bigdata-wikipedia_2.11-0.1-SNAPSHOT.jar`


## Common SBT commands:
- From the root directory of the project, you can compile the project: `$ sbt clean compile`
- Run the project: `$ sbt run`
- Package the project: `$ sbt clean package`
### Descriptions of the most common SBT commands:
|Command|Description|
|--------|--------|
|`clean`:| 	Removes all generated files from the target directory.|
|`compile`:|	Compiles source code files that are in src/main/scala, src/main/java, and the root directory of the project.|
|`~ compile`:|	Automatically recompiles source code files while you’re running SBT in interactive mode (i.e., while you’re at the SBT command prompt).|
|`console`:|	Compiles the source code files in the project, puts them on the classpath, and starts the Scala interpreter (REPL).|
|`consoleQuick`:|	Starts the Scala interpreter (REPL) with the project dependencies on the classpath.|
|`doc`:|	Generates API documentation from your Scala source code using scaladoc.|
|`help`:|  	Issued by itself, the help command lists the common commands that are currently available. When given a command, help provides a description of that command.|
|`inspect`:|	Displays information about . For instance, inspect library-dependencies displays information about the libraryDependencies setting. (Variables in build.sbt are written in camelCase, but at the SBT prompt, you type them using this hyphen format instead of camelCase.)|
|`package`:|	Creates a JAR file (or WAR file for web projects) containing the files in src/main/scala, src/main/java, and resources in src/main/resources.|
|`package-doc`:|	Creates a JAR file containing API documentation generated from your Scala source code.|
|`publish`:|	Publishes your project to a remote repository. See Recipe 18.15, “Publishing Your Library”.|
|`publish-local`:|	Publishes your project to a local Ivy repository. See Recipe 18.15, “Publishing Your Library”. reload Reloads the build definition files (build.sbt, project/.scala, and project/.sbt), which is necessary if you change them while you’re in an interactive SBT session.|
|`run`:|	Compiles your code, and runs the main class from your project, in the same JVM as SBT. If your project has multiple main methods (or objects that extend App), you’ll be prompted to select one to run.|
|`test`:|	Compiles and runs all tests.|
|`test:console`:|	Compiles the source code files in the project, puts them on the classpath, and starts the Scala interpreter (REPL) in “test” mode (so you can use ScalaTest, Specs2, ScalaCheck, etc.).|
|`update`:|	Updates external dependencies.|