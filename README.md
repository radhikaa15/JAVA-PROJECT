
# Campus Course & Records Manager (CCRM)

##  Project Overview

Campus Course & Records Manager (**CCRM**) is a **Java SE console application** that helps institutes manage:

* **Students** (create, update, deactivate, enrollments, transcripts)
* **Courses** (create, update, assign instructors, search/filter with streams)
* **Enrollment & Grades** (record marks, compute GPA, generate transcript)
* **File I/O** (import/export CSV, backups with timestamped folders, recursive utilities)

This project demonstrates **Java OOP principles, advanced Java features, and design patterns** in a real-world application.

---

## How to Run

1. **Requirements**

   * JDK 11+ (tested with JDK 17)
   * IDE: Eclipse / IntelliJ IDEA
   * Git (for cloning repo)

2. **Steps**

   ```bash
   git clone https://github.com/<your-username>/ccrm-project.git
   cd ccrm-project
   ```

   * Import into Eclipse as an **existing Java project**.
   * Run the main class:

     ```
     edu.ccrm.cli.CCRMApp
     ```
   * Follow the **menu-driven workflow**.

---

##  Evolution of Java

* **1995**: Java 1.0 released (Oak → Java).
* **1998**: Java 2 (J2SE, J2EE, J2ME split).
* **2004 (Java 5)**: Generics, annotations, enums, enhanced for loop.
* **2011 (Java 7)**: NIO.2, try-with-resources, diamond operator.
* **2014 (Java 8)**: Lambdas, Streams API, Date/Time API.
* **2017 (Java 9)**: Modules system.
* **2018+**: Local variable inference (`var`), records, switch expressions.

---

##  Java Editions Comparison

| Feature | Java ME         | Java SE                | Java EE (Jakarta EE)             |
| ------- | --------------- | ---------------------- | -------------------------------- |
| Scope   | Mobile/embedded | Desktop & general apps | Enterprise web apps              |
| APIs    | Limited         | Full core Java APIs    | Adds Servlets, JSP, EJB, JPA     |
| Usage   | IoT, phones     | CLI, desktop apps      | Web servers, distributed systems |
| Example | Mobile games    | Our **CCRM project**   | Banking systems                  |

---

##  JDK, JRE, JVM Explained

* **JDK (Java Development Kit)** → tools to **compile & run** Java programs.
* **JRE (Java Runtime Environment)** → runtime environment containing JVM + core libraries.
* **JVM (Java Virtual Machine)** → executes Java bytecode → machine code.

 **Flow**: Source `.java` → Compiler → `.class` (bytecode) → JVM → Machine instructions.

---

##  Install Java on Windows

1. Download JDK from [Oracle](https://www.oracle.com/java/technologies/downloads/).
2. Run installer & set environment variable:

   ```
   JAVA_HOME=C:\Program Files\Java\jdk-17
   PATH=%JAVA_HOME%\bin
   ```
3. Verify installation:

   ```bash
   java -version
   ```


---

##  Eclipse Setup

1. Open Eclipse → **File → New → Java Project**.
2. Import existing source (`src/edu/ccrm`).
3. Set run configuration: Main class = `edu.ccrm.cli.CCRMApp`.
4. Run project → see menu-driven interface.


---

##  Project Structure

```
edu.ccrm
 ├─ cli/            # Menu-driven console UI
 ├─ domain/         # Person, Student, Instructor, Course, Enrollment, Enums
 ├─ service/        # StudentService, CourseService, EnrollmentService
 ├─ io/             # Import/Export (CSV), Backup utilities
 ├─ util/           # Validators, RecursionUtil, ConsoleUtil
 └─ config/         # AppConfig (Singleton)
```

---

##  Features Demonstrated

* **Encapsulation** → Student (private fields + getters/setters).
* **Inheritance & Abstraction** → Person → Student/Instructor.
* **Polymorphism** → `toString()` overrides, service interfaces.
* **Immutability** → `CourseCode`.
* **Static Nested Class** → `Course.Builder`.
* **Inner/Anonymous Classes** → `ConsoleUtil.bannerPrinter()`.
* **Interfaces** → `StudentService`, `CourseService`.
* **Enums** → Semester, Grade (with points).
* **Design Patterns** → Singleton (`AppConfig`), Builder (`Course`).
* **Exceptions** → Custom (`DuplicateEnrollmentException`, `MaxCreditLimitExceededException`).
* **Streams & Lambdas** → Course search/filter, GPA reports.
* **Recursion** → `RecursionUtil.totalSize()`.
* **NIO.2** → Import/Export CSV, backup folders.
* **Date/Time API** → Enrollment dates, backup timestamps.

---

##  Mapping Table (syllabus → code)

| Concept           | File/Class                                                                  |
| ----------------- | --------------------------------------------------------------------------- |
| Encapsulation     | `Student.java`                                                              |
| Inheritance       | `Person.java`, `Student.java`                                               |
| Abstraction       | `Person.java` (abstract methods)                                            |
| Polymorphism      | `EnrollmentService`, `toString()` overrides                                 |
| Singleton         | `AppConfig.java`                                                            |
| Builder           | `Course.Builder`                                                            |
| Custom Exceptions | `DuplicateEnrollmentException.java`, `MaxCreditLimitExceededException.java` |
| Streams API       | `CourseServiceImpl.java`                                                    |
| Recursion         | `RecursionUtil.java`                                                        |
| Date/Time API     | `Student.java`, `Enrollment.java`, `BackupService.java`                     |
| File I/O (NIO.2)  | `ImportExportService.java`, `BackupService.java`                            |

---

##  Usage Demo

```
==== CCRM - Campus Course & Records Manager ====
1. Manage Students
2. Manage Courses
3. Enrollment & Grades
4. Import/Export
5. Backup & Size
6. Exit
```

Example session:

```
Choose option: 1
Students: 1-Add 2-List 3-PrintProfile 4-Back
Choose: 1
RegNo: 23BCY10082
Full name: Somya Shekhar Tiwari
Email: somya@example.com
DOB (yyyy-mm-dd): 2004-05-18
Added: Student{id=..., regNo=23BCY10082, ...}
```


---

##  Exports & Backups

* Exported data → `~/ccrm-data/export/students.csv`, `courses.csv`.
* Backup created → `~/ccrm-data/backup_20250924_153000/`


---

## Assertions

* Example: `assert id != null : "id must not be null";` in `Person.java`.
* Enable assertions with:

  ```bash
  java -ea edu.ccrm.cli.CCRMApp
  ```

---

##  Screenshots

*  JDK installation (`java -version`)
*  Eclipse project setup
*  Running program
*  Export/Backup folders

---

## Acknowledgements

* Oracle Java Documentation
* Java SE Tutorials (docs.oracle.com)
* StackOverflow discussions

---
## AUTHOR 
NAME- RADHIKA AGARWAL
EMAIL- radhikaa1512@gmail.com
INSTITUTION - VIT BHOPAL


