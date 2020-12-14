# Software Engineering Revision

## Sample questions

### Question 1

#### (a) Explain the concept of a version control system. Indicate the major types of such systems

- A version control system is a software package that when initiated will monitor your files for changes and allow you to tag the changes at different levels so that you can revisit those tagged stages whenever needed. Version control provides the following capabilities:
- A place to store the source code, images, build scripts, and so on needed to build your software project;
- The ability to track the history of changes to those files, and to view the state of the file at various points in the software life cycle;
- Mechanisms and tooling to make it easy to work in parallel with a team of software developers on the same project.
- There are three types of version control systems available, classified based on their mode of operation: Local version control system, Centralised version control system, Distributed version control system.

#### (b) Write short notes on each of the following in the context of version control

##### Repository

- In almost all version control systems, the repository is a central place that holds the master copy of all versions of your project’s files. Some version control systems use a database as the repository, some use regular files, and some use a combination of the two. Either way, the repository is clearly a pivotal component of your version control strategy. You need it sitting on a safe, secure and reliable machine. And it should go without saying that it needs to get backed up regularly. Most version control systems today support networked operation.

##### Strict locking

- All files that are checked out are initially flagged as being “read only”. They can be inspected, used to build an application, but can’t be edited or changed. To do that, the user has to ask the repository’s permission. If no one else is editing that same file, then the repository gives permission and changes the permission of the user’s local copy of the file to be “read/write” and they then can be edited. If anyone else asks to edit that same file while it is flagged by the user they will be refused. After the changes are finished and the file checked back in, the local copy reverts back to being read only, and it becomes available for others to edit.

##### Optimistic locking

- Each developer is permitted to edit any checked out file: the files are checked out in a read/write state. However, the repository will not allow users to check in a file that has been updated in the repository since last checked out. Instead, it asks the user to update their local copy of the file to include the latest repository changes before checking in. Instead of simply overwriting all the users work with the latest repository version of the file, the version control system attempts to merge the repository changes with the user’s changes.

### Question 2

#### (a) Describe the definition of the three model levels in Model Driven Architecture (MDA) and their links in the MDA process

The model in MDA has three levels:

- Computation independent (CIM): describes requirements and needs at a very abstract level, without any reference to implementation (computing) aspects; e.g., description of user requirements or business objectives.
- Platform independent (PIM): defines the behavior of the systems in terms of stored data and performed algorithms, without any technical or platform details;
- Platform-specific (PSM): defines all the technological aspects in detail.

Diagram found in the lectures or in *Solution of Tutorial on MDSE.doc*.

#### (b) MDA has been widely used to support code generation. Describe the code generation process supported by MDA models and techniques

The code generation process starts at requirement engineering stage, then move through design and implementation stage. The following diagram describes the links between MDA model and the code generation process.

Diagram found in the lectures or in *Solution of Tutorial on MDSE.doc*.

#### (c) In the context of MDSE, what is reverse engineering? discuss the possible outcomes of the reverse engineering

The diagram describes the input and output of reverse engineering in MDSE. The possible products are listed in the right hand end of the diagram.

Diagram found in the lectures or in *Solution of Tutorial on MDSE.doc*.

### Question 3

#### (a) Discuss the typical interface types you are likely to meet during the interface testing of software systems

Typical interfaces types include:

- Parameter interfaces: data passed from one procedure to another
- Shared memory interfaces: block of memory is shared between procedures
- Procedural interfaces: sub-system encapsulates a set of procedures to be called by other sub-systems
- Message passing interfaces: sub-systems or objects request services from other sub-systems or objects

#### (b) With examples, discuss the typical interface errors you are likely to meet during the interface testing of software systems

Popular Interface errors include:

- Interface misuse: A calling component calls another component and makes an error in its use of its interface. For example, parameters in the wrong order.
- Interface misunderstanding: A calling component embeds assumptions about the behaviour of the called component which are incorrect.
- Timing errors: The called and the calling component operate at different speeds and out-of-date information is accessed.

#### (c) Use the V-model to describe the parallel process between software development and test planning and documentation. Indicate the typical elements of test documents and discuss their roles

Test documentation is a parallel effort with development. The related process is shown in the following figure, which is known as the V-model of development:

- model found in lectures or notes

Test documents and roles:
Test documentation includes all test program documents from overall test plan through the final test report. Typically, a set of test document includes:

- Test Plan. Test plan describes the whole planned test process. It is first set up during requirement phase, and keeps evolving throughout the life cycle.
 A test plan should cover the objectives and scope, test Items, tasks and deliverables, testing approaches and schedule.
- Test Cases. Test cases are situations that simulate actual use of the software. They should be small enough to be manageable. A sample outline of test case may include test items, input specification, output specification, and inter-case dependencies.
- Test Procedures. A test procedure is a set of step-by-step instructions for the execution of a test case. It is tied to the test case and its test data.
- Test Report. After practical testing and test analysis, a test report should be completed to summarise the test results, including variances and evaluation.

### Question 4

#### (a) Explain what a User Story is and its roles in the requirement engineering in agile methodology

User stories are used in agile methodology, especially eXtreme Programming (XP). A user story is a simple description of some requirement written from a user’s viewpoint. It is usually on an index card, typically 6" x 4". A user story is not a completely defined requirement, but rather a “reference point for a conversation”. Detailed requirements will evolve through interaction between the customer and the developers. The aim is to shift toward having face-to-face conversations about requirements and technical issues.

The user stories is the centre and key drive in the requirement engineering of agile methodology. It records the key idea of requirements, provides the reference point for interaction between the user and developer, maps to the implemented product (i.e. acts as the input of implementation), and is the basis for the development of acceptance test cases.

### Question 5
  
#### (a) Software evolution is critical and inevitable for software systems. Explain the Lehman’s laws of the evolution of large tailored software system

| Law                         | Description                                                                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Continuing change           | A program that is used in a real-world environment must necessarily change, or else become progressively less useful in that environment.                                                    |
| Increasing complexity       | As an evolving program changes, its structure tends to become more complex. Extra resources must be devoted to preserving and simplifying the structure.                                     |
| Large program evolution     | Program evolution is a self-regulating process. System attributes such as size, time between releases, and the number of reported errors is approximately invariant for each system release. |
| Organizational stability    | Over a program’s lifetime, its rate of development is approximately constant and independent of the resources devoted to system development.                                                 |
| Conservation of familiarity | Over the lifetime of a system, the incremental change in each release is approximately constant.                                                                                             |
| Continuing growth           | The functionality offered by systems has to continually increase to maintain user satisfaction.                                                                                              |
| Declining quality           | The quality of systems will decline unless they are modified to reflect changes in their operational environment.                                                                            |
| Feedback system             | Evolution processes incorporate multiagent, multiloop feedback systems and you have to treat them as feedback systems to achieve significant product improvement.                            |

#### (b) Presumably, you are the manager of the evolution team of a large enterprise computing system

**Discuss what types of maintenance your team may encounter during the service of the system.**

Software maintenance is the activity to modify a software after it has been put into use. In practice, you may encounter three types of maintenance:

- Maintenance to repair software faults (corrective): Changing a system to correct deficiencies in the way meets its requirements.

- Maintenance to adapt software to a different operating environment (adaptive): Changing a system so that it operates in a different environment (computer, OS, etc.) from its initial implementation.

- Maintenance to add to or modify the system’s functionality (perfective): Modifying the system to satisfy new requirements.

**Discuss the cost factors that will affect your maintenance budget.**

Your maintenance costs may be determined by the following factors:

- Team stability: Maintenance costs are reduced if the same staff are involved with them for some time.
- Contractual responsibility: The developers of a system may have no contractual responsibility for maintenance so there is no incentive to design for future change.
- Staff skills: Maintenance staff are often inexperienced and have limited domain knowledge.
- Program age and structure: As programs age, their structure is degraded and they become harder to understand and change.

**Explain what maintenance prediction is and what you should include in such prediction.**

Maintenance prediction is concerned with assessing which parts of the system may cause problems and have high maintenance costs. Change acceptance depends on the maintainability of the components affected by the change. Implementing changes degrades the system and reduces its maintainability.

Maintenance costs depend on the number of changes and costs of change depend on maintainability. Typically, the prediction model should cover the following scope as shown in the figure below.

Refer to figure in notes.

## Exam 1

### Question 2/1

#### (a) Explain the concept of the non-functional requirements for a computing system. Describe the typical non-functional requirements to be covered during requirement engineering

Services or functions offered by the system, e.g. timing constraints. NFRs define system properties and constraints e.g. reliability, response time and storage requirements. Constraints are I/O device capability, system representations, etc. NFRs may be more critical than functional requirements. If these are not met, the system may be useless.

Figure available in : *solution of Tutoial on RE.doc*

#### (b) Explain what a User Story is and discuss its roles in the requirement engineering in agile methodology

User stories are used in agile methodology, especially eXtreme Programming (XP). A user story is a simple description of some requirement written from a user’s viewpoint. It is usually on an index card, typically 6" x 4". A user story is not a completely defined requirement, but rather a “reference point for a conversation”. Detailed requirements will evolve through interaction between the customer and the developers. The aim is to shift toward having face-to-face conversations about requirements and technical issues.

The user stories is the centre and key drive in the requirement engineering of agile methodology. It records the key idea of requirements, provides the reference point for interaction between the user and developer, maps to the implemented product (i.e. acts as the input of implementation), and is the basis for the development of acceptance test cases.

#### (c) List at least 6 stakeholders in requirement engineering and discuss the concerns that each stakeholder may have

During requirement engineering, in particular at its elicitation stage, you need to identify all the stakeholders who must be consulted. The stakeholders may come from each of the “four worlds”.

- Users - concerned with the features and functionality of the new system
- Designers – including architects and developers, who want to build a perfect system, or reuse existing code;
- Systems analysts - want to “get the requirements right”
- Training and user support staff - want to make sure the new system is usable and manageable
- Business analysts - want to make sure “we are doing better than the competition”
- Technical authors - will prepare user manuals and other documentation for the new system
- The project manager - wants to complete the project on time, within budget, with all objectives met.

### Question 2/2

Answered above, or solution available in *Solution of Tutorial on MDSE.doc*.

### Question 2/3

#### (a) Discuss the process and benefits of the following modern testing methods:  (i) thread testing; (ii) stress testing; (iii) back to back testing. Discuss what kind(s) of software systems these testing methods are suitable for

Thread testing

- Suitable for real-time and object-oriented systems
- Based on testing an operation which involves a sequence of processing steps which thread their way through the system
- Start with single event threads then go on to multiple event threads
- Complete thread testing is impossible because of the large number of event combinations

Stress testing

- Exercises the system beyond its maximum design load. Stressing the system often causes defects to come to light
- Stressing the system test failure behaviour. Systems should not fail catastrophically. Stress testing checks for unacceptable loss of service or data
- Particularly relevant to distributed systems which can exhibit severe degradation as a network becomes overloaded

Back-to-back testing

- Present the same tests to different versions of the system and compare outputs. Differing outputs imply potential problems
- Reduces the costs of examining test results. Automatic comparison of outputs.
- Possible when a prototype is available or with regression testing of a new system version

#### (b) Use the V-model to describe the parallel process between software development and test planning and documentation.  Indicate the typical elements of test documents and discuss their roles

Answerd in question 3/C. Figure for V-Model availalbe in *Solution of Tutorial on Testing 2.doc*

#### (c) The following diagram describes the behaviour of a ventilation fan control component in a workshop.  It switches its state between “on” and “off” depending on the current temperature and alarm status.  Design the at least 5 test cases for the component

You need to use boundary values and equivalent partition techniques to develop the test cases.

The occurrences of events should be considered together with boundary values and equivalent classes techniques.

Test cases:

| From off state         |                                         |
|------------------------|-----------------------------------------|
| input: alarm on;       | output: state transition from off to on |
| input: temperature=25; | output: state transition from off to on |

| From on state:                       |                                         |
|--------------------------------------|-----------------------------------------|
| input: alarm off and temperature=24; | output: state transition from on to off |
| input: alarm off and temperature=25; | output: no state transition             |
| input: alarm on and temperature=24;  | output: no state transition             |

## Exam 2

### Question 3/2

#### (a) Modularity is a critical issue for producing high quality and highly maintainable software. Explain the concept of modularity. Describe the existing approaches to enforce modularity, i.e. to create a truly modular system

Modularising a software design refers to a logical partitioning of the system design that allows complex software to be manageable for the purpose of implementation and maintenance. The logic of partitioning may be based on related functions, implementation considerations, data, or other criteria. The term modularity is widely used, and systems are deemed modular when they can be decomposed into a number of components that may be mixed and matched in a variety of configurations. Such components are able to connect, interact, or exchange resources (data) in some way by adhering to a standardised interface. Modular applications are systems of components that are loosely coupled.

To create a truly modular system, it is important to not only have it modular in the design phase, but to also take that design and implement it in such a way that it is still modular at runtime. Modularity can therefore be subdivided in both design time modularity and runtime modularity:
Design time modularity:

- Similar to object-oriented programming, there is no silver bullet that will magically introduce modularity. There are trade-offs to be made, and patterns exist to help you do so. The most important step toward modularity is coming up with a logical separation of modules. This is basically what most architects will do, but they do this on the level of systems and layers. We need to do this on the code level as well, on a much more fine-grained level. This means that modularity doesn’t come for free: we need to actively work toward it. Just throwing a framework in the mix will not make a system modular all of a sudden.

Runtime modularity

- Identifying modules in a design will already help, creating a clear design. Without a runtime environment that respects modules, it is very hard to enforce modularity. Enforcing sounds like a bad thing, and you might say that it is the role of developers to respect modularity. It certainly is our job as developers to do so, but we can use some help. It is very difficult to not accidentally break modularity by just relying on standards and guidelines when working in a large code base. It’s much easier to work with modules if our runtime supports it. The runtime should at least:
  - Enforce module isolation – a module should only be used by an explicitly defined API, and the runtime should make sure that other classes and interfaces are not visible to the outside world;
  - Enforce and clarify module dependencies – making sure that modules only depend on a well-defined set of other modules, and a module should not load when its dependencies are not resolved;
  - Provide a services framework to consume modules – typically a Service Registry using Dependency Injection.

#### (b) Describe the architecture of OSGi framework. Discuss how to use OSGi framework to achieve good modularity in software development

OSGi is the only mature modularity solution for Java today, and that is unlikely to change anytime soon. Although OSGi has been criticized for being too complex to use in the past, recent improvements to tooling and frameworks have changed this completely.

Nowadays OSGi is applied in a much broader field and has become the de facto modularity solution in Java. When using OSGi, you need an implementation. The most popular OSGi implementations are Apache Felix and Eclipse Equinox. Both are mature implementations, but Equinox tends to be a little more heavyweight, and there are some implementation choices that only make sense for Eclipse usage (the Eclipse IDE is built entirely on top of OSGi). It really doesn’t matter much which implementation is used however, because the bundles you create and the compendium services run on any implementation.

In the past few years, a lot of progress has been made on OSGi tooling. When considering a good tool for OSGi development, we have a list of requirements it should take care of:

- Automatically generate bundle JAR files;
- Generate package imports using byte code analysis;
- Provide an easy way to start an OSGi container to run and test our code;
- Hot code updates in a running container for a fast development turnaround;
- Run in-container integration tests;
- Help with versioning of bundles.

##### new source

The OSGi(Open Services Gateway initiative) framework provides a dynamic modular architecture which has been used in many applications such as Eclipse Equinox, Apache Felix, etc.

OSGi framework architecture consists three conceptual layers. Each layer is dependent on the layer(s) beneath it. The diagram below describe the overview of each layer.

<https://www.programcreek.com/wp-content/uploads/2011/07/OSGiLayeredArchitecture1.jpg>

**Module layer**
Module layer defines OSGi module concept - bundle, which is a JAR file with extra metadata. A bundle contains class files and related resources such as images, xml files.

Through manifest.mf metadata file, Module layer declare which contained packages in JAR file are visible to outside, and declare on which external packages the bundle depend.

Some metadata examples:
Export-Package: com.programcreek.helloexport
It declares which packages are visible to users.
Import-Package: com.programcreek.helloimport
It declares when external packages are required.

Lifecycle layer:

- This layer defines how bundles are dynamically installed and managed in the OSGi framework. It provides a way for a bundle to gain access to the underlying OSGi framework.
- If OSGi were a car, module layer would provide modules such as tire, seat, etc, and the lifecycle layer would provide electrical wiring which makes the car run.

Service layer:

- In this layer, service providers publish services to service registry, while service clients search the registry to find available services to use.
- This is like a service-oriented architecture (SOA) which has been largely used in web services. Here OSGi services are local to a single VM, so it is sometimes called SOA in a VM.
<https://www.osgi.org/developer/modularity/>

### Question 3/3

#### (a) With examples, discuss the typical interface errors you are likely to meet during the interface testing of software systems

answered in Question 3

#### (b) Testing the non-functional aspects of reusable components is an important issue, in particular in real-time embedded systems. Discuss what the **guidelines** should be for reusing and testing software components in such an environment

The basic idea is to provide evidence, based on the component’s contracts and the experience accumulated, that a component can be reused immediately, that only parts can be reused, or that it cannot be reused.

Reliability requirement:

- The principle is that a component may be reused in a context with lower reliability requirements. However, previously experienced reliability cannot be utilized if input domains are outside historical use of the component. After run for an adequately long time and properly adapted, the component could reach a higher reliability.

Deadline Requirement:

- If we reuse a component with only a deadline requirement in a new environment in which the execution time is shorter, the component can be reused without re-testing.

Timing Failure Behaviour:

- This failure mode yields a correct result (value), although the procurement of the result is time-wise incorrect. For example, deadline violations, start of task too early, incorrect period time, too much jitter, too many interrupts.

#### (c) Test-Driven Development (TDD) is a new approach to software development and testing. Describe the TDD approach and discuss the benefits it has (Lecture - Software Testing 2)

Test-driven development (TDD) is an approach to program development in which you inter-leave testing and code development. Tests are written before code and ‘passing’ the tests is the critical driver of development.  You develop code incrementally, along with a test for that increment. You don’t move on to the next increment until the code that you have developed passes its test. TDD was introduced as part of agile methods such as Extreme Programming. However, it can also be used in plan-driven development processes.

Start by identifying the increment of functionality that is required. This should normally be small and implementable in a few lines of code. Write a test for this functionality and implement this as an automated test. Run the test, along with all other tests that have been implemented. Initially, you have not implemented the functionality so the new test will fail. Implement the functionality and re-run the test. Once all tests run successfully, you move on to implementing the next chunk of functionality.

Benefits of test-driven development:

- Code coverage. Every code segment that you write has at least one associated test so all code written has at least one test.
- Regression testing. A regression test suite is developed incrementally as a program is developed.
- Simplified debugging. When a test fails, it should be obvious where the problem lies. The newly written code needs to be checked and modified.
- System documentation. The tests themselves are a form of documentation that describes what the code should be doing.

### Question 3/4

#### (a) Software evolution is critical and inevitable for software systems. Explain the Lehman’s laws of the evolution of large tailored software system (2)

answered above at Question 5.

#### (b) To assure the quality of a software system, the developers must comply with a set of design principles. List 4 of these design principles and discuss how they help to improve the software quality

A set of guidelines which when applied appropriately should result in good quality software.

bro this list would be like 4 pages long

SOLID

SOLID is an acronym formed by the names of 5 design principles centered around better code design, maintainability, and extendability.

- write code that’s easy to maintain;
- make it easier to extend the system with new functionality without breaking the existing ones;
- write code that’s easy to read and understand.

Single Responsibility Principle

- These should never be more than one reason for a class to change
- Single responsibility means that your class should only do one thing. If your class is responsible for getting users’ data from the database, it shouldn’t care about displaying the data as well. Those are different responsibilities and should be handled separately.

Open/Closed Principle

- A module should be open for extension but closed for modification
- The Open/Closed Principle states that a module should be open for extension, but closed for modification. That means you should be able to extend a module with new features not by changing its source code, but by adding new code instead. The goal is to keep working, tested code intact, so over time, it becomes bug resistant.

Liskov Substitution Principle

- Subclasses should be substitutable for their base classes
- You should be able to substitute a parent class with any of its child classes, without breaking the system. Putting it more simply, implementations of the same interface should never give a different result.

Interface Segregation Principle

- Clients should not be forced to depend upon interfaces that they do not use
- The Interface Segregation Principle states that you should never force the client to depend on methods it doesn’t use.
- Rather than loading the class which has multiple clients with all the methods that the clients need, create specific interfaces for each client and multiply inherit them into the class.

Dependency Inversion Principle

- The dependency inversion principle states that high-level modules should not depend on low-level modules - both should depend on abstractions.
- Abstractions should not depend upon details. Details should depend upon abstractions.

#### (c) Indicate the major types of version control systems. Discuss the advantages that using a version control system (e.g. SVN, GIT) can bring to a software project

There are three types of version control systems available, classified based on their mode of operation:

- **Local version control system** – It works by keeping patch sets (that is, the difference between the file's content at progressive stages) using a special format in the version tracker that is stored in your local hard disk. It can then recreate the file's contents exactly at any given point in time by adding up all the relevant patches in order and "checking it out" (reproducing the content to the user's workplace).
- **Centralised version control system** – People were not able to work collaboratively on the same project, as the files with their versions are stored in somebody's local computer and were not accessible to other people working on the same files. This is solved by keeping the files in a common place (server) that everybody has access to from their local machines (clients). Hence, the birth of a centralized version control system. Whenever people want to edit single or multiple files only the last version of the files are retrieved. As the files are stored in one single location from which everybody needs to share the files, any changes made to the files are automatically shared with other individuals as well.
- **Distributed version control system** – There is a high degree of risk involved in using a centralised version control system because the users only have the last version of files in their system for working purposes; there is a chance you might ultimately lose the entire history of your files if the server gets corrupt and if you don't have fail-safe procedures implemented. A distributed version control system is designed to act both ways. It stores the entire history of the file/files on each and every machine locally and also syncs the local changes made by the user back to the server whenever required so that the changes can be shared with others providing a collaborative working environment. There are several other advantages in terms of performance, ease of use, and administration. It's a general saying that "you name anything that a centralized version control system can perform; a distributed version control system can handle the same thing and perform much better".

Version Control advantages:

- Central repository is easier to secure/backup;
- An audit trail of source code versions and changes made;
- The ability to roll-back to specific versions of the source;
- Support for team development via techniques such as locking;
- Creating and joining of branches allows for the release/support of different software versions.
