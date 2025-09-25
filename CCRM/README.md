Campus Course & Records Manager (CCRM)
📖 Project Overview
The Campus Course & Records Manager (CCRM) is a robust Java SE console-based application engineered to facilitate the comprehensive management of academic and administrative records for educational institutions. It provides a centralized platform for handling:

Student Management: Creation, modification, enrollment, unenrollment, and transcript generation for student records.

Course Administration: Creation, modification, search functionality, and assignment of instructors to courses.

Enrollment & Grade Processing: Recording of grades, computation of Grade Point Averages (GPA), and automated transcript generation.

File System Utilities: Functionality for importing/exporting data via CSV, executing recursive backups, and generating various analytical reports.

The application serves as a comprehensive showcase of advanced Java programming paradigms, including Object-Oriented Programming (OOP), modern NIO.2 File I/O, the Stream API, the Date/Time API, sophisticated Exception Handling, and strategic implementation of Design Patterns such as Singleton and Builder.

How to Run
To build and execute the CCRM application, follow these terminal commands from the project's root directory:

1. Compilation

Compile all source files from their respective packages into the bin directory. This command ensures all dependencies are resolved.

javac -d bin src/edu/ccrm/cli/MainMenu.java src/edu/ccrm/cli/CLIApp.java src/edu/ccrm/domain/*.java src/edu/ccrm/service/*.java src/edu/ccrm/io/*.java src/edu/ccrm/util/*.java src/edu/ccrm/config/*.java

2. Execution

Launch the main application from the command line.

java -cp bin edu.ccrm.cli.CLIApp

Historical Context: The Evolution of Java
A concise overview of key milestones in the development of the Java platform:

1995: Initial public release of Java 1.0 by Sun Microsystems.

2004: Launch of Java 5.0, a significant update that introduced foundational language features like Generics and Enums.

2011: Oracle Corporation acquires Sun Microsystems, assuming stewardship of the Java platform.

2014: The release of Java 8, which revolutionized development with the introduction of Lambda Expressions and the Stream API.

2017: Java 9 introduces the Java Platform Module System (JPMS), also known as Project Jigsaw, to enhance modularity.

2023: Java 21 is released, continuing the rapid innovation cycle as a designated Long-Term Support (LTS) version.

Java Editions: A Comparative Overview
The Java ecosystem is organized into distinct editions, each tailored to a specific application domain.

Edition

Primary Application

Target Environment

Java ME

Mobile and embedded devices.

Resource-constrained hardware with limited processing and memory.

Java SE

Desktop and command-line applications.

The foundational platform for all Java development, providing core libraries.

Java EE

Enterprise-grade applications.

Distributed systems, web servers, and large-scale, multi-tiered architectures. (Now known as Jakarta EE).

The Java Ecosystem: Core Components
A clear distinction between the essential components of the Java runtime environment:

JDK (Java Development Kit): A comprehensive suite of tools for professional Java development, encompassing the JRE, the Java compiler (javac), a debugger, and extensive class libraries.

JRE (Java Runtime Environment): A foundational environment that contains all the necessary elements to execute compiled Java applications, including the JVM and core libraries.

JVM (Java Virtual Machine): The conceptual machine that interprets and executes Java bytecode, acting as the critical layer that enables platform independence ("Write Once, Run Anywhere").

Execution Flow:
The development process culminates in the transformation of source code into executable bytecode, which is then managed by the runtime environment.

Source Code (.java) -> Compiled by javac -> Bytecode (.class) -> Executed by the JVM within the JRE.

Development Environment Configuration
Installation of the Java Development Kit (JDK)

To establish a functional development environment on a Windows platform, follow these steps:

Acquire the JDK: Obtain the official installer for JDK 17 (or a later version) from either the Oracle or OpenJDK website.

Execute the Installer: Launch the executable file and proceed with the default installation settings. It is recommended to note the installation path for future reference (e.g., C:\Program Files\Java\jdk-17).

Configure Environment Variables:

Navigate to the System Properties and access the "Environment Variables" dialog.

Under "System variables," create a new variable named JAVA_HOME and set its value to your JDK installation directory.

Append %JAVA_HOME%\bin to the system's Path variable to ensure the Java executables are accessible from the command line.

Validate the Installation: Open a new command-line interface (e.g., Command Prompt or PowerShell) and execute the following commands to confirm a successful installation.

java -version
javac -version

Configuring the Eclipse IDE

IDE Acquisition: Download the Eclipse IDE for Java Developers from the official Eclipse website.

Project Creation: Launch the IDE and create a new Java Project via the menu: File -> New -> Java Project. Name the project CCRM.

Source Code Integration: Import the project's source code by copying the src/ directory into your newly created project folder.

Initial Execution: To launch the application, locate CLIApp.java within the src folder, right-click, and select Run As -> Java Application.

Architectural Blueprint: Syllabus to Code Mapping
This table provides a high-level mapping of core syllabus topics to their specific implementation within the project's source code, serving as a guide to the application's internal structure.

Syllabus Topic

Demonstrating File/Class

Implementation Detail

Encapsulation

Student.java

Achieved through the use of private fields with public getter and setter methods.

Inheritance

Person.java -> Student.java, Instructor.java

The Student and Instructor classes extend the abstract base class Person.

Abstraction

Person.java

The Person class utilizes abstract methods that are implemented by its subclasses.

Polymorphism

TranscriptService.java

Demonstrated by invoking the toString() method on different object types.

Singleton Pattern

AppConfig.java

A single instance of the AppConfig class is maintained throughout the application lifecycle.

Builder Pattern

Course.Builder

The Course object is constructed using a dedicated nested Builder class for clarity and immutability.

Exceptions

DuplicateEnrollmentException.java

A custom exception is defined to handle specific business logic errors.

File I/O (NIO.2)

ImportExportService.java

Utilizes the modern Java NIO.2 framework for file system operations.

Recursion

RecursionUtils.java

Implements recursive algorithms for tasks such as file system traversal.

Enums

Grade.java, Semester.java

Provides type-safe enumerated constants for grades and semesters.

Notes on Assertions
Assertions are a valuable debugging tool in Java. They are used to test a developer's assumptions about the program's state. By default, assertions are disabled at runtime for performance.

Enabling Assertions

To enable assertions, you need to use the -ea (enable assertions) flag with the java command.

Command

Description

java -ea com.project.Main

Enables assertions for all non-system classes.

java -ea:com.project.utils... com.project.Main

Enables assertions for the com.project.utils package and all its subpackages.

java -ea:com.project.Main com.project.Main

Enables assertions only for the com.project.Main class.

For any questions, feel free to contact me.
Contact Number: 9528550896# Run
java -cp bin edu.ccrm.cli.CLIApp
