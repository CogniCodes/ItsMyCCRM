Project: Campus Course & Records Manager (CCRM)

Requirements
------------
- Java 17 JDK or later
- Recommended IDE: IntelliJ IDEA / Eclipse (optional)
- Build: javac / java (Maven setup optional)

How to compile & run (Linux / macOS with bash)
1. From repository root:
   javac -d out $(find src -name "*.java")
   java -cp out edu.ccrm.cli.CCRMApplication

2. On Windows (PowerShell):
   mkdir out
   javac -d out (Get-ChildItem -Recurse -Filter *.java).FullName
   java -cp out edu.ccrm.cli.CCRMApplication

Java Evolution:

1991 – Project Oak by James Gosling at Sun Microsystems for embedded applications.
1995 – Oak renamed Java; launched for web development with applets.
1996 – Release of Java 1.0; "Write Once, Run Anywhere" campaign began.
1998 – Java 2 (J2SE, J2EE, J2ME) was made public for desktop, enterprise, and.
2004 (Java 5.0) – Major update with Generics, Annotations, Enhanced for-loop, Auto-boxing.
2006 - Sun open-sourced Java (OpenJDK).
2009 - Oracle bought out Sun Microsystems and became caretaker for Java.
2011 (Java 7) – New try, switch on strings.
2014 (Java 8) – A new release with Lambdas, Streams, and API.
2017 (Java 9) – Modules like Project Jigsaw
2018+ – Started 6-month release cycle for quicker releases.
Nowadays (Java 17 LTS, Java 21 LTS) – Sealed classes, pattern matching, virtual threads (Project Loom).

Java SE vs EE vs ME

Java Standard Edition - 
Core Java platform ( fundamentals).
Includes libraries: Collections, JDBC, Multithreading, etc.
Employed in desktop applications, utilities, and standalone programs.
It is the foundation for both Java ME and Java EE.

Java Enterprise Edition - 
constructed on top of Java SE with extra APIs for business solutions.
Provides Servlets, JSP, JMS, Web Services.
Designed for large scale, distributed, web based applications.
Compliant with multi-tier architecture (client, business, database).
Example: Internet banking sites, shopping sites.

Java Micro Edition - 
A subset of Java SE, optimized for resource-constrained devices.
Offer lightweight APIs for embedded devices, IoT devices, and mobile devices.
Employed in first cellular applications, PTV set top boxes, smartcards, sensors.
Small footprint and lightweight memory usage.

In short:
SE = Core Java (Foundation).
EE = Enterprise/WEB applications (based on SE). 
ME = Light-weight variant for small/embedded systems. 

JRE vs JVM vs JDK

Java Virtual Machine
Virtual machine running JVM bytecode.
This translates .class (bytecode) into CPU/OS machine code.
Guarantees platform independence ← "Write Once, Run Anywhere".
Overseeing memory (Garbage Collection), security, and execution.

Java Runtime Environment
Includes JVM + core libs to execute Java programs.
Does not include development tools.
Compatible with end users who do not care about executing Java programs.
Example: If it's a Java based game/application installation, JRE is enough.

Java Development Kit
Ultimate bundle for Java developers.
Includes JRE + development tools (compiler `javac`, debugger, documentation tools, etc.). Learners must write, assemble, and run Java programs. Used to write, construct, and debug Java programs.

Project notes
- Data exported to: ${user.home}/ccrm-data
- Minimal seed data is created by the application at startup
- To change storage path modify AppConfig.get().storageFolder() in AppConfig (simple change)
- No external libraries required
