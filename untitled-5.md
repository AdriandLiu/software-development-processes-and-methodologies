# Engineering Practices for Building Quality Software

Engineering Practices for Building Quality Software 

Welcome to Engineering Processes for Building Quality Software! 

Quality comes in a variety of variations. Functional correctness, which most training in programming languages and "coding" focus on, is well established in courses while you're learning to be a developer. The other factors of quality tend to be less emphasized, if not ignored entirely. The modules in this course will begin to fill in these gaps, as well as orient learners to the ways in which these areas of quality can be addressed. 

Each of six common development stages will be examined. From design to final project deployment, quality can be injected into every action taken towards product success. However, measuring that quality and proving that it exceeds the level necessary to satisfy the requirements of each relevant stakeholder. 

In this course, learners will display the knowledge through quizzes and apply their learning by: 

* writing quality scenarios to evaluate quality attributes quantitatively, 
* reviewing good code style and critiquing real-world examples of code style, 
* learn about static analysis and tools to automatically identify issues in code, and 
* assessing the use of comments and self-documentation to provide context to written code. 

Divided into four weeks, the course provides a sweeping introduction to quality in the software development lifecycle. In addition to explanatory lectures and opportunities to evaluate a variety of sources of software quality, a curated set of resources allow the learner to dive deeper into the content. 

What is Quality Software 

The standard of something as measured against other things of a similar kind, the degree of excellence of something 

Of good quality: excellent 

Quality throughout the engineering process 

* Design 
* Architecture & Security 
* Implementation 
* Testing & Deployment 

Design 

* What does good design look like 
* Coupling, cohesion and more 
* Quality metrics 
* Software design patterns 

Architecture & Security 

* Security 
* Usability 
* Performance 
* Availability 

Implementation 

* Code Style – coding standard 
* Debugging 
* Commenting – documentation within the code 
* Build Process 

Testing & Deployment 

* Test Selection 
* Test Adequacy 
* Continuous Integration 
* Continuous Deployment 

Striving for quality throughout the lifecycle 

Variety of approaches across 6 content areas 

Practical measures of quality 

Identifying problems before they start 

What is good design? 

‘Good’ 

What is software?  

Software quality attributes 

* Performance 
* Security 
* Modifiability 
* Reliability 
* Usability 

Coupling & Cohesion 

Coupling – The level of dependency between 2 entities 

Cohesion – How well an entity’s components related to one another 

Liskov’s substitution Principle 

If S is a subtype of T, then objects of type T in a program may be replaced with objects of type S without altering any of the desirable properties of that program eg. Correctness 

SOLID 

S – Single responsibility 

O – Open/Closed principle 

L – Liskov substitution principle 

I – Interface segregation principle 

D – Dependency inversion principle 

Law of Demeter 

Principle of least knowledge 

Formally a method m of an object O may only invoke the methods of the following kinds of objects 

O itself 

M’s parameters 

Any objects created/instantiated within m 

O’s direct component objects 

A global variable, accessible by O in the scope of m 

Consider the effects of your work in a variety of perspectives 

Quality attributes help answer – When is it good enough? 

Quality criteria help identify locations which need extra care 

Improving one often degrades another – choose wisely 

What is software? 

https://docs.microsoft.com/en-us/previous-versions/msp-n-p/ee658094\(v=pandp.10\) 

Chapter 16: Quality Attributes 

* 01/13/2010 
* 22 minutes to read 

For more details of the topics covered in this guide, see [Contents of the Guide](https://docs.microsoft.com/en-us/previous-versions/msp-n-p/ee658086%28v%3dpandp.10%29). 

Contents 

* Overview 
* Common Quality Attributes 
* Additional Resources 

Overview 

Quality attributes are the overall factors that affect run-time behavior, system design, and user experience. They represent areas of concern that have the potential for application wide impact across layers and tiers. Some of these attributes are related to the overall system design, while others are specific to run time, design time, or user centric issues. The extent to which the application possesses a desired combination of quality attributes such as usability, performance, reliability, and security indicates the success of the design and the overall quality of the software application. 

When designing applications to meet any of the quality attributes requirements, it is necessary to consider the potential impact on other requirements. You must analyze the tradeoffs between multiple quality attributes. The importance or priority of each quality attribute differs from system to system; for example, interoperability will often be less important in a single use packaged retail application than in a line of business \(LOB\) system. 

This chapter lists and describes the quality attributes that you should consider when designing your application. To get the most out of this chapter, use the table below to gain an understanding of how quality attributes map to system and application quality factors, and read the description of each of the quality attributes. Then use the sections containing key guidelines for each of the quality attributes to understand how that attribute has an impact on your design, and to determine the decisions you must make to addresses these issues. Keep in mind that the list of quality attributes in this chapter is not exhaustive, but provides a good starting point for asking appropriate questions about your architecture. 

Common Quality Attributes 

The following table describes the quality attributes covered in this chapter. It categorizes the attributes in four specific areas linked to design, runtime, system, and user qualities. Use this table to understand what each of the quality attributes means in terms of your application design. 

| Category  | Quality attribute  | Description  |
| :--- | :--- | :--- |
| Design Qualities  | Conceptual Integrity  | Conceptual integrity defines the consistency and coherence of the overall design. This includes the way that components or modules are designed, as well as factors such as coding style and variable naming.  |
| Maintainability  | Maintainability is the ability of the system to undergo changes with a degree of ease. These changes could impact components, services, features, and interfaces when adding or changing the functionality, fixing errors, and meeting new business requirements.  |  |
| Reusability  | Reusability defines the capability for components and subsystems to be suitable for use in other applications and in other scenarios. Reusability minimizes the duplication of components and also the implementation time.  |  |
| Run-time Qualities  | Availability  | Availability defines the proportion of time that the system is functional and working. It can be measured as a percentage of the total system downtime over a predefined period. Availability will be affected by system errors, infrastructure problems, malicious attacks, and system load.  |
| Interoperability  | Interoperability is the ability of a system or different systems to operate successfully by communicating and exchanging information with other external systems written and run by external parties. An interoperable system makes it easier to exchange and reuse information internally as well as externally.  |  |
| Manageability  | Manageability defines how easy it is for system administrators to manage the application, usually through sufficient and useful instrumentation exposed for use in monitoring systems and for debugging and performance tuning.   |  |
| Performance  | Performance is an indication of the responsiveness of a system to execute any action within a given time interval. It can be measured in terms of latency or throughput. Latency is the time taken to respond to any event. Throughput is the number of events that take place within a given amount of time.  |  |
| Reliability  | Reliability is the ability of a system to remain operational over time. Reliability is measured as the probability that a system will not fail to perform its intended functions over a specified time interval.  |  |
| Scalability  | Scalability is ability of a system to either handle increases in load without impact on the performance of the system, or the ability to be readily enlarged.  |  |
| Security  | Security is the capability of a system to prevent malicious or accidental actions outside of the designed usage, and to prevent disclosure or loss of information. A secure system aims to protect assets and prevent unauthorized modification of information.  |  |
| System Qualities  | Supportability  | Supportability is the ability of the system to provide information helpful for identifying and resolving issues when it fails to work correctly.  |
| Testability  | Testability is a measure of how easy it is to create test criteria for the system and its components, and to execute these tests in order to determine if the criteria are met. Good testability makes it more likely that faults in a system can be isolated in a timely and effective manner.  |  |
| User Qualities  | Usability  | Usability defines how well the application meets the requirements of the user and consumer by being intuitive, easy to localize and globalize, providing good access for disabled users, and resulting in a good overall user experience.  |

The following sections describe each of the quality attributes in more detail, and provide guidance on the key issues and the decisions you must make for each one: 

* Availability 
* Conceptual Integrity 
* Interoperability 
* Maintainability 
* Manageability 
* Performance 
* Reliability 
* Reusability 
* Scalability 
* Security 
* Supportability 
* Testability 
* User Experience / Usability 

Availability 

Availability defines the proportion of time that the system is functional and working. It can be measured as a percentage of the total system downtime over a predefined period. Availability will be affected by system errors, infrastructure problems, malicious attacks, and system load. The key issues for availability are: 

* A physical tier such as the database server or application server can fail or become unresponsive, causing the entire system to fail. Consider how to design failover support for the tiers in the system. For example, use Network Load Balancing for Web servers to distribute the load and prevent requests being directed to a server that is down. Also, consider using a RAID mechanism to mitigate system failure in the event of a disk failure. Consider if there is a need for a geographically separate redundant site to failover to in case of natural disasters such as earthquakes or tornados. 
* Denial of Service \(DoS\) attacks, which prevent authorized users from accessing the system, can interrupt operations if the system cannot handle massive loads in a timely manner, often due to the processing time required, or network configuration and congestion. To minimize interruption from DoS attacks, reduce the attack surface area, identify malicious behavior, use application instrumentation to expose unintended behavior, and implement comprehensive data validation. Consider using the Circuit Breaker or Bulkhead patterns to increase system resiliency. 
* Inappropriate use of resources can reduce availability. For example, resources acquired too early and held for too long cause resource starvation and an inability to handle additional concurrent user requests. 
* Bugs or faults in the application can cause a system wide failure. Design for proper exception handling in order to reduce application failures from which it is difficult to recover. 
* Frequent updates, such as security patches and user application upgrades, can reduce the availability of the system. Identify how you will design for run-time upgrades. 
* A network fault can cause the application to be unavailable. Consider how you will handle unreliable network connections; for example, by designing clients with occasionally-connected capabilities. 
* Consider the trust boundaries within your application and ensure that subsystems employ some form of access control or firewall, as well as extensive data validation, to increase resiliency and availability. 

Conceptual Integrity 

Conceptual integrity defines the consistency and coherence of the overall design. This includes the way that components or modules are designed, as well as factors such as coding style and variable naming. A coherent system is easier to maintain because you will know what is consistent with the overall design. Conversely, a system without conceptual integrity will constantly be affected by changing interfaces, frequently deprecating modules, and lack of consistency in how tasks are performed. The key issues for conceptual integrity are: 

* Mixing different areas of concern within your design. Consider identifying areas of concern and grouping them into logical presentation, business, data, and service layers as appropriate. 
* Inconsistent or poorly managed development processes. Consider performing an Application Lifecycle Management \(ALM\) assessment, and make use of tried and tested development tools and methodologies. 
* Lack of collaboration and communication between different groups involved in the application lifecycle. Consider establishing a development process integrated with tools to facilitate process workflow, communication, and collaboration. 
* Lack of design and coding standards. Consider establishing published guidelines for design and coding standards, and incorporating code reviews into your development process to ensure guidelines are followed. 
* Existing \(legacy\) system demands can prevent both refactoring and progression toward a new platform or paradigm. Consider how you can create a migration path away from legacy technologies, and how to isolate applications from external dependencies. For example, implement the Gateway design pattern for integration with legacy systems. 

Interoperability 

Interoperability is the ability of a system or different systems to operate successfully by communicating and exchanging information with other external systems written and run by external parties. An interoperable system makes it easier to exchange and reuse information internally as well as externally. Communication protocols, interfaces, and data formats are the key considerations for interoperability. Standardization is also an important aspect to be considered when designing an interoperable system. The key issues for interoperability are: 

* Interaction with external or legacy systems that use different data formats. Consider how you can enable systems to interoperate, while evolving separately or even being replaced. For example, use orchestration with adaptors to connect with external or legacy systems and translate data between systems; or use a canonical data model to handle interaction with a large number of different data formats. 
* Boundary blurring, which allows artifacts from one system to defuse into another. Consider how you can isolate systems by using service interfaces and/or mapping layers. For example, expose services using interfaces based on XML or standard types in order to support interoperability with other systems. Design components to be cohesive and have low coupling in order to maximize flexibility and facilitate replacement and reusability. 
* Lack of adherence to standards. Be aware of the formal and de facto standards for the domain you are working within, and consider using one of them rather than creating something new and proprietary. 

Maintainability 

Maintainability is the ability of the system to undergo changes with a degree of ease. These changes could impact components, services, features, and interfaces when adding or changing the application’s functionality in order to fix errors, or to meet new business requirements. Maintainability can also affect the time it takes to restore the system to its operational status following a failure or removal from operation for an upgrade. Improving system maintainability can increase availability and reduce the effects of run-time defects. An application’s maintainability is often a function of its overall quality attributes but there a number of key issues that can directly affect maintainability: 

* Excessive dependencies between components and layers, and inappropriate coupling to concrete classes, prevents easy replacement, updates, and changes; and can cause changes to concrete classes to ripple through the entire system. Consider designing systems as well-defined layers, or areas of concern, that clearly delineate the system’s UI, business processes, and data access functionality. Consider implementing cross-layer dependencies by using abstractions \(such as abstract classes or interfaces\) rather than concrete classes, and minimize dependencies between components and layers. 
* The use of direct communication prevents changes to the physical deployment of components and layers. Choose an appropriate communication model, format, and protocol. Consider designing a pluggable architecture that allows easy upgrades and maintenance, and improves testing opportunities, by designing interfaces that allow the use of plug-in modules or adapters to maximize flexibility and extensibility. 
* Reliance on custom implementations of features such as authentication and authorization prevents reuse and hampers maintenance. To avoid this, use the built-in platform functions and features wherever possible. 
* The logic code of components and segments is not cohesive, which makes them difficult to maintain and replace, and causes unnecessary dependencies on other components. Design components to be cohesive and have low coupling in order to maximize flexibility and facilitate replacement and reusability. 
* The code base is large, unmanageable, fragile, or over complex; and refactoring is burdensome due to regression requirements. Consider designing systems as well defined layers, or areas of concern, that clearly delineate the system’s UI, business processes, and data access functionality. Consider how you will manage changes to business processes and dynamic business rules, perhaps by using a business workflow engine if the business process tends to change. Consider using business components to implement the rules if only the business rule values tend to change; or an external source such as a business rules engine if the business decision rules do tend to change. 
* The existing code does not have an automated regression test suite. Invest in test automation as you build the system. This will pay off as a validation of the system’s functionality, and as documentation on what the various parts of the system do and how they work together. 
* Lack of documentation may hinder usage, management, and future upgrades. Ensure that you provide documentation that, at minimum, explains the overall structure of the application. 

Manageability 

Manageability defines how easy it is for system administrators to manage the application, usually through sufficient and useful instrumentation exposed for use in monitoring systems and for debugging and performance tuning. Design your application to be easy to manage, by exposing sufficient and useful instrumentation for use in monitoring systems and for debugging and performance tuning. The key issues for manageability are: 

* Lack of health monitoring, tracing, and diagnostic information. Consider creating a health model that defines the significant state changes that can affect application performance, and use this model to specify management instrumentation requirements. Implement instrumentation, such as events and performance counters, that detects state changes, and expose these changes through standard systems such as Event Logs, Trace files, or Windows Management Instrumentation \(WMI\). Capture and report sufficient information about errors and state changes in order to enable accurate monitoring, debugging, and management. Also, consider creating management packs that administrators can use in their monitoring environments to manage the application. 
* Lack of runtime configurability. Consider how you can enable the system behavior to change based on operational environment requirements, such as infrastructure or deployment changes. 
* Lack of troubleshooting tools. Consider including code to create a snapshot of the system’s state to use for troubleshooting, and including custom instrumentation that can be enabled to provide detailed operational and functional reports. Consider logging and auditing information that may be useful for maintenance and debugging, such as request details or module outputs and calls to other systems and services. 

Performance 

Performance is an indication of the responsiveness of a system to execute specific actions in a given time interval. It can be measured in terms of latency or throughput. Latency is the time taken to respond to any event. Throughput is the number of events that take place in a given amount of time. An application’s performance can directly affect its scalability, and lack of scalability can affect performance. Improving an application’s performance often improves its scalability by reducing the likelihood of contention for shared resources. Factors affecting system performance include the demand for a specific action and the system’s response to the demand. The key issues for performance are: 

* Increased client response time, reduced throughput, and server resource over utilization. Ensure that you structure the application in an appropriate way and deploy it onto a system or systems that provide sufficient resources. When communication must cross process or tier boundaries, consider using coarse-grained interfaces that require the minimum number of calls \(preferably just one\) to execute a specific task, and consider using asynchronous communication. 
* Increased memory consumption, resulting in reduced performance, excessive cache misses \(the inability to find the required data in the cache\), and increased data store access. Ensure that you design an efficient and appropriate caching strategy. 
* Increased database server processing, resulting in reduced throughput. Ensure that you choose effective types of transactions, locks, threading, and queuing approaches. Use efficient queries to minimize performance impact, and avoid fetching all of the data when only a portion is displayed. Failure to design for efficient database processing may incur unnecessary load on the database server, failure to meet performance objectives, and costs in excess of budget allocations. 
* Increased network bandwidth consumption, resulting in delayed response times and increased load for client and server systems. Design high performance communication between tiers using the appropriate remote communication mechanism. Try to reduce the number of transitions across boundaries, and minimize the amount of data sent over the network. Batch work to reduce calls over the network. 

Reliability 

Reliability is the ability of a system to continue operating in the expected way over time. Reliability is measured as the probability that a system will not fail and that it will perform its intended function for a specified time interval. The key issues for reliability are: 

* The system crashes or becomes unresponsive. Identify ways to detect failures and automatically initiate a failover, or redirect load to a spare or backup system. Also, consider implementing code that uses alternative systems when it detects a specific number of failed requests to an existing system. 
* Output is inconsistent. Implement instrumentation, such as events and performance counters, that detects poor performance or failures of requests sent to external systems, and expose information through standard systems such as Event Logs, Trace files, or WMI. Log performance and auditing information about calls made to other systems and services. 
* The system fails due to unavailability of other externalities such as systems, networks, and databases. Identify ways to handle unreliable external systems, failed communications, and failed transactions. Consider how you can take the system offline but still queue pending requests. Implement store and forward or cached message-based communication systems that allow requests to be stored when the target system is unavailable, and replayed when it is online. Consider using Windows Message Queuing or BizTalk Server to provide a reliable once-only delivery mechanism for asynchronous requests. 

Reusability 

Reusability is the probability that a component will be used in other components or scenarios to add new functionality with little or no change. Reusability minimizes the duplication of components and the implementation time. Identifying the common attributes between various components is the first step in building small reusable components for use in a larger system. The key issues for reusability are: 

* The use of different code or components to achieve the same result in different places; for example, duplication of similar logic in multiple components, and duplication of similar logic in multiple layers or subsystems. Examine the application design to identify common functionality, and implement this functionality in separate components that you can reuse. Examine the application design to identify crosscutting concerns such as validation, logging, and authentication, and implement these functions as separate components. 
* The use of multiple similar methods to implement tasks that have only slight variation. Instead, use parameters to vary the behavior of a single method. 
* Using several systems to implement the same feature or function instead of sharing or reusing functionality in another system, across multiple systems, or across different subsystems within an application. Consider exposing functionality from components, layers, and subsystems through service interfaces that other layers and systems can use. Use platform agnostic data types and structures that can be accessed and understood on different platforms. 

Scalability 

Scalability is ability of a system to either handle increases in load without impact on the performance of the system, or the ability to be readily enlarged. There are two methods for improving scalability: scaling vertically \(scale up\), and scaling horizontally \(scale out\). To scale vertically, you add more resources such as CPU, memory, and disk to a single system. To scale horizontally, you add more machines to a farm that runs the application and shares the load. The key issues for scalability are: 

* Applications cannot handle increasing load. Consider how you can design layers and tiers for scalability, and how this affects the capability to scale up or scale out the application and the database when required. You may decide to locate logical layers on the same physical tier to reduce the number of servers required while maximizing load sharing and failover capabilities. Consider partitioning data across more than one database server to maximize scale-up opportunities and allow flexible location of data subsets. Avoid stateful components and subsystems where possible to reduce server affinity. 
* Users incur delays in response and longer completion times. Consider how you will handle spikes in traffic and load. Consider implementing code that uses additional or alternative systems when it detects a predefined service load or a number of pending requests to an existing system. 
* The system cannot queue excess work and process it during periods of reduced load. Implement store-and-forward or cached message-based communication systems that allow requests to be stored when the target system is unavailable, and replayed when it is online. 

Security 

Security is the capability of a system to reduce the chance of malicious or accidental actions outside of the designed usage affecting the system, and prevent disclosure or loss of information. Improving security can also increase the reliability of the system by reducing the chances of an attack succeeding and impairing system operation. Securing a system should protect assets and prevent unauthorized access to or modification of information. The factors affecting system security are confidentiality, integrity, and availability. The features used to secure systems are authentication, encryption, auditing, and logging. The key issues for security are: 

* Spoofing of user identity. Use authentication and authorization to prevent spoofing of user identity. Identify trust boundaries, and authenticate and authorize users crossing a trust boundary. 
* Damage caused by malicious input such as SQL injection and cross-site scripting. Protect against such damage by ensuring that you validate all input for length, range, format, and type using the constrain, reject, and sanitize principles. Encode all output you display to users. 
* Data tampering. Partition the site into anonymous, identified, and authenticated users and use application instrumentation to log and expose behavior that can be monitored. Also use secured transport channels, and encrypt and sign sensitive data sent across the network 
* Repudiation of user actions. Use instrumentation to audit and log all user interaction for application critical operations. 
* Information disclosure and loss of sensitive data. Design all aspects of the application to prevent access to or exposure of sensitive system and application information. 
* Interruption of service due to Denial of service \(DoS\) attacks. Consider reducing session timeouts and implementing code or hardware to detect and mitigate such attacks. 

Supportability 

Supportability is the ability of the system to provide information helpful for identifying and resolving issues when it fails to work correctly. The key issues for supportability are: 

* Lack of diagnostic information. Identify how you will monitor system activity and performance. Consider a system monitoring application, such as Microsoft System Center. 
* Lack of troubleshooting tools. Consider including code to create a snapshot of the system’s state to use for troubleshooting, and including custom instrumentation that can be enabled to provide detailed operational and functional reports. Consider logging and auditing information that may be useful for maintenance and debugging, such as request details or module outputs and calls to other systems and services. 
* Lack of tracing ability. Use common components to provide tracing support in code, perhaps though Aspect Oriented Programming \(AOP\) techniques or dependency injection. Enable tracing in Web applications in order to troubleshoot errors. 
* Lack of health monitoring. Consider creating a health model that defines the significant state changes that can affect application performance, and use this model to specify management instrumentation requirements. Implement instrumentation, such as events and performance counters, that detects state changes, and expose these changes through standard systems such as Event Logs, Trace files, or Windows Management Instrumentation \(WMI\). Capture and report sufficient information about errors and state changes in order to enable accurate monitoring, debugging, and management. Also, consider creating management packs that administrators can use in their monitoring environments to manage the application. 

Testability 

Testability is a measure of how well system or components allow you to create test criteria and execute tests to determine if the criteria are met. Testability allows faults in a system to be isolated in a timely and effective manner. The key issues for testability are: 

* Complex applications with many processing permutations are not tested consistently, perhaps because automated or granular testing cannot be performed if the application has a monolithic design. Design systems to be modular to support testing. Provide instrumentation or implement probes for testing, mechanisms to debug output, and ways to specify inputs easily. Design components that have high cohesion and low coupling to allow testability of components in isolation from the rest of the system. 
* Lack of test planning. Start testing early during the development life cycle. Use mock objects during testing, and construct simple, structured test solutions. 
* Poor test coverage, for both manual and automated tests. Consider how you can automate user interaction tests, and how you can maximize test and code coverage. 
* Input and output inconsistencies; for the same input, the output is not the same and the output does not fully cover the output domain even when all known variations of input are provided. Consider how to make it easy to specify and understand system inputs and outputs to facilitate the construction of test cases. 

User Experience / Usability 

The application interfaces must be designed with the user and consumer in mind so that they are intuitive to use, can be localized and globalized, provide access for disabled users, and provide a good overall user experience. The key issues for user experience and usability are: 

* Too much interaction \(an excessive number of clicks\) required for a task. Ensure you design the screen and input flows and user interaction patterns to maximize ease of use. 
* Incorrect flow of steps in multistep interfaces. Consider incorporating workflows where appropriate to simplify multistep operations. 
* Data elements and controls are poorly grouped. Choose appropriate control types \(such as option groups and check boxes\) and lay out controls and content using the accepted UI design patterns. 
* Feedback to the user is poor, especially for errors and exceptions, and the application is unresponsive. Consider implementing technologies and techniques that provide maximum user interactivity, such as Asynchronous JavaScript and XML \(AJAX\) in Web pages and client-side input validation. Use asynchronous techniques for background tasks, and tasks such as populating controls or performing long-running tasks. 

Additional Resources 

For more information on implementing and auditing quality attributes, see the following resources: 

* "Implementing System-Quality Attributes" at [http://msdn.microsoft.com/en-us/library/bb402962.aspx](http://msdn.microsoft.com/en-us/library/bb402962.aspx). 
* "Software Architecture in the New Economy" at [http://msdn.microsoft.com/en-us/library/cc168642.aspx](http://msdn.microsoft.com/en-us/library/cc168642.aspx). 
* "Quality-Attribute Auditing: The What, Why, and How" at [http://msdn.microsoft.com/en-us/library/bb508961.aspx](http://msdn.microsoft.com/en-us/library/bb508961.aspx). 
* Feathers, Michael. Working Effectively With Legacy Code. Prentice Hall, 2004. 
* Baley, Kyle and Donald Belcham. Brownfield Application Development in .NET. Manning Publications Co, 2008. 
* Nygard, Michael. Release It!: Design and Deploy Production-Ready Software. Pragmatic Bookshelf, 2007. 

[https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=12433](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=12433) 

Quality Attributes 

Abstract 

Computer systems are used in many critical applications where a failure can have serious consequences \(loss of lives or property\). Developing systematic ways to relate the software quality attributes of a system to the system's architecture provides a sound basis for making objective decisions about design trade-offs and enables engineers to make reasonably accurate predictions about a system's attributes that are free from bias and hidden assumptions. The ultimate goal is the ability to quantitatively evaluate and trade off multiple software quality attributes to arrive at a better overall system. The purpose of this report is to take a small step in the direction of developing a unifying approach for reasoning about multiple software quality attributes. In this report, we define software quality, introduce a generic taxonomy of attributes, discuss the connections between the attributes, and discuss future work leading to an attribute-based methodology for evaluating software architectures. 

Quality Metrics 

Measuring Coupling 

Degree to which entities on each other 

Instability 

A metric to help identify problematic relationships between entities 

Measures the potential for change to cascade throughout a system 

Instability, despite the connotation is not necessarily good or bad 

Instability Measurement 

Instability is determined by 2 forms of coupling, afferent \(incoming\) and efferent \(outgoing\) 

For module X 

Afferent coupling \(AC\) counts other modules that depend on X 

Efferent coupling \(EC\) counts other modules that X depends on 

Instability is the proportion of EC in the total sum of coupling 

1 = EC 

AC + EC 

Instability Example 

Client 

![Shape](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABEAAAAXCAYAAADtNKTnAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAADBSURBVDhPYyAEXIoOL3ctOpIA5ZIHnIsO33cpPFwA5ZIHXIqOvKfYJUBD/lPFEOfiww5QLunAPf+4AtUMcc0/YgAVIg44Fx7yAEWrc+HhBueiI/1glwBpkDjIRfYl+yWgSnED+/r9HECN70GaseD3RBkCAjAXYGBS0gvINnQDQIkO5EqoEuKAS+GR9ciGOBUdCoBKEQ9AgQg3pPDIfqgw6QBo+3mQISRHMTIAJXfngqPzoVzyACggiY7SUTB8AQMDAFkjh2mmrmgPAAAAAElFTkSuQmCC)

![Shape](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJUAAAAbCAYAAAB1GM3nAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAImSURBVGhD7ZohTMNAFIYrkUgkEonEjXQbIJFIJG5th8CBQyKRSCRyskl7yyQSiZycRI73v16X9VZ63bJAyP4veWGh16e+vL+9XhBG2UcvMfNKRWbai00q9daN84delN91h/kpqnOf7gWEtKEzSPdVnDi7gEgqUyFWKqLNXPHCJHvHtW6SPWNtPzHXuL8/MMe2JSF+zpLxkYoDgSCeCAWxwsRMXOlk2n2VUpaSioiXOu1u0wPbkhA/Ou2kNDIx7ZL8tZho+acrnv6vEG8lZm07QvxgSqk4dTGL6eaIp1NQpazGLKambUmIHzyXQZzVmJXnOEe6uphVYeV+PCfaloT40WkntYhZidBiojXErERxsTaPyvttO0L8lDGrLwciUjg0j+VEa45Z84T1jFmyEWXMimQ3GptNMYttFZ12ZqRrtRizZE2w0QtpCvGqMSsiTh3p5rqRrOJVY1b+ntiWhPg5H0wOIU5tzDrSadlrZcyGcXaF+9HHtiTEz0rMRuMXiNU6ZuVe1G98IkOk25/kP7Mcs6VIkErlaohZyKlrISuk3ULMSn98khvxq8cOsIhZxKWI1DZmsU7Xt4hZvHAs9ZjhDdheIrsKJpVOLDdmW5xEQUEidx22WritQn5kcRIFZUUScYqYrTmJsijs68nbr21DSHsw4WqlQulU49YIWRN9TlsSSWNTJhS3O8jG6DEledbClwUetiRbgSIRQgghhBBCCCHkzwiCb3lFrp3NYWk3AAAAAElFTkSuQmCC)![Shape](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEMAAAAbCAYAAAAnFzLpAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAFmSURBVFhH7ZghU8NAEEYjkUgkEonEpZO7gkUikbhcDgQO/gESWYlERmYmd51KZCUSWVlZ9ls2TBhicEx3v5mbadM1ebP7eneFj3lDa1fF/s016XFe59NCa8qH7qBq+isXlosBjIvp3cX85G7TTMp0BgAYBAEBGAACKOqcS4CTMn3ByGB0MEIMJuStb/LrPObrsu4OpUxfLurVsW9SIBiddMyOP9Mz/CZl+oKuQHf4mF64WwjMIODzuDyRMn1hAZNPWMAhfwCMCVjyS8AEyARMwcj4kO5/CJhGywQMAYd8Q1BaBoMFAdMzE7AJeDos4Ng/wy8AYwKW0L7lDCCq0K95lEYClpLJsLipTr7uX/4iYO4sdNU+AxlS3nVHkC2OAwzma7V4BgGPzlI6gAxBV+CkzQKWk/bEalXuawSKAUG+ZTu99ADhzdzo5auYV/AKXz3g0krT3zPfudALq9+sWSwWi8Xy31IUn99lVpj+9IOdAAAAAElFTkSuQmCC)&lt;&lt; façade bar &gt;&gt; 

![Shape](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABcAAAAXCAYAAADgKtSgAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAEHSURBVEhL7ZQhc8JAEIUjkZXIyspKXJjcpSD7EypxuWwQda1DViKR/QmVmckdg0QikUhkJey72RONTBfHN7Pm5WZ3b/ddMuvCr6m7eXYLLPlvS+H8QtsnkfTIP9pRQWFnyB/zqn0QWY982Y6R3NahRTGR9cBYMB7jthuRdMFiucDFOv8uki629g4FCupeRdLFULeGRcsqPIsUUVk4lsrd/0QH8bKhcbEF32YfD/wXdFm47oCE8SbYBYeaXTGWlDSFyi5m1e4RXfeTGwpfcmQYyfP9xAi8Zjk2HLbkRP47fwuwi9ReMdxSNGHFSU+pgGn8VD7rgG5LCm/RPbX/FFmf5P07d7TIsitEq6UYHb7ZaAAAAABJRU5ErkJggg==)

Complex 1complex2complex3complex4complex5 

5/ 1+5 = 5/6 – High Instability 

&lt;&lt; façade bar &gt;&gt; - measure of instability 

Example 2  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)Complex 1complex2complex3complex4 

Service 

0/4+0 = 0 – Low instability \(High abstractness\) 

Example 3 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)  Service 1Service 2Service 3 

Schedule Service 

ClassRankingInstructors 

Similar amounts of EC and AC 

Coupling can be measured quantitatively 

* High coupling can lead to a domino effect when change occurs 
* Measuring coupling can help identify problems classes and design 
* Instability is not necessarily good or bad 
* Perfect instability or abstractness is neither possible nor advisable 

[http://www.arisa.se/compendium/node109.html\#metric:CF](http://www.arisa.se/compendium/node109.html#metric:CF) 

Coupling Factor \(![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) \) 

Works with all instances of a common meta-model, regardless if they where produced with the Java or the UML front-end. The respective call, create, field access, and type reference relations \(Java\) or association, message and type reference relations \(UML\) express the coupling \(exclusive inheritance\) between two classes. They are mapped to relations of type Invokes, Accesses, and \`\`Is Of Type", respectively, in the common meta model and further to type coupling in the view. By defining a view containing only classes and packages as elements, the metric definition can ignore methods and fields as part of its description, since the relations originating from them are lifted to the class element. 

Description 

Coupling Factor \(CF\) measures the coupling between classes excluding coupling due to inheritance. It is the ratio between the number of actually coupled pairs of classes in a scope \(e.g., package\) and the possible number of coupled pairs of classes. CF is primarily applicable to object-oriented systems. 

Scope 

Package 

View 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

* Grammar ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) 
* Productions ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) 
* Relations ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)[3.1](http://www.arisa.se/compendium/footnode.html%22%20/l%20%22foot3658) 
* Mapping ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif): 

| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| :--- | :--- | :--- | :--- |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |

* \[Text Wrapping Break\] 

Definition 

The ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)value of a package ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)is defined: 

| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| :--- | :--- | :--- | :--- |
|  |  | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
|  |  | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
|  |  | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |

\[Text Wrapping Break\] 

Scale 

Absolute. 

Domain 

Integers in ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif). 

Highly Related Software Quality Properties 

Re-Usability [2.4](http://www.arisa.se/compendium/node38.html#property:UsabilityR) 

is negatively influenced by coupling. 

Understandability for Reuse [2.4.1](http://www.arisa.se/compendium/node39.html#property:UnderstandabilityR): 

A art of a system that has a high \(outgoing\) efferent coupling may be highly inversely related to understandability, since it uses other parts of the system which need to be understood as well. 

Understandability decreases with increasing CF. 

Attractiveness [2.4.4](http://www.arisa.se/compendium/node48.html#property:AttractivenessR): 

Parts that have a high \(outgoing\) efferent coupling may be highly inversely related to attractiveness, since they are using other parts of the system which need to be understood as well, and represent dependencies. 

Attractiveness decreases with increasing CF. 

Maintainability [2.6](http://www.arisa.se/compendium/node60.html#property:Maintainability) 

decreases with increasing CF. 

Analyzability [2.6.1](http://www.arisa.se/compendium/node61.html#property:Analyzability): 

Parts that have a high \(outgoing\) efferent coupling may be highly inversely related to analyzability, since they are using other parts of the system which need to be analyzed as well. 

Analyzability decreases with increasing CF. 

Changeability [2.6.2](http://www.arisa.se/compendium/node64.html#property:Changeability): 

Parts that have a high \(outgoing\) efferent coupling may be inversely related to changeability, since they are using other parts of the system which might need to be changed as well. 

Changeability decreases with increasing CF. 

Stability [2.6.3](http://www.arisa.se/compendium/node67.html#property:Stability): 

Parts showing a high \(outgoing\) efferent coupling may be inversely related to stability, since they are using other parts of the system, which are can affect them. 

Stability decreases with increasing CF. 

Testability [2.6.4](http://www.arisa.se/compendium/node70.html#property:Testability): 

Parts that have a high \(outgoing\) efferent coupling may be highly inversely related to testability, since they are using other parts of the system which increase the number of possible test paths. 

Testability decreases with increasing CF. 

Portability [2.7](http://www.arisa.se/compendium/node74.html#property:Portability) 

decreases with increasing CF. 

Adaptability [2.7.1](http://www.arisa.se/compendium/node75.html#property:Adaptability): 

Parts that have a high \(outgoing\) efferent coupling may be inversely related to adaptability, since they are using other parts of the system which might need to be adapted as well. 

Adaptability decreases with increasing CF. 

Related Software Quality Properties 

Functionality [2.1](http://www.arisa.se/compendium/node7.html#property:Functionality) 

is both negatively and positively influenced by coupling. 

Interoperability [2.1.3](http://www.arisa.se/compendium/node14.html#property:Interoperability): 

Parts that have a high \(outgoing\) efferent coupling may be directly related to interoperability, since they are using/interacting with other parts of the system. 

Interoperability might increase with increasing CF. 

Security [2.1.4](http://www.arisa.se/compendium/node17.html#property:Security): 

Parts that have a high \(outgoing\) efferent coupling may be inversely related to security, since they can be affected by security problems in other parts of the system. 

Security might decrease with increasing CF. 

Reliability [2.2](http://www.arisa.se/compendium/node21.html#property:Reliability) 

might decrease with increasing CF. 

Fault-tolerance [2.2.2](http://www.arisa.se/compendium/node25.html#property:Fault-tolerance): 

Parts that have a high \(outgoing\) efferent coupling may be inversely related to fault-tolerance, since they can be affected by faults in other parts of the system. 

Fault-Tolerance might decrease with increasing CF. 

Recoverability [2.2.3](http://www.arisa.se/compendium/node28.html#property:Recoverability): 

Parts that have a high \(outgoing\) efferent coupling may be inversely related to recoverability, since their data is distributed in other parts of the system making their recovery difficult. 

Recoverability might decrease with increasing CF. 

Re-Usability [2.4](http://www.arisa.se/compendium/node38.html#property:UsabilityR) 

might decrease with increasing CF. 

Learnability for Reuse [2.4.2](http://www.arisa.se/compendium/node42.html#property:LearnabilityR): 

Parts that have a high \(outgoing\) efferent coupling may be inversely related to learnability, since they are using other parts of the system which need to be understood as well. 

Learnability might decrease with increasing CF. 

Operability for Reuse - Programmability [2.4.3](http://www.arisa.se/compendium/node45.html#property:OperabilityR): 

Parts that have a high \(outgoing\) efferent coupling may be inversely related to learnability, since they are using other parts of the system, which represent dependencies. 

Programmability might decrease with increasing CF. 

Efficiency [2.5](http://www.arisa.se/compendium/node52.html#property:Efficiency) 

might decrease with increasing CF. 

Time Behavior [2.5.1](http://www.arisa.se/compendium/node53.html#property:Time): 

Parts that have a high \(outgoing\) efferent coupling may be inversely related to time behavior, since they are using other parts of the system, thus execution during test or operation does not stay local, but might involve huge parts of the system. 

Time behavior might get worse with increasing CF. 

Resource Utilization [2.5.2](http://www.arisa.se/compendium/node56.html#property:Resource): 

Parts that have a high \(outgoing\) efferent coupling may be inversely related to resource utilization, since they are using other parts of the system, thus execution during test or operation does not stay local, but might involve huge parts of the system. 

Resource utilization might get worse with increasing CF. 

References 

* CF is discussed in \[[8](http://www.arisa.se/compendium/node123.html#metrics:mood),[2](http://www.arisa.se/compendium/node123.html#famoos-handbook),[17](http://www.arisa.se/compendium/node123.html#validation:mayerhall99),[9](http://www.arisa.se/compendium/node123.html#validation:harrison98)\], 
* it is implemented in the VizzAnalyzer Metrics Suite. 

Since 

Compendium 1.0 

Measuring Cohesion 

Cohesion – measure of the interdependence of data and responsibilities within a class 

Lack of Cohesion of Methods \(LCOM\) 

A metric to help identify problem classes 

Several variants exist \(LCOM1, LCOM2, LCOM96a, etc\) 

LCOM4 \(Hitz & Montazeri\) is relatively simple yet useful 

LCOM4 Measurement 

This is a simple measure of the number of connected components 

Having 1 connected component of one is considered high cohesion 

Methods are ‘connected’ if 

* they both access the same class level variable, or 
* one method calls the other 

Cohesion can be measured quantitatively 

Low cohesion can indicate poor quality and design 

LCOM4 is a simple way of measuring the cohesion of classes 

LCOM4 is not the only measurement approach 

Cohesion is only one measure to be considered in context 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

[https://www.aivosto.com/project/help/pm-oo-cohesion.html\#LCOM4](https://www.aivosto.com/project/help/pm-oo-cohesion.html#LCOM4) 

Cohesion metrics 

[Project Metrics](https://www.aivosto.com/project/help/pm-index.html) 

Cohesion metrics measure how well the methods of a class are related to each other. A cohesive class performs one function. A non-cohesive class performs two or more unrelated functions. A non-cohesive class may need to be restructured into two or more smaller classes. 

The assumption behind the following cohesion metrics is that methods are related if they work on the same class-level variables. Methods are unrelated if they work on different variables altogether. In a cohesive class, methods work with the same set of variables. In a non-cohesive class, there are some methods that work on different data. 

See also [Object-oriented metrics](https://www.aivosto.com/project/help/pm-oo.html) 

The idea of the cohesive class 

A cohesive class performs one function. Lack of cohesion means that a class performs more than one function. This is not desirable. If a class performs several unrelated functions, it should be split up. 

* High cohesion is desirable since it promotes encapsulation. As a drawback, a highly cohesive class has high coupling between the methods of the class, which in turn indicates high testing effort for that class. 
* Low cohesion indicates inappropriate design and high complexity. It has also been found to indicate a high likelihood of errors. The class should probably be split into two or more smaller classes. 

Project Analyzer supports several ways to analyze cohesion: 

* [LCOM metrics](https://www.aivosto.com/project/help/pm-oo-cohesion.html#LCOM4) Lack of Cohesion of Methods. This group of metrics aims to detect problem classes. A high LCOM value means low cohesion. 
* [TCC and LCC metrics](https://www.aivosto.com/project/help/pm-oo-cohesion.html#TCC_LCC): Tight and Loose Class Cohesion. This group of metrics aims to tell the difference of good and bad cohesion. With these metrics, large values are good and low values are bad. 
* [Cohesion diagrams](https://www.aivosto.com/project/help/enterprise-diagrams.html#cohesion) visualize class cohesion. 
* [Non-cohesive classes report](https://www.aivosto.com/project/help/reports-xref.html#noncohesive) suggests which classes should be split and how. 

LCOM Lack of Cohesion of Methods 

There are several LCOM ‘lack of cohesion of methods’ metrics. Project Analyzer provides 4 variants: LCOM1, LCOM2, LCOM3 and LCOM4. We recommend the use of LCOM4 for Visual Basic systems. The other variants may be of scientific interest. 

LCOM4 \(Hitz & Montazeri\) recommended metric 

LCOM4 is the lack of cohesion metric we recommend for Visual Basic programs. LCOM4 measures the number of "connected components" in a class. A connected component is a set of related methods \(and class-level variables\). There should be only one such a component in each class. If there are 2 or more components, the class should be split into so many smaller classes. 

Which methods are related? Methods a and b are related if: 

1. they both access the same class-level variable, or 
2. a calls b, or b calls a. 

After determining the related methods, we draw a graph linking the related methods to each other. LCOM4 equals the number of connected groups of methods. 

* LCOM4=1 indicates a cohesive class, which is the "good" class. 
* LCOM4&gt;=2 indicates a problem. The class should be split into so many smaller classes. 
* LCOM4=0 happens when there are no methods in a class. This is also a "bad" class. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

The example on the left shows a class consisting of methods A through E and variables x and y. A calls B and B accesses x. Both C and D access y. D calls E, but E doesn't access any variables. This class consists of 2 unrelated components \(LCOM4=2\). You could split it as {A, B, x} and {C, D, E, y}. 

In the example on the right, we made C access x to increase cohesion. Now the class consists of a single component \(LCOM4=1\). It is a cohesive class. 

It is to be noted that UserControls as well as VB.NET forms and web pages frequently report high LCOM4 values. Even if the value exceeds 1, it does not often make sense to split the control, form or web page as it would affect the user interface of your program. — The explanation with UserControls is that they store information in the the underlying UserControl object. The explanation with VB.NET is the form designer generated code that you cannot modify. 

Implementation details for LCOM4. We use the same definition for a method as with the WMC metric. This means that property accessors are considered regular methods, but inherited methods are not taken into account. Both Shared and non-Shared variables and methods are considered. — We ignore empty procedures, though. Empty procedures tend to increase LCOM4 as they do not access any variables or other procedures. A cohesive class with empty procedures would have a high LCOM4. Sometimes empty procedures are required \(for classic VB implements, for example\). This is why we simply drop empty procedures from LCOM4. — We also ignore constructors and destructors \(Sub New, Finalize, Class\_Initialize, Class\_Terminate\). Constructors and destructors frequently set and clear all variables in the class, making all methods connected through these variables, which increases cohesion artificially. 

Suggested use. Use the [Non-cohesive classes report](https://www.aivosto.com/project/help/reports-xref.html#noncohesive) and [Cohesion diagrams](https://www.aivosto.com/project/help/enterprise-diagrams.html#cohesion) to determine how the classes could be split. It is good to remove dead code before searching for uncohesive classes. Dead procedures can increase LCOM4 as the dead parts can be disconnected from the other parts of the class. 

Readings for LCOM4 

* Hitz M., Montazeri B.: [Measuring Coupling and Cohesion In Object-Oriented Systems](http://www.isys.uni-klu.ac.at/PDF/1995-0043-MHBM.pdf). Proc. Int. Symposium on Applied Corporate Computing, Oct. 25-27, Monterrey, Mexico, 75-76, 197, 78-84. \(Includes the definition of LCOM4 named as "Improving LCOM".\) 

LCOM1, LCOM2 and LCOM3 — less suitable for VB 

LCOM1, LCOM2 and LCOM3 are not as suitable for Visual Basic projects as LCOM4. They are less accurate especially as they don't consider the impact of property accessors and procedure calls, which are both frequently used to access the values of variables in a cohesive way. They may be more appropriate to other object-oriented languages such as C++. We provide these metrics for the sake of completeness. You can use them as complementary metrics in addition to LCOM4. 

LCOM1 Chidamber & Kemerer 

LCOM1 was introduced in the [Chidamber & Kemerer metrics suite](https://www.aivosto.com/project/help/pm-oo-ck.html). It’s also called LCOM or LOCOM, and it’s calculated as follows: 

Take each pair of methods in the class. If they access disjoint sets of instance variables, increase P by one. If they share at least one variable access, increase Q by one. 

LCOM1 = P - Q , if P &gt; QLCOM1 = 0 otherwise 

LCOM1 = 0 indicates a cohesive class. 

LCOM1 &gt; 0 indicates that the class needs or can be split into two or more classes, since its variables belong in disjoint sets. 

Classes with a high LCOM1 have been found to be fault-prone. 

A high LCOM1 value indicates disparateness in the functionality provided by the class. This metric can be used to identify classes that are attempting to achieve many different objectives, and consequently are likely to behave in less predictable ways than classes that have lower LCOM1 values. Such classes could be more error prone and more difficult to test and could possibly be disaggregated into two or more classes that are more well defined in their behavior. The LCOM1 metric can be used by senior designers and project managers as a relatively simple way to track whether the cohesion principle is adhered to in the design of an application and advise changes. 

LCOM1 critique 

LCOM1 has received its deal of critique. It has been shown to have a number of drawbacks, so it should be used with caution. 

First, LCOM1 gives a value of zero for very different classes. To overcome that problem, new metrics, LCOM2 and LCOM3, have been suggested \(see below\). 

Second, Gupta suggests that LCOM1 is not a valid way to measure cohesiveness of a class. That’s because its definition is based on method-data interaction, which may not be a correct way to define cohesiveness in the object-oriented world. Moreover, very different classes may have an equal LCOM1. 

Third, as LCOM1 is defined on variable access, it's not well suited for classes that internally access their data via properties. A class that gets/sets its own internal data via its own properties, and not via direct variable read/write, may show a high LCOM1. This is not an indication of a problematic class. LCOM1 is not suitable for measuring such classes. 

Implementation details. The definition of LCOM1 deals with instance variables but all methods of a class. Class variables \(Shared variables in VB.NET\) are not taken into account. On the contrary, all the methods are taken into account, whether Shared or not. 

Project Analyzer assumes that a procedure in a class is a method if it can have code in it. Thus, Subs, Functions and each of Property Get/Set/Let are methods, whereas a DLL declare or Event declaration are not methods. What is more, empty procedure definitions, such as abstract MustOverride procedures in VB.NET, are not methods. 

Readings for LCOM1 

* Shyam R. Chidamber, Chris F. Kemerer: [A Metrics suite for Object Oriented design](http://www.eso.org/~tcsmgr/oowg-forum/TechMeetings/Articles/OOMetrics.pdf). M.I.T. Sloan School of Management E53-315. 1993. 
* Victor Basili, Lionel Briand and Walcélio Melo: [A Validation of Object-Oriented Design Metrics as Quality Indicators](https://pdfs.semanticscholar.org/2bb8/c1f4eeb5e5ae353adeea0fd6933551b9e932.pdf). IEEE Transactions on Software Engineering. Vol. 22, No. 10, October 1996. 
* Bindu S. Gupta: A Critique of Cohesion Measures in the Object-Oriented Paradigm. Master of Science Thesis. Michigan Technological University, Department of Computer Science. 1997. 

LCOM2 and LCOM3 \(Henderson-Sellers, Constantine & Graham\) 

To overcome the problems of LCOM1, two additional metrics have been proposed: LCOM2 and LCOM3.  

A low value of LCOM2 or LCOM3 indicates high cohesion and a well-designed class. It is likely that the system has good class subdivision implying simplicity and high reusability. A cohesive class will tend to provide a high degree of encapsulation. A higher value of LCOM2 or LCOM3 indicates decreased encapsulation and increased complexity, thereby increasing the likelihood of errors. 

Which one to choose, LCOM2 or LCOM3? This is a matter of taste. LCOM2 and LCOM3 are similar measures with different formulae. LCOM3 varies in the range \[0,1\] while LCOM2 is in the range \[0,2\]. LCOM2&gt;=1 indicates a very problematic class. LCOM3 has no single threshold value. 

It is a good idea to remove any dead variables before interpreting the values of LCOM2 or LCOM3. Dead variables can lead to high values of LCOM2 and LCOM3, thus leading to wrong interpretations of what should be done. 

| Definitions used for LCOM2 and LCOM3  |  |
| :--- | :--- |
| m  | number of procedures \(methods\) in class  |
| a  | number of variables \(attributes\) in class  |
| mA  | number of methods that access a variable \(attribute\)  |
| sum\(mA\)  | sum of mA over attributes of a class  |

Implementation details. m is equal to WMC. a contains all variables whether Shared or not. All accesses to a variable are counted. 

LCOM2 

LCOM2 = 1 - sum\(mA\)/\(m\*a\) 

LCOM2 equals the percentage of methods that do not access a specific attribute averaged over all attributes in the class. If the number of methods or attributes is zero, LCOM2 is undefined and displayed as zero. 

LCOM3 alias LCOM\* 

LCOM3 = \(m - sum\(mA\)/a\) / \(m-1\) 

LCOM3 varies between 0 and 2. Values 1..2 are considered alarming. 

In a normal class whose methods access the class's own variables, LCOM3 varies between 0 \(high cohesion\) and 1 \(no cohesion\). When LCOM3=0, each method accesses all variables. This indicates the highest possible cohesion. LCOM3=1 indicates extreme lack of cohesion. In this case, the class should be split. 

When there are variables that are not accessed by any of the class's methods, 1 &lt; LCOM3 &lt;= 2. This happens if the variables are dead or they are only accessed outside the class. Both cases represent a design flaw. The class is a candidate for rewriting as a module. Alternatively, the class variables should be encapsulated with accessor methods or properties. There may also be some dead variables to remove. 

If there are no more than one method in a class, LCOM3 is undefined. If there are no variables in a class, LCOM3 is undefined. An undefined LCOM3 is displayed as zero. 

Readings for LCOM2/LCOM3 

* Henderson-Sellers, B, L, Constantine and I, Graham: Coupling and Cohesion \(Towards a Valid Metrics Suite for Object-Oriented Analysis and Design\). Object-Oriented Systems, 3\(3\), pp143-158, 1996. 
* Henderson-Sellers, 1996, Object-Oriented Metrics: Measures of Complexity, Prentice Hall. 
* Roger Whitney: Course material. CS 696: Advanced OO. [Doc 6, Metrics](http://www.eli.sdsu.edu/courses/spring97/cs696/notes/metrics/metrics.html). Spring Semester, 1997. San Diego State University.  

TCC and LCC — Tight and Loose Class Cohesion 

The metrics TCC \(Tight Class Cohesion\) and LCC \(Loose Class Cohesion\) provide another way to measure the cohesion of a class. The TCC and LCC metrics are closely related to the idea of LCOM4, even though are are some differences. The higher TCC and LCC, the more cohesive and thus better the class. 

For TCC and LCC we only consider visible methods \(whereas the LCOMx metrics considered all methods\). A method is visible unless it is Private. A method is visible also if it implements an interface or handles an event. In other respects, we use the same definition for a method as for LCOM4. 

Which methods are related? Methods a and b are related if: 

1. They both access the same class-level variable, or 
2. The call trees starting at a and b access the same class-level variable.   For the call trees we consider all procedures inside the class, including Private procedures. If a call goes outside the class, we stop following that call branch. 

When 2 methods are related this way, we call them directly connected. 

When 2 methods are not directly connected, but they are connected via other methods, we call them indirectly connected. Example: A - B - C are direct connections. A is indirectly connected to C \(via B\). 

TCC and LCC definitions 

NP = maximum number of possible connections= N \* \(N-1\) / 2 where N is the number of methods 

NDC = number of direct connections \(number of edges in the connection graph\)NID = number of indirect connections 

Tight class cohesion TCC = NDC/NPLoose class cohesion LCC = \(NDC+NIC\)/NP 

TCC is in the range 0..1.   
LCC is in the range 0..1. TCC&lt;=LCC.   
The higher TCC and LCC, the more cohesive the class is. 

What are good or bad values? According to the authors, TCC&lt;0.5 and LCC&lt;0.5 are considered non-cohesive classes. LCC=0.8 is considered "quite cohesive". TCC=LCC=1 is a maximally cohesive class: all methods are connected. 

As the authors Bieman & Kang stated: If a class is designed in ad hoc manner and unrelated components are included in the class, the class represents more than one concept and does not model an entity. A class designed so that it is a model of more than one entity will have more than one group of connections in the class. The cohesion value of such a class is likely to be less than 0.5. 

LCC tells the overall connectedness. It depends on the number of methods and how they group together. 

* When LCC=1, all the methods in the class are connected, either directly or indirectly. This is the cohesive case. 
* When LCC&lt;1, there are 2 or more unconnected method groups. The class is not cohesive. You may want to review these classes to see why it is so. Methods can be unconnected because they access no class-level variables or because they access totally different variables. 
* When LCC=0, all methods are totally unconnected. This is the non-cohesive case. 

TCC tells the "connection density", so to speak \(while LCC is only affected by whether the methods are connected at all\). 

* TCC=LCC=1 is the maximally cohesive class where all methods are directly connected to each other. 
* When TCC=LCC&lt;1, all existing connections are direct \(even though not all methods are connected\). 
* When TCC&lt;LCC, the "connection density" is lower than what it could be in theory. Not all methods are directly connected with each other. For example, A & B are connected through variable x and B & C through variable y. A and C do not share a variable, but they are indirectly connected via B. 
* When TCC=0 \(and LCC=0\), the class is totally non-cohesive and all the methods are totally unconnected. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

This example \(left\) shows the same class as above. The connections considered are marked with thick violet lines. A and B are connected via variable x. C and D are connected via variable y. E is not connected because its call tree doesn't access any variables. There are 2 direct \("tight"\) connections. There are no additional indirect connections this time. 

On the right, we made C access x to increase cohesion. Now {A, B, C} are directly connected via x. C and D are still connected via y and E stays unconnected. There are 4 direct connections, thus TCC=4/10. The indirect connections are A–D and B–D. Thus, LCC=\(4+2\)/10=6/10. 

TCC/LCC readings 

* Bieman, James M. & Kang, Byung-Kyoo: [Cohesion and reuse in an object-oriented system](http://doi.acm.org/10.1145/211782.211856). Proceedings of the 1995 Symposium on Software. Pages: 259 - 262. ISSN:0163-5948. ACM Press, New York, NY, USA. \(The original definition of TCC and LCC.\) 

Differences between LCOM4 and TCC/LCC 

* High LCOM4 means non-cohesive class. LCOM4=1 is best. Higher values are non-cohesive. 
* High TCC and LCC means cohesive class. TCC=LCC=1 is best. Lower values are less cohesive. 
* Auxiliary methods \(leaf methods that don't access variables\) are treated differently. LCOM4 accepts them as cohesive methods. TCC and LCC consider them non-cohesive. See method E in the examples above. 

Validity of cohesion 

Is data cohesion the right kind of cohesion? Should the data and the methods in a class be related? If your answer is yes, these cohesion measures are the right choice for you. If, on the other hand, you don't care about that, you don't need these metrics. 

There are several ways to design good classes with low cohesion. Here are some examples: 

* A class groups related methods, not data. If you use classes as a way to group auxiliary procedures that don't work on class-level data, the cohesion is low. This is a viable, cohesive way to code, but not cohesive in the "connected via data" sense. 
* A class groups related methods operating on different data. The methods perform related functionalities, but the cohesion is low as they are not connected via data. 
* A class provides stateless methods in addition to methods operating on data. The stateless methods are not connected to the data methods and cohesion is low. 
* A class provides no data storage. It is a stateless class with minimal cohesion. Such a class could well be written as a standard module, but if you prefer classes instead of modules, the low cohesion is not a problem, but a choice. 
* A class provides storage only. If you use a class as a place to store and retrieve related data, but the class doesn't act on the data, its cohesion can be low. Consider a class that encapsulates 3 variables and provides 3 properties to access each of these 3 variables. Such a class displays low cohesion, even though it is well designed. The class could well be split into 3 small classes, yet this may not make any sense. 

Additional Measure of Quality 

Defect Density 

Cyclomatic Complexity 

Cognitive Complexity 

Maintainability Rating 

Coupling Factor 

Lack of Documentation 

Defect Density 

* One of many post mortem quality metrics 
* Defect count found divided by number of lines of code 
* Quick check of quality between classes 

Cyclomatic Complexity 

* Complexity determined by the number of paths in a method 
* All functions start with 1 
* Add one for each control flow split \(if/while/for… etc\) 

Cognitive Complexity 

* An extension of cyclomatic complexity 
* Attempts to incorporate an intuitive sense of complexity 
* Favours measuring complex structure over method count 

Maintainability Rating 

* Measure of the technical debt against the development time to date 
* Example rating for differing ratios \(used by SonarQube\): 
* A – les that 5% of time already spent on development 
* B – 6%-10%  
* C – 11%-20% 
* D – 21%-50% 
* E – 50% and above 

Coupling Factor 

* The ratio of classes of coupled class and the total number of possible coupled classes 
* 2 classes are couple if one has a dependency on the other 
* The coupling factor \(CF\) or package p is defined as 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Lack of Documentation 

* Simplistic ratio of code which is documented and all code 
* 1 Comment per class and 1 comment per method is expected 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Many additional metrics exist 

* Use additional metrics of quality as appropriate 
* Consider the cost and benefit of developing and tracking metrics 
* Some can be used during development, others only in retrospect 
* Historical trends can be used to inform future process and projects 

[http://www.arisa.se/compendium/node121.html\#metric:LOD](http://www.arisa.se/compendium/node121.html#metric:LOD) 

Lack Of Documentation \(![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) \) 

Works with all instances of a common meta-model, regardless of whether they were produced with the Java or the UML front-end. 

Handle 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Description 

How many comments are lacking in a class, considering one class comment and a comment per method as optimum. Structure and content of the comments are ignored. 

Scope 

Class 

View 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

* Grammar ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) 
* Relations ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) 
* Mapping ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif): 

| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| :--- | :--- | :--- | :--- |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |

* \[Text Wrapping Break\] 

Definition 

The ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)value of a element ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)is defined as: 

| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| :--- | :--- | :--- | :--- |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |
| ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) | ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) |  |

\[Text Wrapping Break\] 

Scale 

Rational. 

Domain 

Rational numbers ![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif). 

Highly Related Software Quality Properties 

Re-Usability [2.4](http://www.arisa.se/compendium/node38.html#property:UsabilityR) 

is inversely influenced by LOD. 

Understandability for Reuse [2.4.1](http://www.arisa.se/compendium/node39.html#property:UnderstandabilityR): 

Understanding if a class is suitable for reuse depends on its degree of documentation. 

Understandability decreases with increasing LOD. 

Learnability for Reuse [2.4.2](http://www.arisa.se/compendium/node42.html#property:LearnabilityR): 

Learning if a class is suitable for reuse depends on the degree of documentation. 

Learnability decreases with increasing LOD. 

Operability for Reuse - Programmability [2.4.3](http://www.arisa.se/compendium/node45.html#property:OperabilityR): 

How well a class can be integrated depends on the degree of documentation. 

Programmability decreases with increasing LOD. 

Maintainability [2.6](http://www.arisa.se/compendium/node60.html#property:Maintainability) 

decreases with increasing LOD. 

Analyzability [2.6.1](http://www.arisa.se/compendium/node61.html#property:Analyzability): 

The effort and time for diagnosis of deficiencies or causes of failures in software entity, or for identification of parts to be modified is directly related to its degree of documentation. 

Analyzability decreases with increasing LOD. 

Changeability [2.6.2](http://www.arisa.se/compendium/node64.html#property:Changeability): 

Changing a class requires prior understanding, which, in turn, is more complicated for undocumented classes. 

Changeability decreases with increasing LOD. 

Testability [2.6.4](http://www.arisa.se/compendium/node70.html#property:Testability): 

Writing test cases for classes and methods requires understanding, which, in turn, is more complicated for undocumented classes. 

Testability decreases with increasing LOD. 

Portability [2.7](http://www.arisa.se/compendium/node74.html#property:Portability) 

decreases with increasing LOD. 

Adaptability [2.7.1](http://www.arisa.se/compendium/node75.html#property:Adaptability): 

As for changeability [2.6.2](http://www.arisa.se/compendium/node64.html#property:Changeability), the degree of documentation of software has a direct impact. Each modification requires understanding which is more complicated for undocumented systems. 

Adaptability decreases with increasing LOD. 

Replaceablity [2.7.4](http://www.arisa.se/compendium/node84.html#property:Replaceablity): 

The substitute of a component must imitate its interface. Undocumented interfaces are difficult to check for substitutability and to actually substitute. 

Replaceablity decline with increasing LOD. 

Related Software Quality Properties 

Reliability [2.2](http://www.arisa.se/compendium/node21.html#property:Reliability) 

decreases with increasing LOD. 

Maturity [2.2.1](http://www.arisa.se/compendium/node22.html#property:Maturity): 

Due to reduced analyzability [2.6.1](http://www.arisa.se/compendium/node61.html#property:Analyzability) and testability [2.6.4](http://www.arisa.se/compendium/node70.html#property:Testability), bugs might be left in undocumented software. Therefore, maturity may be influenced by degree of documentation. 

Maturity decreases with increasing LOD. 

Re-Usability [2.4](http://www.arisa.se/compendium/node38.html#property:UsabilityR) 

is inversely influenced by LOD. 

Attractiveness [2.3.4](http://www.arisa.se/compendium/node36.html#property:Attractiveness): 

Attractiveness of a class depends on its adherence to coding conventions such as degree of documentation. 

Attractiveness decreases with increasing LOD. 

Maintainability [2.6](http://www.arisa.se/compendium/node60.html#property:Maintainability) 

decreases with increasing LOD. 

Stability [2.6.3](http://www.arisa.se/compendium/node67.html#property:Stability): 

Due to reduced analyzability [2.6.1](http://www.arisa.se/compendium/node61.html#property:Analyzability) and testability [2.6.4](http://www.arisa.se/compendium/node70.html#property:Testability), also stability may be influenced negatively by size. 

Stability decreases with increasing LOD. 

Metric Definitions 

[https://docs.sonarqube.org/latest/user-guide/metric-definitions/](https://docs.sonarqube.org/latest/user-guide/metric-definitions/) 

Complexity 

Complexity \(complexity\)   
It is the Cyclomatic Complexity calculated based on the number of paths through the code. Whenever the control flow of a function splits, the complexity counter gets incremented by one. Each function has a minimum complexity of 1. This calculation varies slightly by language because keywords and functionalities do. 

[Language-specific details](https://docs.sonarqube.org/latest/user-guide/metric-definitions/) 

Cognitive Complexity \(cognitive\_complexity\)   
How hard it is to understand the code's control flow. See [the Cognitive Complexity White Paper](https://www.sonarsource.com/resources/white-papers/cognitive-complexity.html) for a complete description of the mathematical model applied to compute this measure. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Duplications 

Duplicated blocks \(duplicated\_blocks\)   
Number of duplicated blocks of lines. 

[Language-specific details](https://docs.sonarqube.org/latest/user-guide/metric-definitions/) 

Duplicated files \(duplicated\_files\)   
Number of files involved in duplications. 

Duplicated lines \(duplicated\_lines\)   
Number of lines involved in duplications. 

Duplicated lines \(%\) \(duplicated\_lines\_density\)   
= duplicated\_lines / lines \* 100 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Issues 

New issues \(new\_violations\)   
Number of issues raised for the first time in the New Code period. 

New xxx issues \(new\_xxx\_violations\)   
Number of issues of the specified severity raised for the first time in the New Code period, where xxx is one of: blocker, critical, major, minor, info. 

Issues \(violations\)   
Total count of issues in all states. 

xxx issues \(xxx\_violations\)   
Total count of issues of the specified severity, where xxx is one of: blocker, critical, major, minor, info. 

False positive issues \(false\_positive\_issues\)   
Total count of issues marked False Positive 

Open issues \(open\_issues\)   
Total count of issues in the Open state. 

Confirmed issues \(confirmed\_issues\)   
Total count of issues in the Confirmed state. 

Reopened issues \(reopened\_issues\)   
Total count of issues in the Reopened state 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Maintainability 

Code Smells \(code\_smells\)   
Total count of Code Smell issues. 

New Code Smells \(new\_code\_smells\)   
Total count of Code Smell issues raised for the first time in the New Code period. 

Maintainability Rating \(sqale\_rating\)   
\(Formerly the SQALE rating.\) Rating given to your project related to the value of your Technical Debt Ratio. The default Maintainability Rating grid is: 

A=0-0.05, B=0.06-0.1, C=0.11-0.20, D=0.21-0.5, E=0.51-1 

The Maintainability Rating scale can be alternately stated by saying that if the outstanding remediation cost is: 

* &lt;=5% of the time that has already gone into the application, the rating is A 
* between 6 to 10% the rating is a B 
* between 11 to 20% the rating is a C 
* between 21 to 50% the rating is a D 
* anything over 50% is an E 

Technical Debt \(sqale\_index\)   
Effort to fix all Code Smells. The measure is stored in minutes in the database. An 8-hour day is assumed when values are shown in days. 

Technical Debt on New Code \(new\_technical\_debt\)   
Effort to fix all Code Smells raised for the first time in the New Code period. 

Technical Debt Ratio \(sqale\_debt\_ratio\)   
Ratio between the cost to develop the software and the cost to fix it. The Technical Debt Ratio formula is:   
Remediation cost / Development cost   
Which can be restated as:   
Remediation cost / \(Cost to develop 1 line of code \* Number of lines of code\)   
The value of the cost to develop a line of code is 0.06 days. 

Technical Debt Ratio on New Code \(new\_sqale\_debt\_ratio\)   
Ratio between the cost to develop the code changed in the New Code period and the cost of the issues linked to it. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Quality Gates 

Quality Gate Status \(alert\_status\)   
State of the Quality Gate associated to your Project. Possible values are : ERROR, OK WARN value has been removed since 7.6. 

Quality Gate Details \(quality\_gate\_details\)   
For all the conditions of your Quality Gate, you know which condition is failing and which is not. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Reliability 

Bugs \(bugs\)   
Number of bug issues. 

New Bugs \(new\_bugs\)   
Number of new bug issues. 

Reliability Rating \(reliability\_rating\)   
A = 0 Bugs   
B = at least 1 Minor Bug   
C = at least 1 Major Bug   
D = at least 1 Critical Bug   
E = at least 1 Blocker Bug  

Reliability remediation effort \(reliability\_remediation\_effort\)   
Effort to fix all bug issues. The measure is stored in minutes in the DB. An 8-hour day is assumed when values are shown in days. 

Reliability remediation effort on new code \(new\_reliability\_remediation\_effort\)   
Same as Reliability remediation effort but on the code changed in the New Code period. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Security 

Vulnerabilities \(vulnerabilities\)   
Number of vulnerability issues. 

Vulnerabilities on new code \(new\_vulnerabilities\)   
Number of new vulnerability issues. 

Security Rating \(security\_rating\)   
A = 0 Vulnerabilities   
B = at least 1 Minor Vulnerability   
C = at least 1 Major Vulnerability   
D = at least 1 Critical Vulnerability   
E = at least 1 Blocker Vulnerability  

Security remediation effort \(security\_remediation\_effort\)   
Effort to fix all vulnerability issues. The measure is stored in minutes in the DB. An 8-hour day is assumed when values are shown in days. 

Security remediation effort on new code \(new\_security\_remediation\_effort\)   
Same as Security remediation effort but on the code changed in the New Code period. 

Security Hotspots \(security\_hotspots\) Number of Security Hotspots 

Security Hotspots on new code \(new\_security\_hotspots\) Number of new Security Hotspots in the New Code Period. 

Security Review Rating \(security\_review\_rating\) 

The Security Review Rating is a letter grade based on the percentage of Reviewed \(Fixed or Safe\) Security Hotspots. 

A = &gt;= 80%   
B = &gt;= 70% and &lt;80%   
C = &gt;= 50% and &lt;70%   
D = &gt;= 30% and &lt;50%   
E = &lt; 30%  

Security Review Rating on new code \(new\_security\_review\_rating\) 

Security Review Rating for the New Code Period. 

Security Hotspots Reviewed \(security\_hotspots\_reviewed\) 

Percentage of Reviewed \(Fixed or Safe\) Security Hotspots. 

Ratio Formula: Number of Reviewed \(Fixed or Safe\) Hotspots x 100 / \(To\_Review Hotspots + Reviewed Hotspots\) 

New Security Hotspots Reviewed 

Percentage of Reviewed Security Hotspots \(Fixed or Safe\) for the New Code Period. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Size 

Classes \(classes\)   
Number of classes \(including nested classes, interfaces, enums and annotations\). 

Comment lines \(comment\_lines\)   
Number of lines containing either comment or commented-out code. 

Non-significant comment lines \(empty comment lines, comment lines containing only special characters, etc.\) do not increase the number of comment lines. 

The following piece of code contains 9 comment lines: 

/\*\*                                    +0 =&gt; empty comment line 

 \*                                     +0 =&gt; empty comment line 

 \* This is my documentation            +1 =&gt; significant comment 

 \* although I don't                    +1 =&gt; significant comment 

 \* have much                           +1 =&gt; significant comment 

 \* to say                              +1 =&gt; significant comment 

 \*                                     +0 =&gt; empty comment line 

 \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*           +0 =&gt; non-significant comment 

 \*                                     +0 =&gt; empty comment line 

 \* blabla...                           +1 =&gt; significant comment 

 \*/                                    +0 =&gt; empty comment line 

/\*\*                                    +0 =&gt; empty comment line 

 \* public String foo\(\) {               +1 =&gt; commented-out code 

 \*   System.out.println\(message\);      +1 =&gt; commented-out code 

 \*   return message;                   +1 =&gt; commented-out code 

 \* }                                   +1 =&gt; commented-out code 

 \*/                                    +0 =&gt; empty comment line 

[Language-specific details](https://docs.sonarqube.org/latest/user-guide/metric-definitions/) 

Comments \(%\) \(comment\_lines\_density\)   
Density of comment lines = Comment lines / \(Lines of code + Comment lines\) \* 100 

With such a formula: 

* 50% means that the number of lines of code equals the number of comment lines  
* 100% means that the file only contains comment lines  

Directories \(directories\)   
Number of directories. 

Files \(files\)   
Number of files. 

Lines \(lines\)   
Number of physical lines \(number of carriage returns\). 

Lines of code \(ncloc\)   
Number of physical lines that contain at least one character which is neither a whitespace nor a tabulation nor part of a comment. 

[Language-specific details](https://docs.sonarqube.org/latest/user-guide/metric-definitions/) 

Lines of code per language \(ncloc\_language\_distribution\)   
Non Commenting Lines of Code Distributed By Language 

Functions \(functions\)   
Number of functions. Depending on the language, a function is either a function or a method or a paragraph. 

[Language-specific details](https://docs.sonarqube.org/latest/user-guide/metric-definitions/) 

Projects \(projects\)   
Number of projects in a Portfolio. 

Statements \(statements\)   
Number of statements. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Tests 

Condition coverage \(branch\_coverage\)   
On each line of code containing some boolean expressions, the condition coverage simply answers the following question: 'Has each boolean expression been evaluated both to true and false?'. This is the density of possible conditions in flow control structures that have been followed during unit tests execution. 

Condition coverage = \(CT + CF\) / \(2\*B\)   
where  

* CT = conditions that have been evaluated to 'true' at least once 
* CF = conditions that have been evaluated to 'false' at least once 
* B = total number of conditions 

Condition coverage on new code \(new\_branch\_coverage\)   
Identical to Condition coverage but restricted to new / updated source code. 

Condition coverage hits \(branch\_coverage\_hits\_data\)   
List of covered conditions. 

Conditions by line \(conditions\_by\_line\)   
Number of conditions by line. 

Covered conditions by line \(covered\_conditions\_by\_line\)   
Number of covered conditions by line. 

Coverage \(coverage\)   
It is a mix of Line coverage and Condition coverage. Its goal is to provide an even more accurate answer to the following question: How much of the source code has been covered by the unit tests? 

Coverage = \(CT + CF + LC\)/\(2\*B + EL\)   
where  

* CT = conditions that have been evaluated to 'true' at least once 
* CF = conditions that have been evaluated to 'false' at least once 
* LC = covered lines = linestocover - uncovered\_lines 
* B = total number of conditions 
* EL = total number of executable lines \(lines\_to\_cover\) 

Coverage on new code \(new\_coverage\)   
Identical to Coverage but restricted to new / updated source code. 

Line coverage \(line\_coverage\)   
On a given line of code, Line coverage simply answers the following question: Has this line of code been executed during the execution of the unit tests?. It is the density of covered lines by unit tests: 

Line coverage = LC / EL   
where 

* LC = covered lines \(lines\_to\_cover - uncovered\_lines\) 
* EL = total number of executable lines \(lines\_to\_cover\) 

Line coverage on new code \(new\_line\_coverage\)   
Identical to Line coverage but restricted to new / updated source code. 

Line coverage hits \(coverage\_line\_hits\_data\)   
List of covered lines. 

Lines to cover \(lines\_to\_cover\)   
Number of lines of code which could be covered by unit tests \(for example, blank lines or full comments lines are not considered as lines to cover\). 

Lines to cover on new code \(new\_lines\_to\_cover\)   
Identical to Lines to cover but restricted to new / updated source code. 

Skipped unit tests \(skipped\_tests\)   
Number of skipped unit tests. 

Uncovered conditions \(uncovered\_conditions\)   
Number of conditions which are not covered by unit tests. 

Uncovered conditions on new code \(new\_uncovered\_conditions\)   
Identical to Uncovered conditions but restricted to new / updated source code. 

Uncovered lines \(uncovered\_lines\)   
Number of lines of code which are not covered by unit tests. 

Uncovered lines on new code \(new\_uncovered\_lines\)   
Identical to Uncovered lines but restricted to new / updated source code. 

Unit tests \(tests\)   
Number of unit tests. 

Unit tests duration \(test\_execution\_time\)   
Time required to execute all the unit tests. 

Unit test errors \(test\_errors\)   
Number of unit tests that have failed. 

Unit test failures \(test\_failures\)   
Number of unit tests that have failed with an unexpected exception. 

Unit test success density \(%\) \(test\_success\_density\)   
Test success density = \(Unit tests - \(Unit test errors + Unit test failures\)\) / Unit tests \* 100 

Introduction to Patterns and the Observer Pattern 

Design Patterns 

Elements of reusable design 

Vocabulary to talk about design 

Just another abstraction, among many, to reason about design 

Observer 

Common barrier to better modulartity – Need to maintain consistent state 

Subject – has changing state 

Observer – needs to know about changes to that state 

Obvious approach – subject informs observers on change 

Problems with the obvious approach 

Obvious approach – subject informs observers on change 

Conceptually, subjects had no knowledge of observers 

Better approach – create a ‘naïve’ dependency 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Patterns – Common solutions to common problems 

* Each pattern adds a tool to your toolbox when you run into issues 
* The observer pattern is a common solution to the pub/sub problem 
* Patterns are not meant to be taken literally or as set in stone 
* Vary the solutions suggested shape to meet the situations needs 

[https://sourcemaking.com/design\_patterns/observer/cpp/1](https://sourcemaking.com/design_patterns/observer/cpp/1) 

Before 

The number and type of "user interface" \(or dependent\) objects is hard-wired in the Subjectclass. The user has no ability to affect this configuration. 

class DivObserver 

{ 

    int m\_div; 

  public: 

    DivObserver\(int div\) 

    { 

        m\_div = div; 

    } 

    void update\(int val\) 

    { 

        cout &lt;&lt; val &lt;&lt; " div " &lt;&lt; m\_div &lt;&lt; " is " &lt;&lt; val / m\_div &lt;&lt; '\n'; 

    } 

}; 

class ModObserver 

{ 

    int m\_mod; 

  public: 

    ModObserver\(int mod\) 

    { 

        m\_mod = mod; 

    } 

    void update\(int val\) 

    { 

        cout &lt;&lt; val &lt;&lt; " mod " &lt;&lt; m\_mod &lt;&lt; " is " &lt;&lt; val % m\_mod &lt;&lt; '\n'; 

    } 

}; 

class Subject 

{ 

    int m\_value; 

    DivObserver m\_div\_obj; 

    ModObserver m\_mod\_obj; 

  public: 

    Subject\(\): m\_div\_obj\(4\), m\_mod\_obj\(3\){} 

    void set\_value\(int value\) 

    { 

        m\_value = value; 

        notify\(\); 

    } 

    void notify\(\) 

    { 

        m\_div\_obj.update\(m\_value\); 

        m\_mod\_obj.update\(m\_value\); 

    } 

}; 

int main\(\) 

{ 

  Subject subj; 

  subj.set\_value\(14\); 

} 

Output 

14 div 4 is 3 

14 mod 3 is 2 

After 

The Subject class is now decoupled from the number and type of Observer objects. The client has asked for two DivObserver delegates \(each configured differently\), and one ModObserver delegate. 

class Observer 

{ 

  public: 

    virtual void update\(int value\) = 0; 

}; 

class Subject 

{ 

    int m\_value; 

    vector m\_views; 

  public: 

    void attach\(Observer \*obs\) 

    { 

        m\_views.push\_back\(obs\); 

    } 

    void set\_val\(int value\) 

    { 

        m\_value = value; 

        notify\(\); 

    } 

    void notify\(\) 

    { 

        for \(int i = 0; i &lt; m\_views.size\(\); ++i\) 

          m\_views\[i\]-&gt;update\(m\_value\); 

    } 

}; 

class DivObserver: public Observer 

{ 

    int m\_div; 

  public: 

    DivObserver\(Subject \*model, int div\) 

    { 

        model-&gt;attach\(this\); 

        m\_div = div; 

    } 

     /\* virtual \*/void update\(int v\) 

    { 

        cout &lt;&lt; v &lt;&lt; " div " &lt;&lt; m\_div &lt;&lt; " is " &lt;&lt; v / m\_div &lt;&lt; '\n'; 

    } 

}; 

class ModObserver: public Observer 

{ 

    int m\_mod; 

  public: 

    ModObserver\(Subject \*model, int mod\) 

    { 

        model-&gt;attach\(this\); 

        m\_mod = mod; 

    } 

     /\* virtual \*/void update\(int v\) 

    { 

        cout &lt;&lt; v &lt;&lt; " mod " &lt;&lt; m\_mod &lt;&lt; " is " &lt;&lt; v % m\_mod &lt;&lt; '\n'; 

    } 

}; 

int main\(\) 

{ 

  Subject subj; 

  DivObserver divObs1\(&subj, 4\); 

  DivObserver divObs2\(&subj, 3\); 

  ModObserver modObs3\(&subj, 3\); 

  subj.set\_val\(14\); 

} 

Output 

14 div 4 is 3 

14 div 3 is 4 

14 mod 3 is 2 

Strategy Pattern 

Strategy 

Define a family of algorithms, encapsulate each one and make the interchangeable 

Gamma, Helm, Johnson, Vlissides – known as the gang of 4 

Definition 

Client 

Context 

Strategy 

ConcreteStrategy 

![](data:image/png;base64,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EEIIk0EUACGEeTNpgivB3Ow/oZ7gfcABB3TvfOc7u4997GPd+9///u6ggw5q9n70ox81AZ6Qzw0oCQj0fsufyy+/vPva177WffGLX2yrB+6+++6WJ4R+wv0ZZ5zRffnLX+6+/vWvd2eddVZ30003tW0EthtYeUDhcN999zXFAHdlQgghhBBCWEiiAAghzJv+8vblDsHa7DvB/Z577uk22WST7tWvfnW3++67dzvttFO7Puqoo7r999+/22abbbqXvexl6wRy7gj/P/nJT7rHH3983dkB/qYosK3gzjvvbAK+mX5C/W233db+5s72Acv9b7/99rZagGJh4403bmHYFlBMUn6GEEIIIYTJIQqAEMKqgyBvBt82gK233rrbZZddmiIAm266aXfggQc2JcAhhxzSvfKVr1wnkHNn5p7igEBPwL/qqquaMoAfVhK4trKA4G/7AKF/o402as8YSoKf//znTQFAwbDffvt1e++9d7fjjjt2m2+++bqwogQIIYQQQggLTRQAIYRVB+HajDthnyGgF565t9lmm7XfEsTZMVNvxt49ygArAMz4O8yPUO+XYP/Tn/503faBV7ziFW1VgW0FhP099tij+eNrAsLYcsstuy222KIpIPqrAEIIIYQQQlhoMtoMIawqCO+EeLPtTH3mrz7D52+CPWHeDL6VAkVtBeBHfcaPIA8CPEF+r732agL/dttt1xQIhH2rCCgC/G673bZN8BdeKRSGWwBCCCGEEEJYDDLiDCHMG0LxJEEAb8L4ttu2g/cI+mbrCfuW+N98881t377D/Nwr4bwOAyT810qBrbbaqvlD4N9hhx3aMv+DDz64Let/+ctfvs5+mQ032LC5LQPKgEnLwxBCCCGEMHlEARBCmDclyE4KlvMT2s3WW8rvFH6n8du7b0//xRdf3Jb2E8oJ/6UA8DclgM/8lR8EfbP7tSLA4YL1ST/32HfNUAZYMUDp4BrCZ59xHUIIIYQQwmIRBUAIYVVi+f8+++zTTv+nwPBJPjP/9957bxPuzebvueee3fbbb9++DuCQP/v1HdxnHz/h371DDz20HSRIsLf/n2BvKwClADvc19cEmFotwHhWWwVsQ6BYoCgIIYQQQghhMYgCIIQwbyZRaDWrbwXAEUcc0QT9hx56qM362wpgGf/RRx/dZvcpCCgK3COsE/6PPPLIJvzvtttu3WGH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IYSwlEQBEMKEourWANI1BcDdd9/dlkvvt99+3atf/er2PFV88ei/AyS/F5bKW2dbUADYcrHbbrt1Rx11VBQAYSLptw/9tiOEEEJYKrJONYQJpT+QdF2z/a6ZEkZrBUDMwhr0f4fXMfM3ym5R5b3KdwghhBBCmD1RAIQQViXzFSIJqH0imIYQxjGqfRjVXqQdCSGEsNhEARDCCqA/YKzrUfdWMtI4NMWoe+jfn8qMo5QA7PRXYIT5k3wMK4VRZXlc+a7VLyGEEMJikTMAQphQCJt12rxr36R3BsDTTz/dzgDYf//91wmmq32/tHxgFnNwLZ+HXwGYTVgVv/Ai9c7kpTMArrvuuvYpwF133bWdAZDPAIZJQlkeor67+8KadkPbwRTak8Vsr0JYLPpltsqx9ro+oRtCWP9EARDChKJjjQJgeioP/MqHxRpQ898Avvz3WybMHvnJRAEQVgLK8hBtgzbjiSeeaGX80UcfXWevBKe0H2HS0GZX2WY23XTTbqedduq23377bosttkiZDmEZEAVACBNKXwGgk+1/BYDwTwmAsrcaO91f/epXbVD94IMPds8++2y3ySabdJtttlm33XbbdVtttVX7ez75Im9/85vftDwnkBrc9PN6Ln4/99xz7bR7fvvW/eabb74qhV1dExMFQJh0xg2ztA/aD8rbW265pXvggQe6LbfcsglM6n8Ik0SV85rpNy558skn298+33rggQd2O+6447pxSwhh/REFQAgTShQA49GsMT/60Y/a5+NuvPHGJjwaWL/yla/sjjnmmO41r3lNUwQQJNmVh5BPlV/lDwO/9RzymnB67733dltvvXXLdwoGyPehfZRfqHdSYXDzi1/8orvzzjubIuBVr3pVt8suuzShYLVReSLvogAIk0zV+WpTUGVbmb7hhhta+aas9PnWbbbZprVHUQKESaP6O0K/Mq5vVK4J/q997Wu7fffdd92KRM+rDwwhLC1RAIQwofQVAK5X+xaA/mCC8Pz444933/3ud9vgmtBvUG0VgNUAhP9DDjmkO+CAA1reELpr+e3LX/7yphgw+84fMxjPPPNMG5CbrTPLzz95L8+///3vd7fddlvz713veldzy/4jjzyybtXBtttu2/zlh9l9v9zzRxgUCRAW4f+ss85q4Z9wwgndscce25ZPrja8C0Y+RQEQVhrVXinTlJTabmX9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)

Example 1 

Logger can be configured for several types of output 

Selecting strategy 

Whose responsibility is it to select the strategy to use? 

When should the context select? When should it not? 

Client or context requests strategy instances from a StrategyFactory, passing properties uninterpreted 

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABAAAAAI0CAYAAACDJlsCAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAFiUAABYlAUlSJPAAAP+lSURBVHhe7N0HtC1Hdef/RhJISEKgnHMOKCGQUCJIJAkDJmMwGBsbexxmPMuzxuNZa8bzX8sTPB4HZpbH4+WIMZhgRFQWyglJKKOIBEogoYQCCiD5/z6lt59aR+fmc+89997f971ap293dVV19a6qvXdVd7/gX1bRhRBCCCGEEEIIYVmz1urfEEIIIYQQQgghLGPiAAghhBBCCCGEEFYAcQCEEEIIc8TTdBVCCCGEEMaVOABCCCGEEEIIIYQVQBwAIYQQwoh4wQtesHorhBBCCGH8yFcAQghjRb9Lmo4xlS4sLCYlo+RQ8HecACGEEEIYV+IACCGMFf0uKYZUWEo8/fTTcQCEEEIIYayJAyCEMNYwqnRTFYYRgyssJn2jPw6AEEIIIYwzcQCEEMaWn/70p92jjz7awhNPPLF67zOrBPpGVgyusFistdZa3TrrrNNtuOGG3frrr9+2a1iNXIYQQghh3IgDIIQwtjz44IPd9ddf391///3dk08+OaHRH0MrLBbkcu211+522WWXbscdd+w22mij1UcilyGEEEIYP+IACCGMLXfeeWd36qmndg8//HC33nrrNUPLjOtMDat0c2FUDMreD3/4w+6xxx7rDjzwwO6ggw7qtt122yajIYQQQgjjSBwAIYSx5a677urOPPPM7iUveUm38847dxtssEH3whe+cPXR6ZNuLowKDoAKsELle9/7XrfVVlt1++23X7f99tvP2EEVQgghhLBQxAEQQhhbfvCDH3Tnnntut80223Qvf/nL23PWMa7COHHjjTd21113XXNO7bXXXs0BEEIIIYQwrmSdYghhLOGbHPRP1vL/hIRxCajfEEIIIYRxJw6AEMJYwvj3CcD6DGD9hjBORCZDCCGEsJSIAyCEMLYMOgFWmrFV1zxVmIjBY4Pn9cNcGUUaIYQQQghhfokDIIQwlgwaqBVWErW0vO8E6S8/rzARg8cGz+uHuSKNlXZ/QgghhBCWGnEAhBDGmpVsVLp235l/5JFHuh/96Efdj3/84+YIQDkECttT1VU5Eoo6Z6rzpsNPf/rT7qmnnlr9VwghhBBCGEfiAAghhDGDQc7Y9xnEK6+8srv88svXhO9+97vdww8/3OL1Z+6nM5Nfs/ScCr5ff/PNN3cPPfRQM9xn6wTwDXzl9MUG5RqFMyGEEEIIIcwPcQCEEMKYYTb9vvvu66699trua1/7WnfGGWd03/jGN7oTTzyxu/TSS7u77757dcyZwQFgBcC9997bPl133nnndffcc8+0Zu4HDXt/CxwJV199dXfDDTe07TgAQgghhBDGlxesUtairYUQxg5GqZnlc845p9tuu+26l7/85d1LX/rSbu21114dY3miS7bc/6yzzuquv/767ic/+Um79pe85CXdnXfe2W288cbd7rvv3u2xxx5txt0+DoEXvvCF3bbbbtvq6vHHH+8efPDB7oEHHmgz/Iz+jTbaqNtqq62ac+Hiiy/uLrnkkpb+hz70oe6QQw7pXvSiF3V33HFHy1t86Ytv26oD5VIG+Uhf2uuss04z/M8+++zuxS9+cXfkkUd2xx13XEtrpaAO1cH666/f7bXXXt3222+/+kgIIYQQwvix9u+vYvV2CCGMDQxOBu73vve9ZrxuueWW3XrrrdettdbyXrjEQDeTbtbftTPEDzvssGb0M7IZmhtssEH7vfHGG9uKAEv5b7/99ra0/2Uve1l3//33d7feemt3xRVXdLfccktzpHAUMMw5FJzzzW9+sx3fb7/9mmFvVcBVV13V3XTTTS0+1DdHjHicAFYlcDbI67bbbmtpMX6VlaNhhx126A488MDmGFgpqDf1wjGy2WabNSdVCCGEEMK4kkcAQghhjPBMvWX5jEoGu1nlTTfdtBnpe+65Z7fvvvs2hwij//zzz+++9a1vNWeAGf/LLrus7asl+RdddFFL64knnujOPffcFpdTZfPNN2/GutlqaXt+37mM+HIyWCXgEQEG7qOPPtpdc8013ec///nu05/+dJvxF1eZtthiixYqreXuoAkhhBBCWMpEUwshhDHCrDqDmyPAM/tm9DkCbPs1K28JPoPckn1/H3TQQW0m33J9DgDL0i3llxbjfMcdd2wrKqRrRp+hbnm/sOGGG655J0C9ENBKAisB7HPO3nvv3Wa3OR28lNBXCTgidt5555a+Y9tss037Xe6PaIQQQgghLGXiAAghhDHCDLrl5Ax+jwNwBPgFI56Bzii3FN/MviXnZvN32mmnNnP//e9/v60GEJdzgLHPSDdbL237Gemc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H3ywzf5zAuywww7drrvu2r4M4IWA999/f1sR0KdevJgw/RBCmD1xAIQQQgghhDADGP4M0bXWWqtt33333d0VV1zRju24447dJpts0j300EPdXXfd1W255Zbd+uuv3x4DuPDCC9t7Ap5++ukWN8ZsCGGhiQMghBBCCCGEGVAz/2Do33zzzd3111/fDHrGPofAeeed15100knthYD2PfDAA22flQJPPPHEc9IIIYSFIg6AEEIIIYQQZkDN3DPivdzvqquuarP9HgVg6F977bXd2Wef3Z122mntCwCe/X/00UfbKgGOAu8L8NWAEEJYaOIACCGEEEIIYQaUA8Bn/cz+e/mfZ/+9ANB3/2+55ZbmCGD0cw6Ic99993V33nlnO84p4FgIISw0cQCEEEIIIYQwQxj/jzzySFsFsPHGG7dn//fbb79ujz32aO8AWG+99bp11lmn23rrrbs999yzHfNywJe85CVt9l+odwGEEMJCEQdACCGEEEIIM4QDwJL/l73sZd0+++zTHXjggd3RRx/dHXHEEc0JwCmwwQYbtP1HHXVUC475KgAnAOIACCEsNC/4l7yBJIQQlj0U1Xvuuae77rrrugsuuKA7+OCDu+OOO2710RBCCDPF5/w4AKwCePjhh9tz/mb97bfc/+KLL27P+r/3ve9tXwJ44sknup/+5KctDgeA8KIXvah9SSCEEBaK9DghhBBCCCHMAPNnDPcXv/jF3RZbbNHtsssubRXA7rvv3u20007dVltt1W222WbtUYBtttmmPR6wx+57dHvvvXe38847t2McATH+QwgLTXqdEEIIIYQQZoCXAAqe8WfE+xVqPwfBsEW2dVwIIYTFIA6AEEIIIYQQZkgZ8ZMZ845NNMvv+f+8AyCEsNDEARBCCCGEEMKI6M/8T/aqrawECCEsBnEAhBBCCCGEMEL6hv9Es/wx/kMIi0EcACGEEEIIIYyYid4DEEIIi0kcACGEEEIIIYyI/sx+nAAhhHEjDoAQQgghhBBCCGEFEAdACCGEEEIIIYSwAogDIIQQQgghhEUgLwIMISw0cQCEEEIIIYQQQggrgDgAQgghhBBCCCGEFUAcACGEEEIIIYQQwgogDoAQQgghhBBCCGEF8IJ/ycdJQwhh2fPUU09199xzT3fdddd1F1xwQXfwwQd3xx133OqjIYyOwe+eT7QdwnLDC/3WWmut7rHHHutuu+227vzzz+/uuuuu7iMf+Ui33XbbdU8//fTqmCEsX+rFln6HveQyL75cfOIACCGEFUAcAGG+oU488sgj3b333tv95Cc/aX+Xomc76kZY7pD3ddZZpzkAfvCDH3SXXnpp+33nO9/ZbbXVVq0fTjsIyx1OMG2hfms8WH/99buNN96422ijjeIEWGTiAAghhBVAHABhVJTaQIGzXYocGbvlllu68847ryl8DKEXvvCFUfTCioLR88QTT3QPPvhgd/311zeH2FFHHdVtuummMf7DikCf3w/awqOPPtptueWW3X777dftv//+bXwYpD+ehPklDoAQQlgBxAEQRkWpDRS1vsL25JNPdt/+9re7U045pdthhx26rbfeOg6AsKIg62uvvXZbAaC/vfrqq5sD4I1vfGO3xRZbrI4VwvKHI0zQHu64447u1u/e2j3x+BPdy1/+8u7YY4/tXvSiF62O+SxxACwccQCEEMIKIA6AMCqGOQD8mvW89tpru1NOPaU79FWHdnvvvXdT8qLQhZUCWef0MtvJ6Lnkkku6u+++u3v3u9/d3gGgnUTtDisBbUHgAPje977XdI9bb72123333bvjjz8+DoBFJg6AEEJYAcQBEEZFqQ0UtVLY/D7++OPNAXD66ad3r3nNa7oDDjigW3fddaPQhRUFebca5s4772yPw/j90Ic+tMYBEMJKofp+L8L0OIwVYlaHveUtb4kDYJHJZwBDCCGEMCf6TgHPdpYS57eWgiYkrIRA5r3t/6c//Wn7rTaQtpCw0gKZF4pqA2HxyV0IIYQQwpyp2ZtS/EJYqVhxVQ6AEFY62oE2MegQCItHHAAhhBBCmDZ9Ja6vzPW3OQOy3DmEZ1fHhBDCuBAHQAghhBBGQmZ3QgghhPEmDoAQQgghhBCWILXaJuHZEEKYnDgAQgghhBBCCCGEFUAcACGEEEIIIYQQwgogDoAQQgghhBBCCGEFEAdACCGEEEIIS5D6KkfCsyGEMDlxAIQQQgghhBBCCCuAOABCCCGEEEIIIcwb+ULD+BAHQAghhBBCCCGEeSVOgPEgDoAQQgghhBBCCPNGjP/xIQ6AEEIIIcyJ/su3nn766fabF3KNlijPS4e11167hcj/0kM7S1sbLdMdC9JeJmeUchkHQAghhBDmBMVtrbXWar9PPfXUmn1hNHCqVJgvYvSMjnXWWad70YtetMYJkLodf8rw18b0Yblno+OFL3xhawtFf2xIPS8OL1hV8an5EEJY5lBo7rnnnu66667rLrjggu7ggw/ujjvuuNVHVzY//elPW/1QSmK0zp4nn3yy+/a3v92ddtpp3Wtf+9pu//3379Zdd901BlDUjZmh3vqzyOpvvmV0vp0Myx33hiPs0Ucf7e66667u3HPP7e68887uwx/+cLfjjjuOpB3M5/0fV6reXHvfkBwVLf1nNtrf1c5Gcb9WKlWHuP3227trrrmmu+GGG7qddtqp6R6cAvoa9avNzIaVdG9KFgX1qs769VZ1PV3iAAghhBVAHADP5yc/+Un32GOPdT/+8Y+bE8Cs3UwH0fAMVAn1edNNN3XnnHNOd/jhh3d77713mwUNs4exQ1FWj5wps1WUp8MTTzzRPf744+03quHs0YdwANzzw3u6S755Sff973+/e9/73tdtt912I3GurMQ+qj8jv95667WgTYyiLird+pWm+2Rc4NSMQ2z69O+H7eqvvve97zXj/7vf/W5zhB177LFtvK37Olunzkrpp1ynUA4TQd2qt/XXX7+1BX/PpD3EARBCCCuAOACezx133NFmJe69995mvG644YZtQM2wOHPUGRn74Q9/2H3nO99pSt7WW2+9xgGQOp056owRQia33XbbtqJi4403Xn10dMiH0a9vuPnmm9s2ZZKCHmZGKeD6E/fOKgDOAM4w/cso2sFMlPzlAnlkjP/oRz9qbWGvvfbqtt9+++YUmyv9e6Juqx+79NJLuwcffHAkeaw01GMFPPDAA03/cP823XTTbvfdd2/7Od7V/0yN12IU7Wkp0V8xoX/hsD3qqKPaeMspZv90iQMghBBWAHEAPJ/rr7++LdEt43+rrbaK0TMHqBOMRwbPi1/84ucoJFE1Zg5l7+67727K80te8pLuDW94QzN+Ro17456df/75rX/YZJNNupe+9KVtZinMnJJ194+B41dbYOCMqh3MxlhaylgFw+C55ZZbWlvgUNlvv/1GIqP9e6JeORpuu+227vTTT2/Hdt111xVX36Og1Vn7/4I2LqhX9aktbLDBBmsevbMvDoDpUddLT7Gqgg5z/PHHd/vuu2/rs2eykiIOgBBCWAHEAfB8PK/OAWBWdYcdduh22WWXNmNNYQ8zg/JWClypFX6F1Ofs0GatUqHkPfLII91b3vKWNtMz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)

Good example of refactoring 

Strategy allows expansion in a family of algorithms 

* Abstract operation out of a client into it’s own hierarchy 
* Strategy separates operation based on circumstances 
* Factory encapsulates complexity of selecting specific ConcreteStrategy 
* Client can be purely ignorant of types and selection criteria 

[https://www.oodesign.com/strategy-pattern.html](https://www.oodesign.com/strategy-pattern.html) 

Strategy 

Motivation 

There are common situations when classes differ only in their behavior. For this cases is a good idea to isolate the algorithms in separate classes in order to have the ability to select different algorithms at runtime.  

Intent 

Define a family of algorithms, encapsulate each one, and make them interchangeable. Strategy lets the algorithm vary independently from clients that use it. 

Implementation 

![Strategy Implementation UML Class Diagram](data:image/gif;base64,R0lGODlh+gH1AHAAACwAAAAA+gH1AIcAAAADAwMEBAQFBQUGBgYHBwcICAcICAgJCQkLCwsMDAsMDAwNDQ0PDw8QEA8QEBAREREWFhYYGBgaGhocHBweHh4gICAiIiIlJSUnJycpKSkrKystLS0vLy8xMTEzMzM2NjY4ODg6Ojo8PDw+Pj5AQEBCQkJERERHR0dISEhJSUlLS0tNTU1PT09QUEdQUFBRUVFTU1NUVEtUVFRVVVVYWE5YWFhaWlpcXFJcXFxdXV1eXl5gYFVgYF1gYGBiYmJkZF1kZGBkZGRmZmZoaGFoaGRpaWlra2tsbGRsbGhtbW1vb29wcGhwcGxxcXFzc3N1dXV3d3d6enp8fHx/f3F+fn6AgICCgoKEhISGhoaIiIiLi4uNjY2Pj4+RkZGTk5OVlZWXl5eZmZmcnJydnZ2enp6goKCioqKjo6OkpKSmpqaoqKiqqqqrq6utra2vr6+xsbGzs7O1tbW3t7e5ubm7u7u+vr7AwMDCwsLExMTGxsbHx8XHx8fIyMjLy7XKysrLy8vMzMzPz8/T07zR0dHT09PX17/V1dXX19fb28Pb28bZ2dnb28nb29jb29vf38rd3d3f39zg4ODj48rj483i4uLj4+Pk5OTn587m5ubn5+fo6Ojq6urs7Ozu7u7x8fHz8/P39/f5+fn7+/v//+P9/f3///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////8I/wBJCRxIsOCdgggTkjqosOFChw0ZQkQocSLBihYFYsy40WLHiR8hhnQ4MmJGgycvphxYUmHLhC8prtQ48+HMmChv1sRJcqdPnUBX8mT5U2jRlENpBkV69GRSm0aXOm3KkapHq1KrZr26FSRWkV97dgU7VmzUs0zLmlTrMuxatFNr5oSrlS5Xu17ZwnTbVq9Mv3PT4iU72Kzgw3ELv5WrVHFfx3sBq5RMlHJjxHUx39WcF/Jfz4ETcyY8uvRi0agzp968urPpx68jg548u3Lty61J5za8+7Tcp8D5yo79mXho1chZJ3fdG3bz4c+LRz+uvDrz38KlL9e9nXd339a5h//3Ph789fLOv6dHD119e/bn44uXT56++fn46+e/r78////r2RfgfgP6VyCA77F0x4IMNujggxBGKOGEFFZo4YUYZqjhhhx26OGHIIYo4ogklmjiiShKOB1txrG4om0twvgibu5pBx91AiZIoI4G8oigjTkCuWOQOA5ZZI9CInnkj0se6KSPTybJpIs1NgnllVJGaWWWN1LZpYxVekmkmEaSqaSZU4L5JY1rQhUjm2OqGSecZaZJ55ly1nmnnW7O2GeYeeK5p5ZoEhoon8FZ9mebT3Hp6JaQFoplpIcaOuikkj6aKaWXaloppp962imni84J6qibphoqqYneVqqerwrVGiui2bFaq6qororrrIDm6iuvpwIrqrC2Ktrqm8Tueqyfy/aarK7QWvrsr80yemu002ZbranbwtqtrN/Squiw4UpbbrDnknsttetq2266xboKr34A1Gvvvfjmq+++/Pbr778AB/yvtTMJbPDBCCes8ML6ovvuw8a2KyQAplRs8cUYZ6zxxhx37PHHIIfcMQAEr0SxyCinrPLKLLd8McnqRiyzvBIXebLLOOes88owe1vTzTsHLfTQKvesLMQ0z4zsxEQ37bTLRotr8tNUVz101OwqzSzS/0vbbPXXYL9cckpAh2322Rpj7a7Wzs6LbaNeoy331WOfVPbceH+ttttZJ+1312TenffgKKsd89SEJ/703lxvzXbd2CkkONFcXDAAAzlcErIeJWzeediGx0v23JO38LEgIsih+MeMP85t420zFrjVYgCAQilxANBByPXyPrnToR9d8OoV/25xBYQQ73HrfzvefOyy02n8zh4AEAfGoAyRAAJHhGJKvVEgEIEA9pryiQ8FIBADHgGEYEr1BJQPdvBv/0y0KGygYDH++r9sCgd36ADyTFGA3mUCC1LwgSNMkYE8gMBeffjAADxAh4plIgtTyEEfDpjABVoMBWsQxQdDuP84h7nOZyfsj4imp7MBAMB7F1MCANjwBgAc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)

Strategy - defines an interface common to all supported algorithms. Context uses this interface to call the algorithm defined by a ConcreteStrategy.   
   
ConcreteStrategy - each concrete strategy implements an algorithm.   
   
Context  

* contains a reference to a strategy object. 
* may define an interface that lets strategy accessing its data. 

The Context objects contains a reference to the ConcreteStrategy that should be used. When an operation is required then the algorithm is run from the strategy object. The Context is not aware of the strategy implementation. If necessary, addition objects can be defined to pass data from context object to strategy.    
   
The context object receives requests from the client and delegates them to the strategy object. Usually the ConcreteStartegy is created by the client and passed to the context. From this point the clients interacts only with the context.   
 

Applicability & Examples 

Example - Robots Application 

![Strategy Example Robot UML Class Diagram](data:image/gif;base64,R0lGODlh6QH0AHAAACwAAAAA6QH0AIcAAAADAwMEBAQFBQUGBgYHBwcICAcICAgJCQkLCwsMDAsMDAwNDQ0PDw8QEA4QEBAREREUFBQWFhYYGBgaGhocHBweHh4gICAiIiInJycpKSkrKystLS0vLy8xMTEzMzM2NjY4ODg6Ojo8PDw+Pj5AQEBCQkJERERHR0dISEhJSUlLS0tNTU1PT09QUEdQUFBRUVFTU1NUVEtUVFRVVVVYWE5YWFhZWVlaWlpcXFJcXFxeXl5gYFVfX19gYF1gYGBiYmJkZF1kZF5kZF9kZGBkZGRmZmZoaGFoaGNpaWlra2tsbGZtbW1vb29wcGpxcXFzc3N1dXV3d3d6enp8fHx/f3F+fn6AgICCgoKEhISGhoaIiIiLi4uNjY2Pj4+RkZGTk5OVlZWXl5eZmZmcnJyenp6goKCioqKjo6OkpKSmpqaoqKipqamqqqqtra2urq6vr6+wsLCxsbGzs7O1tbW3t7e5ubm7u7u+vr7AwMDCwsLExMTGxsbHx8XIyMjLy7XKysrLy8vMzMzPz7jPz8/T07zR0dHT09PX17/V1dXX19fb28Pb28TZ2dnb28nb29rb29vf38fd3d3f397g4ODj48vj48zi4uLj4+Hk5OTn587n58/m5ubn5+Xo6Ojq6urs7Ozu7u7x8fHz8/P19fX39/f5+fn7+/v//+P9/f3///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////8I/wBRCRxIEFWegggTGlTIUODBhgofQkQocSLBihYdZiyIMWNHix8nhoQ4smFJhicjbry4cmDKhC8pttQ4MybHmQtr4kSJ0yZLnUBb+nTZs2jQlUNpCjW69OjGpDmbSkXKlKrTnUSvgqz6lKtH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)

   
Let's consider an application used to simulate and study robots interaction. For the beginning a simple application is created to simulate an arena where robots are interacting. We have the following classes:   
   
IBehaviour \(Strategy\) - an interface that defines the behavior of a robot   
   
Conctete Strategies: AggressiveBehaviour, DefensiveBehaviour, NormalBehaviour; each of them defines a specific behavior. In order to decide the action this class needs information that is passed from robot sensors like position, close obstacles, etc.   
   
Robot - The robot is the context class. It keeps or gets context information such as position, close obstacles, etc, and passes necessary information to the Strategy class.   
   
In the main section of the application the several robots are created and several different behaviors are created. Each robot has a different behavior assigned: 'Big Robot' is an aggressive one and attacks any other robot found, 'George v.2.1' is really scared and run away in the opposite direction when it encounter another robot and 'R2' is pretty calm and ignore any other robot. At some point the behaviors are changed for each robot.  

public interface IBehaviour {   
public int moveCommand\(\);   
}   
   
public class AgressiveBehaviour implements IBehaviour{   
public int moveCommand\(\)   
{   
System.out.println\("\tAgressive Behaviour: if find another robot attack it"\);   
return 1;   
}   
}   
   
public class DefensiveBehaviour implements IBehaviour{   
public int moveCommand\(\)   
{   
System.out.println\("\tDefensive Behaviour: if find another robot run from it"\);   
return -1;   
}   
}   
   
public class NormalBehaviour implements IBehaviour{   
public int moveCommand\(\)   
{   
System.out.println\("\tNormal Behaviour: if find another robot ignore it"\);   
return 0;   
}   
}   
   
public class Robot {   
IBehaviour behaviour;   
String name;   
   
public Robot\(String name\)   
{   
this.name = name;   
}   
   
public void setBehaviour\(IBehaviour behaviour\)   
{   
this.behaviour = behaviour;   
}   
   
public IBehaviour getBehaviour\(\)   
{   
return behaviour;   
}   
   
public void move\(\)   
{   
System.out.println\(this.name + ": Based on current position" +   
"the behaviour object decide the next move:"\);   
int command = behaviour.moveCommand\(\);   
// ... send the command to mechanisms   
System.out.println\("\tThe result returned by behaviour object " +   
"is sent to the movement mechanisms " +    
" for the robot '"  + this.name + "'"\);   
}   
   
public String getName\(\) {   
return name;   
}   
   
public void setName\(String name\) {   
this.name = name;   
}   
}   
   
   
public class Main {   
   
public static void main\(String\[\] args\) {   
   
Robot r1 = new Robot\("Big Robot"\);   
Robot r2 = new Robot\("George v.2.1"\);   
Robot r3 = new Robot\("R2"\);   
   
r1.setBehaviour\(new AgressiveBehaviour\(\)\);   
r2.setBehaviour\(new DefensiveBehaviour\(\)\);   
r3.setBehaviour\(new NormalBehaviour\(\)\);   
   
r1.move\(\);   
r2.move\(\);   
r3.move\(\);   
   
System.out.println\("\r\nNew behaviours: " +   
"\r\n\t'Big Robot' gets really scared" +   
"\r\n\t, 'George v.2.1' becomes really mad because" +   
"it's always attacked by other robots" +   
"\r\n\t and R2 keeps its calm\r\n"\);   
   
r1.setBehaviour\(new DefensiveBehaviour\(\)\);   
r2.setBehaviour\(new AgressiveBehaviour\(\)\);   
   
r1.move\(\);   
r2.move\(\);   
r3.move\(\);   
}   
} 

Specific problems and implementation 

Passing data to/from Strategy object 

Usually each strategy need data from the context have to return some processed data to the context. This can be achieved in 2 ways.  

* creating some additional classes to encapsulate the specific data. 
* passing the context object itself to the strategy objects. The strategy object can set returning data directly in the context. 

When data should be passed the drawbacks of each method should be analyzed. For example, if some classes are created to encapsulate additional data, a special care should be paid to what fields are included in the classes. Maybe in the current implementation all required fields are added, but maybe in the future some new strategy concrete classes require data from context which are not include in additional classes. Another fact should be specified at this point: it's very likely that some of the strategy concrete classes will not use field passed to the in the additional classes.   
   
On the other side, if the context object is passed to the strategy then we have a tighter coupling between strategy and context. 

Families of related algorithms. 

The strategies can be defined as a hierarchy of classes offering the ability to extend and customize the existing algorithms from an application. At this point the composite design pattern can be used with a special care.  

Optionally Concrete Strategy Objects 

It's possible to implement a context object that carries an implementation for default or a basic algorithm. While running it, it checks if it contains a strategy object. If not it will run the default code and that's it. If a strategy object is found, it is called instead \(or in addition\) of the default code. This is an elegant solution to exposing some customization points to be used only when they are required. Otherwise the clients don't have to deal with Strategy objects. 

Strategy and Creational Patterns 

In the classic implementation of the pattern the client should be aware of the strategy concrete classes. In order to decouple the client class from strategy classes is possible to use a factory class inside the context object to create the strategy object to be used. By doing so the client has only to send a parameter \(like a string\) to the context asking to use a specific algorithm, being totally decoupled of strategy classes. 

Strategy and Bridge 

Both of the patterns have the same UML diagram. But they differ in their intent since the strategy is related with the behavior and bridge is for structure. Further more, the coupling between the context and strategies is tighter than the coupling between the abstraction and implementation in the bridge pattern.   
 

Hot points 

The strategy design pattern splits the behavior \(there are many behaviors\) of a class from the class itself. This has some advantages, but the main draw back is that a client must understand how the Strategies differ. Since clients get exposed to implementation issues the strategy design pattern should be used only when the variation in behavior is relevant to them. 

[https://www.java67.com/2014/12/strategy-pattern-in-java-with-example.html](https://www.java67.com/2014/12/strategy-pattern-in-java-with-example.html) 

Strategy Pattern in Java with Example 

like Can you tell me any design pattern which you have used recently in your project, except [Singleton](http://java67.blogspot.com/2012/08/what-is-singleton-pattern-in-java.html)? This is one of the popular questions from various Java interviews in recent years. I think this actually motivated many Java programmers to explore more design patterns and actually look at the original 23 patterns introduced by GOF. [Strategy pattern](http://javarevisited.blogspot.com/2015/07/strategy-design-pattern-and-open-closed-principle-java-example.html) is one of the useful patterns you can mention while answering such a question. It's very popular, and there are lots of real-world scenarios where the Strategy pattern is very handy. Many programmers ask me what the best way to learn design pattern is, I say you first need to find how other people use it and for that, you need to look at the open-source libraries you use in your daily task. JDK API is one such library I use on a daily basis, and that's why when I explore new algorithms, design patterns, I first search JDK for their usage.   
   
The strategy pattern has found its place in JDK, and you know what I mean if you have sorted ArrayList in Java. Yes, a combination of [Comparator](http://java67.blogspot.com/2014/11/java-8-comparator-example-using-lambda-expression.html), [Comparable](http://java67.blogspot.com/2013/08/difference-between-comparator-and-comparable-in-java-interface-sorting.html), and Collections.sort\(\) method are one of the best real-world examples of the Strategy design pattern.   
   
To understand it more, let's first find out what Strategy pattern is? The first clue is the name itself.  The strategy pattern defines a family of related algorithms l sorting algorithms like [bubble sort](http://javarevisited.blogspot.sg/2014/08/bubble-sort-algorithm-in-java-with.html), [quicksort](http://java67.blogspot.sg/2014/07/quicksort-algorithm-in-java-in-place-example.html), [insertion sort](http://java67.blogspot.sg/2014/09/insertion-sort-in-java-with-example.html) and merge sort, or compression algorithm e.g. zip, gzip, tar, jar, encryption algorithm e.g. MD 5, AES etc and lets the algorithm vary independently from clients that use it.   
   
For example, you can use Strategy pattern to implement a method which sort numbers and allows the client to choose any sorting algorithm at runtime, without modifying client's code. So essentially Strategy pattern provides flexibility, extensible and choice. You should consider using this pattern when you need to select an algorithm at runtime.   
   
In Java, a strategy is usually implemented by creating a hierarchy of classes that extend from a base interface known as Strategy. In this tutorial, we will learn some interesting things about Strategy pattern by writing a Java program and demonstrating how it add value to your code. See [Head First design pattern](http://javarevisited.blogspot.com/2014/11/strategy-design-pattern-in-java-using-Enum-Example.html) for more details on this and other GOF patterns. This book is also updated to Java SE 8 on its 10th anniversary.   
   
   
   
   
 

What is the Intent of Strategy Design Pattern? 

While learning a new pattern, most important thing to understand is intent, motivation. Why? because two design pattern can have the same structure but their intent could be totally different. Even, one of a good example of this theory is [State and Strategy pattern](http://javarevisited.blogspot.com/2014/04/difference-between-state-and-strategy-design-pattern-java.html).   
   
If you look at UML diagram of these two patterns they look identical but the intent of State pattern is to facilitate state transition while the intent of Strategy pattern is to change the behavior of a class by changing internal algorithm at runtime without modifying the class itself.  That's why Strategy pattern is part of behavioral patterns in GOF's original list.   
   
You can correlate Strategy pattern with how people use a different strategy to deal with a different situation, for example if you are confronted with a situation then you will either deal with it or run away two different strategies.   
   
If you have not read already then you should also read the [Head First Design pattern](http://www.amazon.com/dp/0596007124/?tag=javamysqlanta-20), one of the best books to learn practical use of design pattern in Java application. Most of my knowledge of GOF design patterns are attributed to this book. It's been 10 years since the book was first released, thankfully it is now updated to cover Java SE 8 as well. 

Terminology and Structure of the Strategy Pattern 

This pattern has two main component, Strategy interface, and Context class. Strategy interface declares the type of algorithm, it can be [abstract class or interface](http://java67.blogspot.sg/2012/09/what-is-difference-between-interface-abstract-class-java.html). For example, you can define a Strategy interface with method move\(\), now this move becomes strategy and different pieces in a game of chess can implement this method to define their moving strategy.   
   
For example, Rook will move only horizontal or vertical, Bishop will move diagonally, Pawn will move one cell at a time and Queen can move horizontal, vertical and diagonally.  The different strategy employed by different pieces for movement are an implementation of Strategy interface and the code which moves pieces is our Context class.   
   
When we change piece, we don't need to change Context class. If a new piece is added, then also your code which takes care of moving pieces will not require to be modified.   
   
Here is UML diagram of Strategy pattern : 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Pros and Cons of Strategy Pattern 

Every algorithm or pattern has some advantage and disadvantage and this pattern is also no different. The main benefit of using the Strategy pattern is flexibility. The client can choose any algorithm at run time, you can easily add new Strategy without modifying classes which use strategies e.g. Context. This becomes possible because the Strategy pattern is based upon [Open Closed design principle](http://java67.blogspot.sg/2012/09/top-10-java-design-pattern-interview-question-answer.html), which says that new behavior is added by writing new code not by modifying the tried and tested old code.   
   
If you use the Strategy pattern, you will be adding a new Strategy by writing a new class that just needs to implement the Strategy interface. Because of the open-closed principle violation, we cannot use [Enum to implement the Strategy pattern](http://javarevisited.blogspot.com/2014/11/strategy-design-pattern-in-java-using-Enum-Example.html%22%20/t%20%22_blank).   
   
Though it has some advantage and suits well if you know major algorithms well in advance you need to modify your Enum class to add new algorithms which is a violation of open-closed principle. To learn more see [here](http://javarevisited.blogspot.sg/2014/11/strategy-design-pattern-in-java-using-Enum-Example.html).   
 

Real-World Examples of Strategy Design Pattern 

JDK has a couple of examples of this pattern, first is Collection.sort\(List, Comparator\) method, where Comparator is Strategy and Collections.sort\(\) is Context. Because of this pattern, your sort method can sort any object, the object which doesn't exist when this method was written. As long as, Object will implement the Comparator interface \(Strategy interface\), Collections.sort\(\) method will sort it.   
   
Another example is  java.util.Arrays\#sort\(T\[\], Comparator &lt; ? super T &gt; c\) method which similar to Collections.sort\(\) method, except need array in place of List.   
   
You can also see the classic [Head First Design pattern](http://www.amazon.com/dp/0596007124/?tag=javamysqlanta-20) book for more real-world examples of Strategy and other GOF patterns.   
   
   
 

Strategy Pattern Implementation in Java 

Here is a simple Java program which implements a Strategy design pattern. You can use this sample code to learn and experiment with this pattern. The example is very simple, all it does is define a [strategy interface](http://java67.blogspot.com/2014/02/what-is-actual-use-of-interface-in-java.html) for sorting algorithms and use that interface on a method called arrange. This method can arrange objects in increasing or decreasing order, depending upon how you implement. In order to arrange an object, you need sorting and this is provided by a Strategy pattern. This allows you to choose any algorithm to sort your object.   
 

/\*\* 

 \* Java Program to implement Strategy design pattern in Java.  

 \* Strategy pattern allows you to supply different strategy without 

 \* changing the Context class, which uses that strategy. You can 

 \* also introduce new sorting strategy any time. Similar example 

 \* is Collections.sort\(\) method, which accept Comparator or Comparable 

 \* which is actually a Strategy to compare objects in Java. 

 \*  

 \* @author WINDOWS 8 

 \*/ 

public class Test { 

    public static void main\(String args\[\]\) throws InterruptedException { 

        // we can provide any strategy to do the sorting  

        int\[\] var = {1, 2, 3, 4, 5 }; 

        Context ctx = new Context\(new BubbleSort\(\)\); 

        ctx.arrange\(var\); 

        // we can change the strategy without changing Context class 

        ctx = new Context\(new QuickSort\(\)\); 

        ctx.arrange\(var\); 

    } 

} 

interface Strategy { 

    public void sort\(int\[\] numbers\); 

} 

class BubbleSort implements Strategy { 

    @Override 

    public void sort\(int\[\] numbers\) { 

        System.out.println\("sorting array using bubble sort strategy"\); 

    } 

} 

class InsertionSort implements Strategy { 

    @Override 

    public void sort\(int\[\] numbers\) { 

        System.out.println\("sorting array using insertion sort strategy"\); 

    } 

} 

class QuickSort implements Strategy { 

    @Override 

    public void sort\(int\[\] numbers\) { 

        System.out.println\("sorting array using quick sort strategy"\); 

    } 

} 

class MergeSort implements Strategy { 

    @Override 

    public void sort\(int\[\] numbers\) { 

        System.out.println\("sorting array using merge sort strategy"\); 

    } 

} 

class Context { 

    private final Strategy strategy; 

    public Context\(Strategy strategy\) { 

        this.strategy = strategy; 

    } 

    public void arrange\(int\[\] input\) { 

        strategy.sort\(input\); 

    } 

} 

Output 

sorting array using bubble sort strategy 

sorting array using quick sort strategy 

Things to Remember about Strategy Pattern in Java 

Now let's revise what you have learned in this tutorial about the strategy design pattern  :   
   
1\) This pattern defines a set of related algorithm and encapsulate them in separated classes, and allows the client to choose any algorithm at run time.   
   
2\) It allows adding a new algorithm without modifying existing algorithms or context class, which uses algorithms or strategies.   
   
3\) The strategy is a behavioral pattern in the GOF list.   
   
4\) The strategy pattern is based upon the Open Closed design principle of [SOLID Principles of Object-Oriented Design](https://pluralsight.pxf.io/c/1193463/424552/7490?u=https%3A%2F%2Fwww.pluralsight.com%2Fcourses%2Fprinciples-oo-design).   
   
5\) Collections.sort\(\) and Comparator interface is a real-world example of the Strategy pattern.   
   
   
That's all about how to implement the Strategy pattern in Java. For your practice write a Java program to implement encoding and allow the client to choose between different encoding algorithm like base 64. This pattern is also very useful when you have situation where you need to behave differently depending upon type like writing a method to process trades if trades are of type NEW,  it will be processed differently, if it is CANCEL then it will be processed differently and if its AMEND then also it will be handled differently, but remember each time we need to process trade.   
   
   
Further Learning   
[Design Pattern Library   
](https://pluralsight.pxf.io/c/1193463/424552/7490?u=https%3A%2F%2Fwww.pluralsight.com%2Fcourses%2Fpatterns-library)[From 0 to 1: Design Patterns - 24 That Matter - In Java    
](https://click.linksynergy.com/fs-bin/click?id=JVFxdTr9V80&subid=0&offerid=323058.1&type=10&tmpid=14538&RD_PARM1=https%3A%2F%2Fwww.udemy.com%2Ffrom-0-to-1-design-patterns%2F)[Java Design Patterns - The Complete Masterclass   
](https://click.linksynergy.com/fs-bin/click?id=JVFxdTr9V80&subid=0&offerid=323058.1&type=10&tmpid=14538&RD_PARM1=https%3A%2F%2Fwww.udemy.com%2Fjava-design-patterns-the-complete-masterclass%2F)[SOLID Principles of Object-Oriented Design   
   
   
](https://pluralsight.pxf.io/c/1193463/424552/7490?u=https%3A%2F%2Fwww.pluralsight.com%2Fcourses%2Fprinciples-oo-design)Other Java Design Patterns tutorials you may like 

* Top 5 Courses to learn Design Pattern in Java \([courses](https://javarevisited.blogspot.com/2018/02/top-5-java-design-pattern-courses-for-developers.html)\) 
* 5 Free Courses to learn Object Oriented Programming \([courses](http://www.java67.com/2018/02/5-free-object-oriented-programming-online-courses.html)\) 
* Difference between Factory and Dependency Injection Pattern? \([answer](https://javarevisited.blogspot.com/2015/06/difference-between-dependency-injection.html)\) 
* Top 5 Courses to learn Microservices in Java with Spring \([courses](https://medium.com/javarevisited/top-5-courses-to-learn-microservices-in-java-and-spring-framework-e9fed1ba804d?)\) 
* How to create thread-safe Singleton in Java? \([example](http://javarevisited.blogspot.sg/2012/12/how-to-create-thread-safe-singleton-in-java-example.html#axzz5EAUtcsud)\) 
* How to implement Strategy Design Pattern in Java? \([example](https://javarevisited.blogspot.com/2015/07/strategy-design-pattern-and-open-closed-principle-java-example.html)\) 
* Difference between Factory and AbstractFactory Pattern? \([example](http://javarevisited.blogspot.sg/2012/12/how-to-create-thread-safe-singleton-in-java-example.html#axzz5EAUtcsud)\) 
* 18 Java Design Pattern Interview Questions with Answers \([list](http://www.java67.com/2012/09/top-10-java-design-pattern-interview-question-answer.html)\) 
* How to design a Vending Machine in Java? \([questions](https://javarevisited.blogspot.sg/2016/06/design-vending-machine-in-java.html#axzz4sZVwtCgs)\) 
* 20 System Design Interview Questions \([list](http://www.java67.com/2018/05/top-20-system-design-interview-questions-answers-programming.html)\) 
* Difference between State and Strategy Design Pattern in Java? \([answer](http://javarevisited.blogspot.sg/2014/04/difference-between-state-and-strategy-design-pattern-java.html)\) 
* Top 5 Courses to learn Design Patterns in Java \([courses](https://javarevisited.blogspot.com/2018/02/top-5-java-design-pattern-courses-for-developers.html)\) 
* 5 Free Courses to learn Data Structure and Algorithms \([courses](https://javarevisited.blogspot.com/2018/01/top-5-free-data-structure-and-algorithm-courses-java--c-programmers.html)\) 
* My favorite courses to learn Software Architecture \([courses](https://medium.com/javarevisited/top-5-courses-to-learn-software-architecture-in-2020-best-of-lot-5d34ebc52e9)\) 

   
Thanks for reading this article so far. If you like these design pattern interview questions then please share with your friends and colleagues. If you have any questions or feedback then please drop a note.   
   
P. S. - If you are looking for some free courses to learn Design Pattern and Software Architecture, I also suggest you check out the [Java Design Patterns and Architecture](http://bit.ly/java-design-patterns-tutorial) course by John Purcell on Udemy. It's completely free, all you need to do is create an Udemy account to access this course.  

   
   
Read more: [https://www.java67.com/2014/12/strategy-pattern-in-java-with-example.html\#ixzz6QNuk4QNa](https://www.java67.com/2014/12/strategy-pattern-in-java-with-example.html#ixzz6QNuk4QNa) 

Adapter Pattern 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Adapter limits change when replacing classes 

* Legacy code relies on the same interface as before 
* Adapter maps the legacy calls to methods of new class 
* 2 forms of the adapter – object adapter and class adapter 
* 1 of several forms of refactoring pattern 

[https://www.geeksforgeeks.org/adapter-pattern/](https://www.geeksforgeeks.org/adapter-pattern/) 

Adapter Pattern 

This pattern is easy to understand as the real world is full of adapters.   For example consider a USB to Ethernet adapter. We need this when we have an Ethernet interface on one end and USB on the other. Since they are incompatible with each other. we use an adapter that converts one to other. This example is pretty analogous to Object Oriented Adapters. In design, adapters are used when we have a class \(Client\) expecting some type of object and we have an object \(Adaptee\) offering the same features but exposing a different interface. 

To use an adapter: 

1. The client makes a request to the adapter by calling a method on it using the target interface. 
2. The adapter translates that request on the adaptee using the adaptee interface. 
3. Client receive the results of the call and is unaware of adapter’s presence. 

Definition: 

The adapter pattern convert the interface of a class into another interface clients expect. Adapter lets classes work together that couldn’t otherwise because of incompatible interfaces. 

Class Diagram:   
![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) 

The client sees only the target interface and not the adapter. The adapter implements the target interface. Adapter delegates all requests to Adaptee. 

Example: 

Suppose you have a Bird class with fly\(\) , and makeSound\(\)methods. And also a ToyDuck class with squeak\(\) method. Let’s assume that you are short on ToyDuck objects and you would like to use Bird objects in their place. Birds have some similar functionality but implement a different interface, so we can’t use them directly. So we will use adapter pattern. Here our client would be ToyDuck and adaptee would be Bird. 

Below is Java implementation of it. 

filter\_none 

edit 

play\_arrow 

brightness\_4 

// Java implementation of Adapter pattern  

interface Bird  

{  

    // birds implement Bird interface that allows  

    // them to fly and make sounds adaptee interface  

    public void fly\(\);  

    public void makeSound\(\);  

}  

class Sparrow implements Bird  

{  

    // a concrete implementation of bird  

    public void fly\(\)  

    {  

        System.out.println\("Flying"\);  

    }  

    public void makeSound\(\)  

    {  

        System.out.println\("Chirp Chirp"\);  

    }  

}  

interface ToyDuck  

{  

    // target interface  

    // toyducks dont fly they just make  

    // squeaking sound  

    public void squeak\(\);  

}  

class PlasticToyDuck implements ToyDuck  

{  

    public void squeak\(\)  

    {  

        System.out.println\("Squeak"\);  

    }  

}  

class BirdAdapter implements ToyDuck  

{  

    // You need to implement the interface your  

    // client expects to use.  

    Bird bird;  

    public BirdAdapter\(Bird bird\)  

    {  

        // we need reference to the object we  

        // are adapting  

        this.bird = bird;  

    }  

    public void squeak\(\)  

    {  

        // translate the methods appropriately  

        bird.makeSound\(\);  

    }  

}  

class Main  

{  

    public static void main\(String args\[\]\)  

    {  

        Sparrow sparrow = new Sparrow\(\);  

        ToyDuck toyDuck = new PlasticToyDuck\(\);  

        // Wrap a bird in a birdAdapter so that it   

        // behaves like toy duck  

        ToyDuck birdAdapter = new BirdAdapter\(sparrow\);  

        System.out.println\("Sparrow..."\);  

        sparrow.fly\(\);  

        sparrow.makeSound\(\);  

        System.out.println\("ToyDuck..."\);  

        toyDuck.squeak\(\);  

        // toy duck behaving like a bird   

        System.out.println\("BirdAdapter..."\);  

        birdAdapter.squeak\(\);  

    }  

}  

Output: 

Sparrow... 

Flying 

Chirp Chirp 

ToyDuck... 

Squeak 

BirdAdapter... 

Chirp Chirp 

Explanation :    
Suppose we have a bird that can makeSound\(\), and we have a plastic toy duck that can squeak\(\). Now suppose our client changes the requirement and he wants the toyDuck to makeSound than ?   
Simple solution is that we will just change the implementation class to the new adapter class and tell the client to pass the instance of the bird\(which wants to squeak\(\)\) to that class.   
Before : ToyDuck toyDuck = new PlasticToyDuck\(\);   
After : ToyDuck toyDuck = new BirdAdapter\(sparrow\);   
You can see that by changing just one line the toyDuck can now do Chirp Chirp !! 

Object Adapter Vs Class Adapter   
The adapter pattern we have implemented above is called Object Adapter Pattern because the adapter holds an instance of adaptee. There is also another type called Class Adapter Pattern which use inheritance instead of composition but you require multiple inheritance to implement it.   
Class diagram of Class Adapter Pattern: 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Here instead of having an adaptee object inside adapter \(composition\) to make use of its functionality adapter inherits the adaptee. 

Since multiple inheritance is not supported by many languages including java and is associated with many problems we have not shown implementation using class adapter pattern. 

Advantages: 

* Helps achieve reusability and flexibility. 
* Client class is not complicated by having to use a different interface and can use polymorphism to swap between different implementations of adapters. 

Disadvantages: 

* All requests are forwarded, so there is a slight increase in the overhead. 
* Sometimes many adaptations are required along an adapter chain to reach the type which is required. 

References:   
Head First Design Patterns \( Book \) 

This article is contributed by Sulabh Kumar. If you like GeeksforGeeks and would like to contribute, you can also write an article and mail your article to contribute@geeksforgeeks.org. See your article appearing on the GeeksforGeeks main page and help other Geeks. 

Please write comments if you find anything incorrect, or you want to share more information about the topic discussed above 

[https://refactoring.guru/design-patterns/adapter](https://refactoring.guru/design-patterns/adapter) 

Adapter 

Also known as: Wrapper 

 Intent 

Adapter is a structural design pattern that allows objects with incompatible interfaces to collaborate. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

 Problem 

Imagine that you’re creating a stock market monitoring app. The app downloads the stock data from multiple sources in XML format and then displays nice-looking charts and diagrams for the user. 

At some point, you decide to improve the app by integrating a smart 3rd-party analytics library. But there’s a catch: the analytics library only works with data in JSON format. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

You can’t use the analytics library “as is” because it expects the data in a format that’s incompatible with your app. 

You could change the library to work with XML. However, this might break some existing code that relies on the library. And worse, you might not have access to the library’s source code in the first place, making this approach impossible. 

 Solution 

You can create an adapter. This is a special object that converts the interface of one object so that another object can understand it. 

An adapter wraps one of the objects to hide the complexity of conversion happening behind the scenes. The wrapped object isn’t even aware of the adapter. For example, you can wrap an object that operates in meters and kilometers with an adapter that converts all of the data to imperial units such as feet and miles. 

Adapters can not only convert data into various formats but can also help objects with different interfaces collaborate. Here’s how it works: 

1. The adapter gets an interface, compatible with one of the existing objects. 
2. Using this interface, the existing object can safely call the adapter’s methods. 
3. Upon receiving a call, the adapter passes the request to the second object, but in a format and order that the second object expects. 

Sometimes it’s even possible to create a two-way adapter that can convert the calls in both directions. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Let’s get back to our stock market app. To solve the dilemma of incompatible formats, you can create XML-to-JSON adapters for every class of the analytics library that your code works with directly. Then you adjust your code to communicate with the library only via these adapters. When an adapter receives a call, it translates the incoming XML data into a JSON structure and passes the call to the appropriate methods of a wrapped analytics object. 

 Real-World Analogy 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

A suitcase before and after a trip abroad. 

When you travel from the US to Europe for the first time, you may get a surprise when trying to charge your laptop. The power plug and sockets standards are different in different countries. That’s why your US plug won’t fit a German socket. The problem can be solved by using a power plug adapter that has the American-style socket and the European-style plug. 

 Structure 

Object adapter 

This implementation uses the object composition principle: the adapter implements the interface of one object and wraps the other one. It can be implemented in all popular programming languages. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

1. The Client is a class that contains the existing business logic of the program. 
2. The Client Interface describes a protocol that other classes must follow to be able to collaborate with the client code. 
3. The Service is some useful class \(usually 3rd-party or legacy\). The client can’t use this class directly because it has an incompatible interface. 
4. The Adapter is a class that’s able to work with both the client and the service: it implements the client interface, while wrapping the service object. The adapter receives calls from the client via the adapter interface and translates them into calls to the wrapped service object in a format it can understand. 
5. The client code doesn’t get coupled to the concrete adapter class as long as it works with the adapter via the client interface. Thanks to this, you can introduce new types of adapters into the program without breaking the existing client code. This can be useful when the interface of the service class gets changed or replaced: you can just create a new adapter class without changing the client code. 

Class adapter 

This implementation uses inheritance: the adapter inherits interfaces from both objects at the same time. Note that this approach can only be implemented in programming languages that support multiple inheritance, such as C++. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

1. The Class Adapter doesn’t need to wrap any objects because it inherits behaviors from both the client and the service. The adaptation happens within the overridden methods. The resulting adapter can be used in place of an existing client class. 

 Pseudocode 

This example of the Adapter pattern is based on the classic conflict between square pegs and round holes. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Adapting square pegs to round holes. 

The Adapter pretends to be a round peg, with a radius equal to a half of the square’s diameter \(in other words, the radius of the smallest circle that can accommodate the square peg\). 

// Say you have two classes with compatible interfaces: 

// RoundHole and RoundPeg. 

class RoundHole is 

    constructor RoundHole\(radius\) { ... } 

    method getRadius\(\) is 

        // Return the radius of the hole. 

    method fits\(peg: RoundPeg\) is 

        return this.getRadius\(\) &gt;= peg.radius\(\) 

class RoundPeg is 

    constructor RoundPeg\(radius\) { ... } 

    method getRadius\(\) is 

        // Return the radius of the peg. 

// But there's an incompatible class: SquarePeg. 

class SquarePeg is 

    constructor SquarePeg\(width\) { ... } 

    method getWidth\(\) is 

        // Return the square peg width. 

// An adapter class lets you fit square pegs into round holes. 

// It extends the RoundPeg class to let the adapter objects act 

// as round pegs. 

class SquarePegAdapter extends RoundPeg is 

    // In reality, the adapter contains an instance of the 

    // SquarePeg class. 

    private field peg: SquarePeg 

    constructor SquarePegAdapter\(peg: SquarePeg\) is 

        this.peg = peg 

    method getRadius\(\) is 

        // The adapter pretends that it's a round peg with a 

        // radius that could fit the square peg that the adapter 

        // actually wraps. 

        return peg.getWidth\(\) \* Math.sqrt\(2\) / 2 

// Somewhere in client code. 

hole = new RoundHole\(5\) 

rpeg = new RoundPeg\(5\) 

hole.fits\(rpeg\) // true 

small\_sqpeg = new SquarePeg\(5\) 

large\_sqpeg = new SquarePeg\(10\) 

hole.fits\(small\_sqpeg\) // this won't compile \(incompatible types\) 

small\_sqpeg\_adapter = new SquarePegAdapter\(small\_sqpeg\) 

large\_sqpeg\_adapter = new SquarePegAdapter\(large\_sqpeg\) 

hole.fits\(small\_sqpeg\_adapter\) // true 

hole.fits\(large\_sqpeg\_adapter\) // false 

 Applicability 

 Use the Adapter class when you want to use some existing class, but its interface isn’t compatible with the rest of your code. 

 The Adapter pattern lets you create a middle-layer class that serves as a translator between your code and a legacy class, a 3rd-party class or any other class with a weird interface. 

 Use the pattern when you want to reuse several existing subclasses that lack some common functionality that can’t be added to the superclass. 

 You could extend each subclass and put the missing functionality into new child classes. However, you’ll need to duplicate the code across all of these new classes, which [smells really bad](https://refactoring.guru/smells/duplicate-code). 

The much more elegant solution would be to put the missing functionality into an adapter class. Then you would wrap objects with missing features inside the adapter, gaining needed features dynamically. For this to work, the target classes must have a common interface, and the adapter’s field should follow that interface. This approach looks very similar to the [Decorator](https://refactoring.guru/design-patterns/decorator) pattern. 

 How to Implement 

1. Make sure that you have at least two classes with incompatible interfaces: 

* A useful service class, which you can’t change \(often 3rd-party, legacy or with lots of existing dependencies\). 
* One or several client classes that would benefit from using the service class. 

1. Declare the client interface and describe how clients communicate with the service. 
2. Create the adapter class and make it follow the client interface. Leave all the methods empty for now. 
3. Add a field to the adapter class to store a reference to the service object. The common practice is to initialize this field via the constructor, but sometimes it’s more convenient to pass it to the adapter when calling its methods. 
4. One by one, implement all methods of the client interface in the adapter class. The adapter should delegate most of the real work to the service object, handling only the interface or data format conversion. 
5. Clients should use the adapter via the client interface. This will let you change or extend the adapters without affecting the client code. 

 Pros and Cons 

*  Single Responsibility Principle. You can separate the interface or data conversion code from the primary business logic of the program. 
*  Open/Closed Principle. You can introduce new types of adapters into the program without breaking the existing client code, as long as they work with the adapters through the client interface. 
*  The overall complexity of the code increases because you need to introduce a set of new interfaces and classes. Sometimes it’s simpler just to change the service class so that it matches the rest of your code. 

 Relations with Other Patterns 

* [Bridge](https://refactoring.guru/design-patterns/bridge) is usually designed up-front, letting you develop parts of an application independently of each other. On the other hand, [Adapter](https://refactoring.guru/design-patterns/adapter) is commonly used with an existing app to make some otherwise-incompatible classes work together nicely. 
* [Adapter](https://refactoring.guru/design-patterns/adapter) changes the interface of an existing object, while [Decorator](https://refactoring.guru/design-patterns/decorator) enhances an object without changing its interface. In addition, Decorator supports recursive composition, which isn’t possible when you use Adapter. 
* [Adapter](https://refactoring.guru/design-patterns/adapter) provides a different interface to the wrapped object, [Proxy](https://refactoring.guru/design-patterns/proxy) provides it with the same interface, and [Decorator](https://refactoring.guru/design-patterns/decorator) provides it with an enhanced interface. 
* [Facade](https://refactoring.guru/design-patterns/facade) defines a new interface for existing objects, whereas [Adapter](https://refactoring.guru/design-patterns/adapter) tries to make the existing interface usable. Adapter usually wraps just one object, while Facade works with an entire subsystem of objects. 
* [Bridge](https://refactoring.guru/design-patterns/bridge), [State](https://refactoring.guru/design-patterns/state), [Strategy](https://refactoring.guru/design-patterns/strategy) \(and to some degree [Adapter](https://refactoring.guru/design-patterns/adapter)\) have very similar structures. Indeed, all of these patterns are based on composition, which is delegating work to other objects. However, they all solve different problems. A pattern isn’t just a recipe for structuring your code in a specific way. It can also communicate to other developers the problem the pattern solves. 

What is Software Architecture? 

Why should we care? 

* Good things are well architected 
* Good architecture is hard 
* Poor architectures collapse quickly 

Projects will fail 

Architectural Qualities 

* Performance 
* Ease of maintenance 
* Security 
* Testability 
* Usability 

Software architecture is bigger than software 

* View constraint, control and possibility from an enterprise lens 
* Good architecture helps project success, bad architecture ensures it fails 
* Architectural qualities drive much of the work of an architect 
* Established architectural styles should be recognizable and repeatable 

Industry work group that created the standard also created this website \(please forgive the lack of web design\): 

[http://www.iso-architecture.org/ieee-1471/getting-started.html](http://www.iso-architecture.org/ieee-1471/getting-started.html) 

Community-developed description of the ISO 42010 standard on Architecture. 

[https://en.wikipedia.org/wiki/ISO/IEC\_42010](https://en.wikipedia.org/wiki/ISO/IEC_42010) 

Getting Started with ISO/IEC/IEEE 42010 

This page provides some starting points for using the Standard \(previously IEEE 1471:2000\). 

The Standard 

The best place to start is with the Standard itself. The published version of ISO/IEC/IEEE 42010 can be obtained from [ISO](http://www.iso.org/iso/iso_catalogue/catalogue_ics/catalogue_detail_ics.htm?csnumber=50508) or from [IEEE](http://standards.ieee.org/findstds/standard/42010-2011.html). 

The Standard has several parts. The first part is a conceptual model of architecture descriptions \(ADs\). The conceptual model, sometimes called the “metamodel”, defines a set of terms and their relations \[see [Conceptual Model](http://www.iso-architecture.org/ieee-1471/cm/)\]. This metamodel has been widely used and discussed in industry and in the academic literature \[see [Bibliography](http://www.iso-architecture.org/ieee-1471/reading-room.html#refs)\]. The conceptual model establishes terms, their definitions and relations which are then used in expressing the requirements. 

Architecture Descriptions 

The second part of the Standard describes best practices for creating an architecture description. The best practices are specified in the Standard as 24 requirements \(written as “shalls”\) \[see [ADs](http://www.iso-architecture.org/ieee-1471/ads/)\]. An architecture description conforms to the Standard if it satisfies those requirements. Taken together, the “shalls” imply a process for preparing an AD roughly like this: 

1. Identify the system stakeholders who have a stake in the architecture and record them in the AD. Be sure to consider: the users, operators, acquirers, owners, suppliers, developers, builders and maintainers of the system – when applicable. 
2. Identify the architecture concerns of each stakeholder. Be sure to consider these common concerns – when applicable: 

* purposes of the system; 
* suitability of the architecture for achieving system’s purposes; 
* feasibility of constructing the system; 
* potential risks and impacts of the system to its stakeholders, throughout the life cycle; and  
* maintainability and evolvability of the system 

1. Choose one or more architecture viewpoints for expressing the architecture, such that each concern \[see 2, above\] is framed by at least one viewpoint. 
2. Record those viewpoints in the AD and provide a rationale for each choice of viewpoint. 
3. Document each chosen viewpoint by writing a viewpoint definition \[see [below](http://www.iso-architecture.org/ieee-1471/getting-started.html#VPs)\] or citing a reference to an existing definition. Each viewpoint definition links the architecture stakeholders and concerns to the kinds of notations and models to be used. Each viewpoint definition helps readers of the AD interpret the resulting view. 
4. Produce architecture views of the system, one for each chosen viewpoint. Each view must follow the conventions of its viewpoint and include: 

* one or more models; 
* identifying information; 

1. Document correspondences between view and model elements. Analyze consistency across all views. Record any known inconsistencies. 
2. Record the AD the rationale\(s\) for architecture decisions made and give evidence of the consideration of multiple architectures and the rationale for this choice. 

Templates for architecture descriptions and for documenting viewpoints are available \[see: [Templates](http://www.iso-architecture.org/ieee-1471/templates/)\]. 

Architecture Viewpoints 

At the core of the Standard is the idea of architecture viewpoints. A viewpoint is a way of looking at the architecture of a system – or a set of conventions for a certain kind of architecture modeling. An architecture viewpoint is determined by: 

1. one or more concerns; 
2. typical stakeholders \(intrested in those concerns and therefore a potential audience for views resulting from this viewpoint\); 
3. one or more model kinds; 
4. for each model kind \(above\), the conventions: languages, notations, modelling techniques, analytical methods and/or other operations to be used on models of this kind; 
5. sources. 

The ISO/IEC/IEEE 42010 Bibliography contains references to definitions of many existing viewpoints. 

Architecture Frameworks and ADLs 

The third part of the Standard specifies best practices for architecture frameworks. 

The Standard only specifies best practices on the documentation of architectures. It is intended to be used within a life cycle and/or within the context of a method or architecture framework – used to develop ADs. The Standard may be used to structure an AD when applied with various architecture frameworks. For example, the Zachman framework matrix essentially identifies a set of stakeholders and concerns to be addressed, and the cell entries suggest the \(viewpoint\) notations, languages and models. \[See the [Survey of Architecture Frameworks](http://www.iso-architecture.org/ieee-1471/afs/) which includes a number of “viewpoint sets”, for the application domains of enterprises, systems and software. 

The Standard also defines requirements on documenting an architecture framework. 

In a similar manner, the Standard can be used to specify Architecture Description Languages \(ADLs\). 

Architectural Styles 

Pipe and filter 

Event based architecture 

Layered architecture 

Blackboard 

Other 

Pipe and Filter 

* Developing components such that the input and output are the same 
* Similar the ‘pipe’ operator in \*nix systems 
* Allows for expansive reusability and parallelization 

Event based architecture 

* Breaks the common ‘reactive’ model 
* Design entire system in observer / observable pattern 
* Also called the publish-subscribe model 

Layered architecture 

* Only communication is between adjacent layers 
* Layers form abstraction hierarchy 
* Dependencies are top down 
* Client server is an example of a layered architecture 

Architectural styles convey essential aspects 

Architectural style constraints design to benefit certain attributes 

Ensure that all components within the system work together well 

Incorporates ideas at the enterprise level rather than class design 

Established architectural styles should be recognisable and repeatable 

View, Viewpoint and Perspective 

How we think about and document architecture 

Focus on essential aspects of the system being built 

Focus on separation of concerns 

Focus on addressing common issues found in large systems 

Views 

A view captures a model meant to address some concern 

An architecture is the combination of all views 

Each view is defined by a single concern call a Viewpoint 

Viewpoint 

View is the vehicle for portraying architecture 

Viewpoint is the best practice for portraying some specific concern 

A set of viewpoints should address artefacts, development and execution 

Perspective 

For cross cutting concerns that don’t fit into a single view 

Quality attributes come into play here 

Apply to all the viewpoints in the system 

Viewpoint and Perspective guide the work 

Addressing each concern by documenting them separately 

Views are the final product at this stage and are the architecture 

Viewpoints allow system organization systematically 

Perspectives influence each viewpoint and the views they represent 

Writing Scenarios 

Architectural quality 

* A system must exhibit values of quality attributes to be successful 
* Quality concerns tend to cut across views 
* Documenting \(and testing\) these qualities is difficult 

Quality Attribute Scenarios 

* Source 
* Stimulus 
* Environment 
* Artefact 
* Response 
* Response Measure 

Scenario Example - Performance 

Parts Depot Inc 

Large retailer exploring web services 

Large number of services 

Source 

Customer using standard web browser 

Stimulus – comes as a result of the source 

User adds an item to their online shopping cart 

Environment 

System is operating normally, system has fewer than 50 concurrent users. Internet latency is less than 100 ms from customer browser to site 

Artefact 

WAGAU tomcat web site 

Response 

Round trip from customer clicking ‘add to cart’ button to customer browser update showing updated cart 

Response measure 

95% of the time under 2.5 seconds 

99.9% of the time under 10 seconds 

Scenarios help use define good systems 

Heuristics are used to allow definitive measurement 

Documenting quality scenarios is key to validation and acceptance 

Identifying the assumptions in the environment is critical 

User sign off on scenarios gives you definitive goals of quality 

Assignment 

Assessing Quality Through Scenarios 

The learner will select a preferred website. Considering the website, the learner will identify three quality attributes that would be important to the site's success and write one reasonable scenario for each quality attribute, presented in one of the formats presented in class. 

Select a public website that you use enough to be familiar with what a typical user may want to do. This website should not require the peer reviewer to sign up for an account or pay to use the site in any way. The website should also not, to the best of your knowledge, serve malware, use JavaScript to complete cryptocurrency mining, or any other negative practice that might harm the peer reviewer. 

Select three quality attributes that are likely to be important when deciding a website architecture for the website you chose. You can use usability, security, performance, reliability, or any other reasonable quality attribute as the basis of your selection. Briefly explain the importance of each quality attribute as it relates to the software/service you selected. 

Then, for each selected quality attribute, write one scenario that would help quantitatively assess whether the software solution meets its goal. You shall write your scenarios using a format that was presented in the lectures.  

Write your first selection, discussion of importance and scenario here. 

Write your second selection, discussion of importance and scenario here. 

Write your third selection, discussion of importance and scenario here. 

Security Perspective 

Security – security is the set of processes and technologies that allow the owners of resources in the system to reliably control who can perform actions on particular resources 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Security is risk management 

Policy – identify risks, categorize and prepare mitigation 

Evaluating the cost and benefit of risks and their prevention 

Identify the principles, resources and sensitive operations 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Security Threats 

Identify sensitive resources 

For each resource 

* What are the characteristics of attackers? 
* Who could try to infringe security? 
* How could they attempt to bypass countermeasures? 
* What would be the consequence? 

Security requires persistent evaluation 

Resources, attacks and best practices must evolve over time 

Managing risk can only happen with analysis 

Analysis includes actor characteristics 

Attack trees can be used to organise security risks 

Attack Trees Models 

Red team – people to come in and attack the system to test its security 

Identifying attack vectors 

Think like an attacker 

Document possible attacks in a tree 

Use the tree to guide further security analysis 

Attack Tree Model 

Format to document results of security anlysis 

Allows for visual categorization to aid understanding 

Gaps and selective elaboration 

Inside attacks are more common than outside 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Attack trees allow for visualising threats 

* Can be used to identify possibility, cost and other attributes 
* Seeing the larger picture is beneficial in analysis 
* These is still a great deal of estimation here, use caution 
* Updating the tree on a regular basis as environment and attacks change 

Security Tactics 

Follow best practice to ease the difficult of meeting and assessing security 

Domain experts have identified and organised defence and analysis 

Technical and social attacks and defences need to be considered 

Recognised Security Principles 

* Principles of least privilege 
* Secure the weakest link – humans are the weakest link 
* Defend in depth 
* Separate and compartmentalize – no single user can have it all 
* KISS – keep it simple stupid 
* Avoid obscurity 
* Use secure defaults 
* Fail secure 
* Assume external entities are untrusted 
* Audit 

Security Audit 

* Most organizations are not mature enough to organize active deterrence 
* Auditing of access and behaviour is essential to discovering breach 
* Logging of all secure authorization and authentication is crucial 

Authenticate and Authorize 

Verify the role and authority 

Ensure that the access control matrix 

* Is implemented properly by access mechanisms 
* Properly implements intent of security policy 

Critical – ensure reliable identification of each principle \(role\) during use 

Information protection 

Secrecy \(or privacy\) is an essential necessity for data 

Transmission of data \(necessary for business\) exposes it to attack 

Encryption can protect information outside authorization control 

Security requires persistent evaluation 

Resources, attacks and best practices must evolve over time 

Managing risk can only happen with analysis 

Analysis includes actor characteristics 

Attack trees can be used to organise security risks 

Coding Style 

Some of this is form over function, there are many defensible choices 

Choices still have to be made – consistency is key 

A variety of types of rule can be considered 

Elements of Good Coding Style 

* Naming conventions 
* Filenames 
* Indentation 
* Placement of braces 
* Use of whitespace \(eg placing pointer symbols\) 

Naming Conventions 

Variable vs Routinevariable\_name vs RoutineName\(\) 

Classes vs ObjectsWidgetmy\_widget 

Member Variables\_variable or variable 

Filenames 

Pick a format 

Common to use underscores \( \_ \) and dashes \(-\) between words 

* My\_shape.cc 
* My-shape.cc 
* Myshape.cc 

Even extensions could need specification 

Indentation 

A timeless battle – tabs vs spaces \(see the reading\) 

Generally speaking, just be consistent 

Important – Indent once per nesting level 

Special rules for when code word wraps at line length limit 

Placement of braces 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Use of whitespace \(eg. Placing pointer symbols\) 

Can make a real difference in understanding 

Double \* a; 

Double\* a; 

Double \*a; 

An example of understanding difficulty: 

Double\* a,b; vs double \*a,b; 

Coding Style 

A matter of ease of understanding 

Attempts to ease cognitive lead 

Consistency allows reader to focus on logic 

Automated processes and tools exist – beautifier 

A discussion of Tabs vs Spaces as indentation 

[https://wiki.c2.com/?TabsVersusSpaces](https://wiki.c2.com/?TabsVersusSpaces) 

[Tabs Versus Spaces](https://proxy.c2.com/cgi/fullSearch?search=TabsVersusSpaces) 

This is one of the eternal [HolyWar](https://wiki.c2.com/?HolyWar)s among programmers: should source-code lines be indented using tab characters or space characters? 

People generally don't mind reading code that is consistently indented using tabs, or code that is consistently indented using spaces. The problems arise when some lines are indented with tabs, and others with spaces. In such cases, the code will only display nicely if the reader has the same tab stop settings as the authors and if all the authors used consistent settings. One way to solve this problem is to force everyone to be "tab people" or "space people". 

The case for tabs: 

* Gives reader control over visual effect. 
* A tab has a meaning of "indent one level" \(disputed; see below\), whereas spaces have many meanings. 
* Fewer keystrokes required to get things aligned. 
* Files are smaller. 
* It's the only way to get vertically aligned columns when we use proportional fonts. 

The case for spaces: 

* Consistent display across all display hardware, text viewer/editor software, and user configuration options. 
* Gives author control over visual effect. 
* Tabs are not as "visible" \(that is, a tab generally looks just like a bunch of spaces\) 

The case for random mixture of tabs and spaces: 

* Easy \(you don't have to think about it\). 
* People who don't like it can use some sort of tool to automatically indent the code however they want. 

Other wrinkles: 

* In some programming languages and tools, tabs and spaces do have different meanings. This argument doesn't apply to those languages, except in relation to [LanguagePissingMatch](https://wiki.c2.com/?LanguagePissingMatch)es. 
* [VersionControl](https://wiki.c2.com/?VersionControl) systems generally do consider whitespace to be significant. If a developer reformats a file to have different indentation, makes a minor change, and then checks in the change, the system is likely to treat it as if the developer changed every line in the file. 
* In [PythonLanguage](https://wiki.c2.com/?PythonLanguage), indentation is semantically significant. Either tabs or spaces may be used for indentation, though it's recommended that programmers use one or the other and stick to it. To quote the language reference, "tabs are replaced \(from left to right\) by one to eight spaces such that the total number of characters up to and including the replacement is a multiple of eight \(this is intended to be the same rule as used by Unix\)." 
* In some editors, hitting the TAB key inserts a tab character at the current position. However, programmers' editors can be configured to use the TAB key to trigger the editors' auto-indent function, which may generate multiple tab characters or multiple spaces. 
* Some text editors can determine the proper tab settings for a file by analyzing it or by reading special markup contained within. Such editors are nice for those people who have them, but they do not solve the general problem. 

Programmers also argue about whether it is acceptable to use tab characters inside source code lines for purposes other than left-side indentation. People may use these to align elements of a multi-line statement or function call, or to align end-of-line comments. The issues are similar to those above, except that tabs inside lines cause addtional problems. 

Most programming languages provide a special character sequence \(such as "\t" in C, C++, Java, and others\) to allow a programmer to make the difference between tabs and spaces more obvious inside strings and character literals. In such languages, it is generally considered bad style to put actual tab characters inside string and character literals. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

The above is an attempt to summarize the discussion below. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

This is a rant about Jamie Zawinski's rant at [http://www.jwz.org/doc/tabs-vs-spaces.html](http://www.jwz.org/doc/tabs-vs-spaces.html) 

Read his rant first. 

Jamie Zawinksi brings up the crucial issue and fails to recognize the significance. \(Because he is clearly a space person.\)  

His mistake is reducing ASCII character 9 to "compression". In his mind ASCII 9 means "display some number of spaces" and that the problem is that people don't agree about what that number should be. WRONG! The point is that code, like any other kind of structured information, has MEANING. The tab character means "indent 1 level" and if programming languages were XML might be written something like &lt;tab/&gt;. How your editor \(or browser or whatever\) chooses to present &lt;tab/&gt; should be determined by your editor's configuration, just like the presentation of &lt;tab/&gt; in an xml document should be determined by its stylesheet. 

To Quote: " With these three interpretations, the ASCII TAB character is essentially being used as a compression mechanism, to make sequences of SPACE-characters take up less room in the file." 

In fact, the tab character is not just a compression for an unspecified number of spaces: I might create an editor that defines the "indent distance" in terms of millimeters! I might create an editor that uses colors instead of actually offsetting the beginning of lines! This reminds me of a friend who said "C++ is all waste: I can do that in pure C with arrays of function pointers." 

The very worst thing to do is the suggestion that he makes: get rid of all tab characters. The problem is information entropy: it is difficult and sometimes impossible to compute "indent distance" from a file which has no tabs \[think inconsistent spacing\]; this is like removing all your &lt;td&gt; tags from a table and replacing them with an equivalent sequence of &nbsp; - a solution that works fine for your 21" monitor but not for my 17" one.  

In fact, the solution is exactly the opposite: NEVER REPLACE TABS WITH SPACES! All editors can be configured to present whatever "indent distance" is desired and without having to add all kinds of crazy comments \(as jwz seems to suggest\). As long as no one in a group of developers uses spaces to indicate an indent, nobody should ever even have to know what other people's preferred "number of columns" is! 

Go forth and tabify! 

-- [KerryKartchner](https://wiki.c2.com/?KerryKartchner) 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

" With these three interpretations, the ASCII TAB character is essentially being used as a compression mechanism, to make sequences of SPACE-characters take up less room in the file." The rant totally ignores the etymology of the tab, and this sentence kind of sums that up: typewriters \(with their tab stops, often custom-settable\) had no concern for how many bytes it took to encode the content they were putting onto paper. Tabs were essentially being used as an indentation mechanism, to ensure that the indentation was consistent \("Did I hit &lt;space&gt; six times or only five?"\). 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

The tab character means "indent 1 level"... 

That assumes "indent 1 level" is meaningful, and I have encountered lots of instances where there is no meaningful interpretation of "indent 1 level". 

For example, when you break a function call with, say, 4 parameters into 4-5 lines, with each parameter on its own line. Often, I want the 2nd parameter to line up with the 1st, what is the "indentation level" of the 2nd parameter? 

''Given that the function call starts at indententation level N, the following lines \(containing further parameters to the function\) are at indentation level N+1.'' 

No, that only makes parameter 2,3,4 line up with each other. They won't line up with parameter 1 except by accident. 

You need spaces \(and a monospace font\) to get things to line up like this: 

  do\_something\_nifty\( meaningful\_name\_source, 

                      meaningful\_name\_for\_dest, 

                      case\_insensitive, 

                      other\_relevant\_parameters 

                      \); 

Yeah, but if you \*really\* need parameter 1 to line up, you can do it like this: 

  do\_something\_nifty\( 

      meaningful\_name\_source, 

      meaningful\_name\_for\_dest, 

      case\_insensitive, 

      other\_relevant\_parameters 

      \); 

which works with either spaces or tabs, both monospace and proportional fonts. 

Tabs for indentation, spaces for alignment 

Emacs: [http://www.emacswiki.org/SmartTabs](http://www.emacswiki.org/SmartTabs) 

Vim: [http://www.vim.org/scripts/script.php?script\_id=231](http://www.vim.org/scripts/script.php?script_id=231) 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

For source code, indentation can in most cases be generated from the code's structure. Don't represent "indent N levels" with tabs or spaces, you already have all you need stored as "if \(...\) {" on the line above. Remember, source code is not text. 

Then [WhatIsSourceCode](https://wiki.c2.com/?WhatIsSourceCode) ? 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

The tab character means "indent 1 level"... 

Actually, for most text editors it means "indent to the next tab stop." For example, one might use tab character to offset the line, to format the columns of a table and to indent the //-style comment on the same line, such as in: 

&lt;tab&gt;&lt;tab&gt;&lt;tab&gt;&lt;tab&gt;&lt;tab&gt;&lt;tab&gt;&lt;tab&gt;&lt;tab&gt;&lt;tab&gt;&lt;tab&gt; 

&lt;tab&gt;char my\_table\[2\]\[\] = { 

&lt;tab&gt;&lt;tab&gt;{ "The first line",&lt;tab&gt;&lt;tab&gt;"abcd" }, 

&lt;tab&gt;&lt;tab&gt;{ "The thirty-second line",&lt;tab&gt;"cdba" }&lt;tab&gt;// Cheating here 

&lt;tab&gt;}; 

As you can see from the example, the difference between "indent 1 level" and "indent to the next tab stop" sometimes means the difference between the number of tab stops used to achieve the same visual representation. 

...and if programming languages were XML might be written something like &lt;tab/&gt;. 

Most programming languages ignore the tab character as a whitespace. You might as well just not write it at all, especially if your programming language were XML. 

The problem is information entropy: it is difficult and sometimes impossible to compute "indent distance" from a file which has no tabs... 

That's exactly why you have to know what other people's preferred "number of columns" is if you are using tab characters in programming languages which treat tabs as whitespaces. 

There are two uses of "indent to the next tab stop" in such programming languages: 

The first is to duplicate in a visually efficient form the structural information already contained in the code \("a poor man's [PrettyPrinter](https://wiki.c2.com/?PrettyPrinter)"\). You don't lose this information if you convert whitespaces to whitespaces, and a good [PrettyPrinter](https://wiki.c2.com/?PrettyPrinter) will do much more than your tab surrogate. 

The second is to provide a reader with the visual representation which isn't contained in the code itself. In this case converting tabs to the corresponding space-indents loses nothing, but losing the tab stops layout makes a mess from the visual representation. 

I might create an editor that uses colors instead of actually offsetting the beginning of lines! 

And you might create an editor that uses colors instead of letters. But most editors in use don't do that, and rightly so. -- [NikitaBelenki](https://wiki.c2.com/?NikitaBelenki) 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

The tab character means "indent 1 level" 

To my jaded view, the tab character is shorthand notation for the XML equivalent "&lt;TAB/&gt;. 

This, in turn, means whatever the tool that reads it wants it to mean. Here are some "meanings" that are already reasonably widespread: 

* Introduce some whitespace 
* Join or separate the current line to the preceding line \(as in "make" and some of its brethren\) 
* Separate two elements \(as in tab-delimited file formats for spreadsheets and their brethren\) 
* Signal the boundary of a semantic element \(in syntax-aware IDE's\) 

There are surely more "meanings" than these four that just haven't occurred to me yet. Replacing tabs with spaces is an incredibly BRAINDAMAGED approach because: 

* It is non-reversible \(without extensive comments and associated rules\) 
* It confuses the representation of the thing with the thing 
* It obscures the meaning of the author 

Brian Cantwell-Smith presents a compelling model that is perhaps relevant: He suggests that we contemplate three different sets: 

* Notation: A particular "marking". "Three", "3", and "III" are three \(hah!\) different notations for the same thing. Some notations for "tab" include "&lt;Tab/&gt;, "\t", "0x0009" and "0x09" \(there may be others\). 
* Symbol: A unique token manipulated by a formal system. Various programs have various symbols for tab -- some of the more broken programs require very elaborate symbols \(such as Zawinski's proposed combination of comments and spaces\). 
* Meaning: An interpretation that we apply to a symbol. Four are enumerated above. 

My suggestion is that a "file" can use whatever Notation it likes for tab, so long as the system that reads it has a mapping onto its tab Symbol, and we are then able to apply whatever Meaning we desire. My own experience has been that embedding an 0x09 in an 8-bit ascii file is easiest to read by the largest variety of programs that I use, and results in the most straightforward way for me to reflect the various meanings that tab has. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

For the "meaning" that you get out of tabs, you don't get much mileage. So someone who prefers 4-space tabs can be happy viewing the code you wrote assuming 3-space tabs. Is it worth the anal-retentiveness? It's really hard to get it exactly right all the time. I have never seen anyone so anal-retentive. Part of the problem is that by default in most editors, tab characters are indistinguishable from spaces. So you don't even know if you've got it right by just casually looking at your own code. 

Having spent the slight majority of my 11 years as a software developer doing maintenance programming, and having downloaded a lot of source from [SourceForge](https://wiki.c2.com/?SourceForge), I can tell you the defacto standard is Tabs Randomly Interspersed In Varying Densities. I don't recall ever seeing a correctly tabbed source file, but I am very thankful when I see a source file with no tab characters at all. They are readable, whether the indentation is 2, 3, or 4. What makes it unreadable is those random tabs. First, I try to guess the author's tab settings. It's usually 2, 3, 4, 6, or 8. If that fails, or if there are several source files in the same project by different authors with different tab settings, I reformat it \(with vi's automatic reformatting \(=\)\). But that's not preferable, since continuation lines and multi-line comments tend to get strangely indented by that. 

So, you can continue hoping the whole world turns anal-retentive. But I'm with jwz. 

Problem: tabs . . . solution: write a program to convert source to your ideal format using editable rules \(for ease of maintenance\). 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

So, you can continue hoping the whole world turns anal-retentive. But I'm with jwz. -- [AnonymousDonor](https://wiki.c2.com/?AnonymousDonor) 

[ProgrammingIsHard](https://wiki.c2.com/?ProgrammingIsHard). Close counts in horseshoes, grenades, and atom bombs. Not programming. If you aren't "anal-retentive", then why \(how? --ed\) are you programming? 

Source code works the same way regardless of whether it has tabs or spaces. That is why most people don't worry much about it: [ProgrammingIsHard](https://wiki.c2.com/?ProgrammingIsHard) and they have more important things to do than futz around with making sure their tabs are consistent. Maybe they should, but they don't, and your silly warfare metaphors won't change that. That's the author's point - tabs make things unnecessarily complicated and life would be easier if everyone used spaces. -- [KrisJohnson](https://wiki.c2.com/?KrisJohnson) 

I hope you aren't working on the makefiles for my next major system build. Oversimplifying complex things is a source of much of today's increasingly unreliable software. Inconsistent tab/space formats that break already fragile IDE's \(because the IDE developers in turn seem to rely on oversimplified mechanisms to identify syntactic elements\) drive whole development teams into using brute-force character editors such as VI and EMACS more than two decades after superior technologies became widely available. If you need a convincing illustration, try debugging even the most straightforward [JavaScript](https://wiki.c2.com/?JavaScript) code under Venkman, the latest greatest state of the art [JavaScript](https://wiki.c2.com/?JavaScript)debugger from the Mozilla folks. I know, you don't need a debugger - all you have to do is insert lots of print statements and then look at the log files. For that matter, tell me about how your "uncomplicated" tab-to-space-converting java editor will let you develop and debug the tab-separated output that your client needs to import into their accounting packages. I guess you'll just have a simple little enhancement that will distinguish the tabs you're trying to emit to the output from the tabs you're indenting your code with - or perhaps you'll just skip all that stupid wasted whitespace and left-align everything. 

I thought it was pretty clear that this discussion is related only to those cases where tabs and spaces are equivalent. We aren't talking about changing the syntax of make or destroying tab-delimited files. I don't think any automated tab-to-space conversion tool would be so brain-damaged that it would convert the "\t" sequence in a Java string to a space. If you are putting literal tab characters into your literal Java strings, rather than using \t, you and the poor souls maintaining your code are going to get some nasty surprises someday. -- [KrisJohnson](https://wiki.c2.com/?KrisJohnson) 

Where did anything on this page limit this discussion "only to those cases where tabs and spaces are equivalent"? It sounds to me as though your convention is painting you into a corner where you are required to jump through very special hoops to use your "simplification". Are you sure the source display in your java debugger understands your spaces and tab stops the same way as your editor? Don't you also advocate this for all the other block-structured languages - C, C++, PERL, Smalltalk, etc? Where does [JavaScript](https://wiki.c2.com/?JavaScript) fit into that mix? Don't you indent tags in XML? Do you ever line up the RHS's of blocks of initializations, for legibility? Don't you sometimes like to be able to read javadoc headers, in source code, that have something approximating a tabular format? 

My argument is that your one very specific oversimplification breaks a huge number of things humans do with code to make it legible. Perhaps if you didn't always convert tabs into spaces, you might have more first-hand experience with the huge number of things you exclude by your conversion. 

You've created a clumsy special case when the general works just fine. 

The article by jwz which started this page is clearly about the visual formatting of source code. I believe everything else on the page up until your comments falls in line with that. 

Obviously, tabs are not the same as spaces and replacing all the tabs in the world with spaces would be a disaster. I do not advocate any such position, and you insult me by assuming that I do. 

I went for several years being a "tab person" and several years being a "space person". I am aware of the strengths and weaknesses of both positions, and use whichever convention is favored by whatever people I am working with. I have used both conventions with several block structured languages and have never run into a problem with any debuggers or other tools with either convention. If you are aware of a specific real-world case where using spaces instead of tabs to indent Java or C++ source code causes problems, I'd be interested to hear about it. \(BTW, why would a source debugger fail if space characters are present???\) 

I don't understand why you ask whether I ever indent code or align things vertically. Obviously I do or I wouldn't be participating in this discussion. Yes, I indent tags in XML. Yes, I line up the RHS's of blocks of initializations for legibility. Yes, I sometimes like to be able to read javadoc headers, in source code, that have something approximating a tabular format. All these things can be done using tabs or spaces. What have I written that implies I favor doing away with all indentation? -- [KrisJohnson](https://wiki.c2.com/?KrisJohnson) 

Please consider the simple case of a javadoc comment. Here is an excerpt from the javadoc header for java.lang.Object.clone\(\) \(I'm using version 1.47, 10/01/98 as distributed in [VisualAge](https://wiki.c2.com/?VisualAge) Java for this example\). 

  \* @exception  CloneNotSupportedException  if the object's class does not 

  \*               support the &lt;code&gt;Cloneable&lt;/code&gt; interface. Subclasses 

  \*               that override the &lt;code&gt;clone&lt;/code&gt; method can also 

  \*               throw this exception to indicate that an instance cannot 

  \*               be cloned. 

  \* @exception  OutOfMemoryError            if there is not enough memory. 

  \* @see        java.lang.Cloneable 

  \*/ 

 protected native Object clone\(\) throws CloneNotSupportedException; 

Please note that I've added a leading space to each line in order to avoid extra wiki prettification. Now, although this surely makes me guilty of being anal retentive, please note that the continuation of the "@exception" line is misaligned. Let me ask which, to you, is more legible - the above, or the following: 

  \* @exceptionCloneNotSupportedExceptionif the object's class does not 

  \*support the &lt;code&gt;Cloneable&lt;/code&gt; 

  \*interface. Subclasses that override 

  \* the &lt;code&gt;clone&lt;/code&gt; method can also 

  \*throw this exception to indicate that an 

  \*instance cannot be cloned. 

  \* 

  \* @exceptionOutOfMemoryErrorif there is not enough memory. 

  \* @seejava.lang.Cloneable 

  \*/ 

 protected native Object clone\(\) throws CloneNotSupportedException; 

My clients and coworkers generally prefer the latter. Your approach precludes it. Is this specific enough for you? 

I'd like to add, parenthetically, that I despise the need to embed multiple tabs in the continuation lines - I would think that by 2002 I'd be able to set tab stops as I've been able to do in any word processor for nearly 30 years. But that is clearly asking too much of the developer tool community. 

* There are \(and have been for some time\) plenty of editors which allow one to set tabs at arbitrary positions. The problem with setting them so that this particular documentation lines up "correctly", is that it's going to mess up the tab positions elsewhere in your source file -- [AndySawyer](https://wiki.c2.com/?AndySawyer) 

Your second example is a great illustration of the basic problem with tabs: your example only looks good if tab stops are set at 8 characters, whereas many other authors' examples only look good if tab stops are set at 3, 4, or 5 characters. Here's your second example with spaces used instead of tabs: 

  \* @exception   CloneNotSupportedException     if the object's class does not 

  \*                                             support the &lt;code&gt;Cloneable&lt;/code&gt; 

  \*                                             interface. Subclasses that override 

  \*                                             the &lt;code&gt;clone&lt;/code&gt; method can also 

  \*                                             throw this exception to indicate that an 

  \*                                             instance cannot be cloned. 

  \* 

  \* @exception   OutOfMemoryError               if there is not enough memory. 

  \* @see         java.lang.Cloneable  

  \*/ 

 protected native Object clone\(\) throws CloneNotSupportedException; 

This looks identical \(ignoring the question marks inserted by wiki\), and it doesn't suffer when displayed in an editor with 4-character tab stops. \(BTW, it has been a while since I've used javadoc; if it just doesn't grok spaces, then I'm completely wrong here.\) -- [KrisJohnson](https://wiki.c2.com/?KrisJohnson) 

Of course you can substitute spaces for tabs in my example, I created my example by substituting tabs for spaces in the original. Why do you think my second example breaks if tab stops are set to other than 8? I just tried this out using my handy-dandy MSWord and a monospace font. Yes, its true that because of the brain-damaged tab support offered by most editors \(including the lame textedit box in our browsers\), the number of extra tabs has to be adjusted - but even that can be done programatically for about the same effort as the tab-to-space conversion macro. In my opinion, a modern source code editor should simply provide for tab stops in the same way that every word processor has done it for decades. 

That's exactly the point I've been trying to make. You can't open your tabbed example in any old source code editor and expect it to look like you intend it to. But you can open the spaced example in practically any editor with a monospaced font and it will look fine. -- kj 

Meanwhile, how much work is it when we now have to change text of the comment? The tab-free approach guarantees that \*every\* character added or removed anywhere in the line prior to the rightmost tabstop forces a compensating manual realignment of the intervening whitespace. By the way, the misalignment that results from the Wiki question-mark provides an illustrative example - it broke your tab-free approach. 

I've found that a lot of work is required to edit examples such as the above with tabs or with spaces. With tabs, you may need to hit fewer keys to get things lined up, but you do still have to deal with a variable number of tabs between columns. To avoid these issues, I tend to format things much like your first example, whether I'm using tabs or spaces. -- kj 

Your approach also precludes the use of proportionally-spaced fonts for rendering source code. Proportionally-spaced fonts have been demonstrated to be more legible for hundreds of years. In a proportionally-spaced font, there is no single width for a "space" - the equivalent of a tab stop is the only option. 

There is no single width for a tab-stop either. I actually do write code using proportional fonts once in a while, just for a change of pace. You still have the problem that you don't know how many tabs you need to manually insert to get your columns to line up, and everything gets screwed up if you change the font later. -- kj 

Finally, I would suggest that all of this tab stuff would be even more elegantly simplified by providing effective table support \(because our Javadoc examples are really just tables\). 

Is the horse dead yet? 

Yeah, rigor is setting in. I'll just note that much of what you state here about benefits of tabs is contingent upon having editors that handle tabs in a much different way than most existing source code editors do. I agree that it would be great if we had programming languages with support for smarter word-processor-like editors that knew how to lay out tables of vertically aligned columns with proportional fonts and which would automatically resize and reflow themselves up as they were edited. Whenever we do get those, we probably won't be using space characters or tab characters in the files to control the layout; it will use some sort of structured format like HTML, XML, or RTF. Until we do get those editors, we have to choose plain-old-ASCII workarounds for the tools we do have. Sometimes tabs work best, and sometimes spaces work best. There is no correct answer - both options suck. -- [KrisJohnson](https://wiki.c2.com/?KrisJohnson) 

An alternate view on tabs is that when a file is saved, tab-stops are at 8-character positions, and your editor should be smart enough to allow that when you enter a tab character, it indents however far you want it to, and converts runs of spaces to equivalent tabs and spaces. Obviously for \(arguably smelly\) file-formats like make, automatic expansion and compression of whitespace as tabs would need to be turned off. -- [MartinRudat](https://wiki.c2.com/?MartinRudat) who read something like that in a programmer's editor somewhere. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

at the end of the line 

Most of this page talks about tabs vs. spaces at the beginning of the line or in the middle of a line of text. What about spaces and tabs at the end of the line \(just before the newline character\) ? 

\(Should I make a whole new wikipage to discuss this ?\) 

[ImakeTool](https://wiki.c2.com/?ImakeTool) mentions some tools that do the wrong thing if spaces are accidentally added to the end of the line. 

ProleText: Invisible formatting information is embedded in trailing spaces and tabs on the ends of lines in an ordinary looking plain-text document. "ProleText is a cool hack" -- Kjetil Torgrim Homme 1998/12/01 "We have no interest in financial gain from the format, and will make our own code to process the format available free." -- ClariNet. Everything in ProleText can easily be translated to HTML; the "inform" ProleText to HTML converter is freely available. -- [http://www.vim.org/scripts/script.php?script\_id=2308](http://www.vim.org/scripts/script.php?script_id=2308)[http://rdrop.com/~cary/html/computer\_graphics\_tools.html\#proletext](http://rdrop.com/~cary/html/computer_graphics_tools.html#proletext) 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Perhaps neither spaces or tabs should be in source code other than spaces to separate symbols. The source code editor should be able to style the source text independently of the meaningful code based on styling rules than can be specified by the user of the editor. In this way the code is just the code, and differences between versions when being compared will only highlight meaningful differences. 

Neither a tabber nor a spacer be! 

Discussion of Bad Coding Standards 

[https://wiki.c2.com/?BadCodingStandards](https://wiki.c2.com/?BadCodingStandards) 

[Bad Coding Standards](https://proxy.c2.com/cgi/fullSearch?search=BadCodingStandards) 

Just in case you didn't have enough bad [CodingStandard](https://wiki.c2.com/?CodingStandard)s in your organization, ;-&gt; here are a few additional suggestions: 

* Cluttering source files with revision histories when it's all available from {cvs rcs sccs pvcs svn...} 
* Imposing coding standards from one language on another, e.g. requiring variables to be declared at the beginning of a method in Java, because that's how you do it in C. 
* Every method should have a header comment describing all parameters, callers, and callees \(I'm not kidding\). See [MassiveFunctionHeaders](https://wiki.c2.com/?MassiveFunctionHeaders) 
* There've been some that require descriptions of all local variables in a method header as well. 
* In C++ every "if", "for", and "while" should be followed by a compound block {} because someone once put a stray semicolon after an if \(do I get a special award for reporting this one? It doesn't even solve the problem\). See [BracesAroundBlocks](https://wiki.c2.com/?BracesAroundBlocks) for more discussion of this point. 
* Importing [HungarianNotation](https://wiki.c2.com/?HungarianNotation) into Java "because that's what was useful in C". 
* [HungarianNotation](https://wiki.c2.com/?HungarianNotation). 
* [HungarianNotation](https://wiki.c2.com/?HungarianNotation) as it is commonly known is one of the ass-stupidest notions ever inflicted on programmers and should never have escaped from the dark corner where it was whelped. [HungarianNotation](https://wiki.c2.com/?HungarianNotation) as it was originally designed is a pretty good idea that can help you 'see' dirty code better by encoding a variable's semantics in its name. See? Not type. Semantics. Read the wiki page on the issue for more information. 
* Worrying more about the placement of braces than about the clarity of the code. \(Personally, I prefer K&R style. I like to reserve vertical whitespace for places where I'm separating things for clarity. But, I can read almost any style and will default to maintaining the style of the original author. Second choice is to convert the style using a pretty-printer.\) 
* [LeastCommonDenominatorRules](https://wiki.c2.com/?LeastCommonDenominatorRules). I've been told not to use a given language construct \(e.g., inheritance\) because a maintenance programmer might not know what it does. 
* A variant of the above: "Don't use [DesignPatterns](https://wiki.c2.com/?DesignPatterns) because less sophisticated programmers may not understand them" 
* Never DocumentYourReasoning. Use [DesignPatterns](https://wiki.c2.com/?DesignPatterns), then don't add a quick comment about why you choose that particular one among alternative patterns. 
* Constant for the empty string, StringUtils.EMPTY\_STRING, and guess who had to change all the legacy code to bring it up to "standard". -- [BenArnold](https://wiki.c2.com/?BenArnold) 
* Ben, were they using [EclipseIde](https://wiki.c2.com/?EclipseIde) and getting tired of the non-internationalized string warnings? Living with the warnings is painful. Turning off the warnings loses a useful check. Putting in the non-i18n comments is really painful. Replacing the empty string is, as you've seen, time-consuming. However, why did you have so many empty strings in your code anyway? --[EricJablow](https://wiki.c2.com/?EricJablow) 
* It might have been because concatenation with the empty string behaves like a null-safe toString\(\). 
* All field names begin with an underscore, in Java... because it was their C++ standard. 
* And it was their C++ because they saw that vendor libraries did it, and concluded that it must be good. 
* Which is interesting because the C++ standard explicitly states that you should NOT do this, because these names are reserved for vendor use, and so may not work if you use them in your application programs! 
* On the other hand, if your editor does name completion, typing an underscore produces a list of field names. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

One of the traps of [BadCodingStandards](https://wiki.c2.com/?BadCodingStandards), when paired with ineffectively led code reviews, is that they give non-productive developers a tool for obstructing productive developers. 

Funny how the same deficient beliefs melt away when the developers in question are programming together trying to pass a [UnitTest](https://wiki.c2.com/?UnitTest). 

Maybe, maybe not. If the "productive" developer merely appears productive because he can sling thousands of lines of bad code in a day, he will end up costing you more in the long run. The "unproductive" developer who spots the defects in the code may just be saving your bacon. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

And now for something completely different! Not a 'bad standard' for coding, but standard for 'bad coding', especially in Java. Serious advice for those who want [JobSecurity](https://wiki.c2.com/?JobSecurity) from obfuscated code: [HowToWriteUnmaintainableCode](https://wiki.c2.com/?HowToWriteUnmaintainableCode), by [RoedyGreen](https://wiki.c2.com/?RoedyGreen).  

-- [DickBotting](https://wiki.c2.com/?DickBotting) 

Hrm... Points 22 and 47 remind me of the X window system. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

I'm gonna try really, really hard not to rub too many people's fur the wrong way here. Coding standards - no matter how bad - are a Good Thing from where I sit. At least the client has thought about it a little bit. Even if one of their pimply-faced, aged 23, fresh grads dragged something off of an Internet page and thrashed it into a three page document that's better than nothing at all. With a coding standard you have something to point to and say, "See? It's right there." I will code to anybody's coding standard no matter how bizarre or obtuse. Having even a stupid one eliminates a lot of "religious wars" before they get any steam whatsoever. At my current client I have had to point out a lot of the flaws in the existing standard, of course. The doc gets revised whenever holes show up. Simple. -- [MartySchrader](https://wiki.c2.com/?MartySchrader) 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

 \#define TRY\_START try { 

 \#define TRY\_END } 

 void foo\(\) { 

TRY\_START 

 bar\(\); 

TRY\_END 

... 

 } 

Unfortunately, I'm not making this up... 

Nor was the person who originally coded that. It is a hack, but it isn't necessarily an unwarranted hack - you can simulate exceptions using macros for the \(lame\) compilers that don't support them. Personally, I just say let old junky compilers die without honor, but if you're developing some uberportable code you have to deal with the ugly issues like the above. 

Even more unfortunately, this was not the case. TRY\_START and TRY\_END have been used because they're so much easier to see that a lower case word a couple of braces. 

\([MicroSoft](https://wiki.c2.com/?MicroSoft)'s 16-bit Visual "C++" compiler had no exceptions. How they could call it C++ when it lacked such basic functionality is beyond me, but it did.\) 

They could, because exceptions were simply not part of C++ in the beginning. And a lot of programmers can happily live without them. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

I'm sure you're not \[making up the try/catch macros\] because I've seen worse. As I recall, the GEM developer's kit \(circa mid-80's\) had a file called portab.h that went something like this: 

\#define begin { 

\#define end } 

How anyone could possibly think that by making their code look vaguely like Pascal makes it more portable is beyond me. -- [AlexValdez](https://wiki.c2.com/?AlexValdez) 

There was a similar pack of definitions in the source code for the Bourne shell I once looked at... made C look just like Pascal. -- [DickBotting](https://wiki.c2.com/?DickBotting) 

\[As a matter of fact, you can thank Steve Bourne himself for that. He was an Algol fan and did not care for C braces and such. We made fun of him for that breach of good sense \(of redefining the language with macros, not for preferring Algol\) even back in the 1970s.\] 

I once programmed C at a company where I found, in an .h file, this bit of egregious macro definition:  

 \#define TRUE 1 

 \#define FALSE 0 

... and I thought that was bad enough, until a week later, in another .h file, I came across:  

 \#define TRUE 0 

 \#define FALSE 1 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

I have seen this 

in begin.h { 

in end.h } 

in main.cpp 

\#include "begin.h" 

 .... do some thing 

\#include "end.h" 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Way back in 1969, after I had learned PL/1 and then moved from OS/360 to DOS \(which had a rather less-capable compiler\), I worked in an organization where \[for efficiency reasons\] they insisted that rather than use procedure calls you had to set variables, set a return label into a label variable, and then GOTO the subroutine \(which would return using a GOTO to its global return label variable\). Like: 

param1 = "hello" 

param2 = "world" 

p1ret = next 

goto proc1 

next: 

/\* continue program \*/ 

I don't think they had much idea of the importance of maintainability on that project. 

They probably had scars from previous environments. And maybe the procedure calls were worse than we would imagine. I mis-read your comment at first and it jogged some memories and I found this: "The original IBM Algol compiler did a GETMAIN system call on every procedure call" on [http://compilers.iecc.com/comparch/article/96-07-031](http://compilers.iecc.com/comparch/article/96-07-031) ...which discusses why programmer time wasn't considered valuable compared with efficiency. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Each function gets a banner generated with [FigLet](https://wiki.c2.com/?FigLet). 

Is this real? 

Sorta. A co-worker came in and asked me where banner\(1\) was. I suggested figlet instead, installed it, and then asked why. He wanted it for his header comments. \(Fortunately, he doesn't set project-wide policy.\) 

 //\_    \_\_  \_\_ \_\_\_\_  \_\_\_\_   \_\_\_\_ \_            \_ 

 //    / \  \|  \/  \|  \_ \/ \_\_\_\| / \_\_\_\| \|\_ \_\_ \_\_\_ \_\_\| \| 

 //   / \_ \ \| \|\/\| \| \|\_\) \\_\_\_ \\| \|   \| '\_ \` \_ \ / \_\` \| 

 //  / \_\_\_ \\| \|  \| \|  \_\_/ \_\_\_\) \| \|\_\_\_\| \| \| \| \| \| \(\_\| \| 

 // /\_/   \\_\\_\|  \|\_\|\_\|   \|\_\_\_\_/\\_\_\_\_ \|\_\| \|\_\| \|\_\|\\_\_,\_\| 

 // 

 // 

 //  Do enough parsing to determine handler for the command and then pass data 

 //  etc. to the handler 

My boss requires this. Fortunately, he doesn't get too upset when I "forget". 

Try this: It takes about 2 seconds longer to scroll to the code you are looking for. If you average looking at 300 routines a day \(including re-visits to the same one\), then you spend 2 x 300 = 600 seconds or about 10 minutes a day scrolling past them. That's about 0.17 hours a day. If a year averages about 260 work days, then those banners require a total of about 44 hours a year \(0.17 x 260\). If your salary plus company overhead is about $60/hr, then those banners cost your company about $2640 per year \(60 x 44\). Present that cost analysis to your boss, and see what he says. Ask him if the marketing value of the banners makes up for that amount. Please report back to this wiki his/her reaction. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

I had a co-worker complain about how my code did not conform to the "standard" 80 characters per line because their editor \(Emacs\) was setup to wrap text at 80 characters. I write code on dual flat 20" panel screens both running at 1600 x 1200. I can see well over 80 character per line easily. A lots of the code I write is significantly more legible at greater then 80 characters. I don't have to purposely create variable names x,y,z, x1,y1,z2, etc just so I can do computations in a small space. I can name these variable: centerPointX, centerPointY, rotatingPointX, rotatingPointY, etc.. Is there anyone else out there who agrees? And for you die hard 80 line people, why can't you get a bigger screen. Seeing more code will make you more productive. Arggg... -- [AnonymousDonor](https://wiki.c2.com/?AnonymousDonor) 

I DO have a bigger screen. That's so I can see my 80-column Emacs window PLUS another window \(e.g., a browser displaying [JavaDoc](https://wiki.c2.com/?JavaDoc) pages\). 

* What did people who had only 80-column screens do then? Did they have a 40-column editor open, so they could use their other utilities too? We have these things called depth-arrangable windows for a reason. --SamuelFalvo 

I don't stick to a hard & fast 80 chars, but I think it's good to keep it under about 90. This has more to do with [TenWordLine](https://wiki.c2.com/?TenWordLine) than legacy terminal displays. Your eyes have to read sideways if the lines get too long, rather than skimming downwards. 

I do tend to break this a lot when the line isn't all that important, for example unit tests and required parameters where there presence is required by the method name. I never read those anyway, so I don't need to worry too much about readability. 

Why not break the line vertically, eg. after assignment statements or operators, instead of using short variable names? -- [JonathanTang](https://wiki.c2.com/?JonathanTang) 

The 80 character rule is particularly pointless. Based on monitors, eyesight, and screen space taken up by IDEs, one may be able to type fewer or more than 80 characters on a line. Go ahead and type in code that best fits the editior environment currently in use. I usually do not worry about a couple of characters that go past the end of the screen and only fix the format if I find it too annoying. Don't try to predict what some unknown person may use in the future to read and edit code. Finally, get on board with the rest of the team and using a common editor and configuration. Don't expect everyone else to do handstands to allow you to use your "clearly superior" code editor. --[WayneMack](https://wiki.c2.com/?WayneMack) 

FWIW, I stick to a 99 character right column in all my code. Why? So I can print it out without having anything wrap onto the next line. \(I print using Courier New@9pt on A4 paper with line numbers so I can do code reviews of my own stuff on the train!\) -- [BevanArps](https://wiki.c2.com/?BevanArps). 

What is the advantage of having everyone on the team use the same editor, that outweighs the advantage of everyone on the team using an editor they find comfortable and productive? -- [GarethMcCaughan](https://wiki.c2.com/?GarethMcCaughan) 

* If you've ever had to pair with a co-developer who was having some problems navigating the code, you'd very quickly realize a different IDE or editor would be a source of great frustration. --SamuelFalvo 
* It's not just the same IDE, it's the same IDE configuration. I'm comfortable with a 9pt font, but my coworker's eyesight is such that he needs at least 36pt. But I'm not about to start trying to limit my lines to 64 characters - I've got more important things to worry about. 

If you're writing open-source software that can and will be hacked on by anyone who wants to bother, it might be polite to not assume everyone in the universe has a 1600x1200 screen. Besides, life can take one weird places, and it might be nice to have code one can comfortably mess with while SSH'd into your server from a VT220 terminal \(true situation\). At least, that's my excuse for sticking to more-or-less 80 columns. -- [SimonHeath](https://wiki.c2.com/?SimonHeath) 

* I don't seem to recall this being an issue back when 40 column screens were the norm, moving towards 80 column screens. Remember, we have 80 column standards only because IBM mainframes chose 80 columns per punchcard. --SamuelFalvo 

Horizontal scrolling can make code very hard to read.  \(Unless your language is optimized for horizontally written content.\) Unless everyone agrees to the same limit, some will be left horizontal scrolling or everyone will have to adopt to identical environments. 

I've found having a horizontal limit helps to guide me to avoid cramming multiple concepts into one line. Compare 

process\_parts\(numWidgets + numGadgets, isInitialized && isIdle, context-&gt;get\_rules\_for\(PROCESSING\)\); 

To 

numParts = numWidgets + numGadgets; 

isReady = isInitialized && isIdle; 

processRules = context-&gt;get\_rules\_for\(PROCESSING\); 

process\_parts\(numParts, isReady, processRules\); 

Or 

process\_parts\( 

numWidgets + numGadgets,  // Number of parts 

isInitialized && isIdle,  // Ready? 

context-&gt;get\_rules\_for\(PROCESSING\)\); // Process Rules 

Some places strictly restrict lines to 74 characters. No more, or your code will not be allowed. 

120 seems to work well for most wide and double-screen environments -- considering multiple windows, side panels and all. 

Limiting width to 80 seems to create problems with reasonably named variables and methods, even if nested conditions and loops are kept to a reasonable level \(line one or two\). Maybe it would work with very highlyobject-oriented code, but it doesn't seem to work well with most Java I've seen -- at least not without MAJOR rework. -- [JeffGrigg](https://wiki.c2.com/?JeffGrigg) 

[PaulGraham](https://wiki.c2.com/?PaulGraham) and some other writers like to maintain a total text width of a few inches for scannability. I suspect the same applies to code. The rest of the screen spacec can be used for utilities or for a vertical split and another batch of code. --[JesseMillikan](https://wiki.c2.com/?JesseMillikan) 

I would be interested in seeing how he structures his Lisp code, because it is not easy to maintain only a few inches when you consider how deeply Lisp code nests. Most Lisp coding conventions I've seen prefer a diagonal layout that can trivially exceed 80 columns, leading to such abhorrences as: 

  \( ....lots of stuff and nesting here; vertical line is right-hand edge of screen .... 

    \(cond               \| 

      \(\(condition-1\)    \| 

       \(result-1\)\)      \| 

      \(\(condition-2\)    \| 

       \(result-2\)\)      \| 

      \(t                \| 

       result-3\)\)\)      \| 

  \)\)\)\)\)...\)\)            \| 

I look at code like this and cannot help but think that a combination of better factoring and a MUCH wider screen would be absolutely critical to good, legible Lisp coding. --SamuelFalvo 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Gee, you think some side effects here? Maybe? 

 if \(a == 5\) { 

printf\("a is equal to 5\n"\); 

b++; 

 } 

 else { 

printf\("a is not equal to 5\n"\); 

b--; 

 } 

Actually, no, I don't see any side effects here, because it is not clear that b is a locally defined and used variable or not. And, a certainly isn't being modified out from the conditional testing. So, no, there is insufficient data to say whether there are any side effects happening here. --SamuelFalvo 

The lifetime and usage of b doesn't matter. The ++ operator usually has the side effect of changing b's value \(same with --\). Even if these operators don't have side effects, there is still the printf statements. --MartinShobe 

I agree with MartinShobe. The 'printf' is cause for a side-effect all on its lonesome \(or a 'computation-effect' if you don't like calling intentional communications 'side-effects', but '[SideEffect](https://wiki.c2.com/?SideEffect)' is the term that has come into wide use\). And the statements 'b++' and 'b--' also have a consequence that qualifies for the term '[SideEffect](https://wiki.c2.com/?SideEffect)' \(having an effect that extends beyond the statement\), with a possible exception being if you overloaded those operators for 'b' to mean something functional. This is true even if you immediately discard 'b' upon exiting the procedure in which it is declared, though in that case you might have been able to say \(if you also rid yourself of the 'printf'\) that the procedure \(as a whole\) had no side-effects. 

In general, if you program with statements rather than expressions, there must be [SideEffect](https://wiki.c2.com/?SideEffect)s. After all, a statement without any [SideEffect](https://wiki.c2.com/?SideEffect)s is a statement that can be optimized by excising it entirely from your program. 

What what you're saying is correct, the original post did not specify any particular context. Every response to mine so far has established a more specific context. Does ++ and -- perform a side-effect? Sure. At the statement level. But across a whole procedure, the answer may not be so clear. 

* Nonetheless it is quite clear that the above is programmed with side-effects, and it is extremely reasonable to justify a claim that there are side-effects \(by pointing at them\). Consider that whole programs can have the emergent property of being side-effect free but still be written in a side-effect-abundant manner. Since we're talking about 'coding-standards' we're not talking about the emergent property... just the nature of the code. 

Statements with no side-effects are still useful. if-statements are side-effect free, unless you use sloppily written macros. All a side-effect is, is something that is not implicit in the inputs and outputs. There is no law that says a side-effect-free computation must do nothing at all. 

* If-statements are of the form if\(condition\) then\(statements-if-true\) else\(statements-if-false\), and \(when executed\) are very rarely side-effect free - that would require both the if-true and if-false sub-statements be side-effect free. And, like any other statement with no side-effect, you could optimize such a statement by being entirely rid of it. If-expressions, OTOH, can be useful even when side-effect free \(if\(condition\) then return\(expression-if-true\) else return\(expression-if-false\)\).  
* And I think that the definition of '[SideEffect](https://wiki.c2.com/?SideEffect)' \(for a function or expression, any non-local change beyond returning a value or set of explicitly defined values\) pretty much means that a completely '[SideEffect](https://wiki.c2.com/?SideEffect)-free' function can, at most, provide exactly the return value and do nothing else. It's worth noting that no function can be completely and truly and absolutely '[SideEffect](https://wiki.c2.com/?SideEffect)-free' in the ideal sense because that would require: no change in time, no change in energy expended, no change in memory consumed, no change in anything - just an instantaneous and zero-cost return of the appropriate value that, indeed, "does nothing at all". Of course, to make the term practical, side-effects of computation itself \(energy consumed, time, memory, heat production, etc.\) are not generally considered '[SideEffect](https://wiki.c2.com/?SideEffect)s' unless they somehow become critical to the systems with which you're working \(e.g. [HardRealTime](https://wiki.c2.com/?HardRealTime)\).  
* As I understand it, only difference between [SideEffect](https://wiki.c2.com/?SideEffect)-free and [ReferentialTransparency](https://wiki.c2.com/?ReferentialTransparency) is that with side-effect-free you can actually look at the world and mutable state and time and otherwise accept inputs that weren't in your explicit input set \(and with referential transparency, you cannot\). A side-effect-free function can return a different value on every call, even given the same inputs, but it still can't 'do' or 'change' anything. 

That being said, I'm still utterly bamboozled why this is here at all; why should side-effects of the form b++/b-- have any bearing on good/bad programming standards, as illustrated above? If the author had written: 

 void someProcedure\(int a\) { 

     if \(a == 5\) { 

         printf\("a is equal to 5\n"\); 

         b++; 

     } else { 

         printf\("a is not equal to 5\n"\); 

         b--; 

     } 

 } 

this is obviously a bad thing, since the post-increment/decrement operators are touching stuff that is not explicitly passed into the procedure as a variable. Rewriting this in a side-effect-free form: 

 int someFunction\(int a\) { 

     int aEquals5 = a == 5; 

     char \*perhaps = aEquals5? " " : " not "; 

     printf\("a is%sequal to 5\n", perhaps\); 

     return b + \(aEquals5 ? 1 : -1\); 

 } 

This is positively side-effect free, except for the printf\(\). --SamuelFalvo 

I also haven't a clue as to the context that brought this into [BadCodingStandards](https://wiki.c2.com/?BadCodingStandards). I was simply responding to your own statement. As to whether the 'b++' and 'b--' are a 'bad' thing - that is still questionable and not obvious. I've never seen a convincing argument that [SideEffect](https://wiki.c2.com/?SideEffect)s are fundamentally always a 'bad' thing, and the need to hack around communications issues in Haskell, and the prevalence of databases and filesystems, all seem to be points to the contrary.  

Programming with side-effects certainly ought to be controllable or at least traceable, such that you can track all non-local changes back to their source, and it would be nice if such could be compiler and programming-environment supported. But if 'b' is well defined with a comment to the effect '//balance of someFunction\(x\) where x=5', that requirement is minimally met. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

 if \(foo\) { 

   // ... 

 } // end if 

 void foo\(\) { 

   // ... 

 } // end foo 

We have somebody at work that does this excessively, even for single line blocks. Here are my issues with it: 

* It breaks up the structure of the code, making it harder to read. 
* The // end &lt;method name&gt; ones become out of date when a method is renamed. 
* My IDE already has parenthesis/brace matching. 

I can understand the reason for using this kind of comment for very long blocks and where many braces close at the same time, but honestly most IDEs can highlight matching braces/parens for you, which renders this whole thing obsolete. 

And if you find the need to this, I'd suggest you look to refactor your code to make it smaller/less nested. 

Code Style- additional aspects 

Not just about spacing and layout 

Most style guides also dictate a variety of naming conventions 

Self documenting code is also a major factor 

Style seems simple until you see examples of poor style 

The intention is to ease understanding for new readers 

When alternatives exist, select one and enforce it 

Consistency is key 

In order to get a sense of the importance of coding style, this assignment asks the learner to review an established \(i.e. documented\) style guide. Learners will identify three style rules that they agree with and three they disagree with, and provide an explanation of why for each. 

Select three items of the style guide that you agree with and, for each, explain why. If there are not enough items you agree with, give your best estimation as to the reason behind the selection \(in your own words\) and the benefits it provides. Note: "There is no reason" and "There are no benefits" are not acceptable answers here. 

Select three items of the style guide that you do not agree with and, for each, explain why. If there are not enough items you disagree with, give your best estimation as to why someone might disagree and what possible downside there is to using it. 

Debugging and Static 

Debugging 

The art of removing defects 

2 major forms – print statements and debugging tools 

Difficulty in visualizing state of the program 

Error Messages 

Error messages are notoriously cryptic in many languages 

Even simple mistakes can result in massive walls of error text 

Customizing error messages can also help 

Identify last known statement to be executed 

Use a debugger 

Debugging 

Using a debugger grants powerful execution statement views 

Debuggers have a sharp learning curve 

Print statements are quick but limited 

In both cases visualization and is not error proof 

Static Analysis 

Variety of way to check code quality by examining source 

Attempt to check beyond syntax errors 

Common error prone areas of development can be analyzed 

Types of analysis 

* Unused variables 
* Empty catch blocks 
* Unnecessary object creation 
* Duplicated code 
* Incorrect Boolean operator 
* Some typos 
* Use of null pointers 
* Division by zero 
* Overflows 
* Out of bounds checks 
* Information leak 
* Use of unsanitized input 
* Many more… 

Static Analysis Control 

Tools to discover poor quality in code while at rest 

Many tools exist for a variety of purposes and languages 

Some level of false positive is to be expected 

One additional automated tool to help find quality problems 

Here are some additional introductions to static analysis tools. 

Very short, but is the portal to much more info.: [https://pmd.github.io/\#about](https://pmd.github.io/#about) 

Again, short, but gateway to another tool: [http://findbugs.sourceforge.net/factSheet.html](http://findbugs.sourceforge.net/factSheet.html) 

Longer FAQ for another tool: [https://scan.coverity.com/faq](https://scan.coverity.com/faq) 

FindBugs looks for bugs in Java programs.  It is based on the concept of bug patterns.  A bug pattern is a code idiom that is often an error.  Bug patterns arise for a variety of reasons: 

* Difficult language features 
* Misunderstood API methods 
* Misunderstood invariants when code is modified during maintenance 
* Garden variety mistakes: typos, use of the wrong boolean operator 

FindBugs uses static analysis to inspect Java bytecode for occurrences of bug patterns.  Static analysis means that FindBugs can find bugs by simply inspecting a program's code: executing the program is not necessary.  This makes FindBugs very easy to use: in general, you should be able to use it to look for bugs in your code within a few minutes of downloading it.  FindBugs works by analyzing Java bytecode \(compiled class files\), so you don't even need the program's source code to use it.  Because its analysis is sometimes imprecise, FindBugs can report false warnings, which are warnings that do not indicate real errors.  In practice, the rate of false warnings reported by FindBugs is less than 50%. 

FindBugs supports a plugin architecture allowing anyone to add new bug detectors.  The [publications page](http://findbugs.sourceforge.net/publications.html) contains links to articles describing how to write a new detector for FindBugs.  If you are familiar with Java bytecode you can write a new FindBugs detector in as little as a few minutes. 

FindBugs is free software, available under the terms of the [Lesser GNU Public License](http://www.gnu.org/copyleft/lesser.html).  It is written in Java, and can be run with any virtual machine compatible with Sun's JDK 1.5.  It can analyze programs written for any version of Java.  FindBugs was originally developed by Bill Pugh and David Hovemeyer.  It is maintained by Bill Pugh, and a [team of volunteers](http://findbugs.sourceforge.net/team.html). 

FindBugs uses [BCEL](http://jakarta.apache.org/bcel/) to analyze Java bytecode.  As of version 1.1, FindBugs also supports bug detectors written using the [ASM](http://asm.objectweb.org/) bytecode framework.  FindBugs uses [dom4j](http://dom4j.org/)for XML manipulation. 

What is Coverity Scan? 

Coverity Scan is a service by which Synopsys provides the results of analysis on open source coding projects to open source code developers that have registered their products with Coverity Scan. 

Synopsys, the development testing leader, is the trusted standard for companies that need to protect their brands and bottom lines from software failures. Coverity Scan is powered by Coverity® Quality Advisor. Coverity Quality Advisor surfaces defects identified by the Coverity Static Analysis Verification Engine \(Coverity SAVE®\) for fast and easy remediation. 

Synopsys offers the results of the analysis completed by Coverity Quality Advisor on registered projects at no charge to registered open source developers. 

What is static analysis? 

Static analysis is a set of processes for finding source code defects and vulnerabilities. 

In static analysis, the code under examination is not executed. As a result, test cases and specially designed input datasets are not required. Examination for defects and vulnerabilities is not limited to the lines of code that are run during some number of executions of the code, but can include all lines of code in the codebase. 

Additionally, Synopsys's implementation of static analysis can follow all the possible paths of execution through source code \(including interprocedurally\) and find defects and vulnerabilities caused by the conjunction of statements that are not errors independent of each other. 

What types of issues does Coverity Quality Advisor find? 

Some examples of defects and vulnerabilities found by Coverity Quality Advisor include: 

* resources leaks 
* dereferences of NULL pointers 
* incorrect usage of APIs 
* use of uninitialized data 
* memory corruptions 
* buffer overruns 
* control flow issues 
* error handling issues 
* incorrect expressions 
* concurrency issues 
* insecure data handling 
* unsafe use of signed values 
* use of resources that have been freed 

The consequences of each type of defect or vulnerability are dependent on the specific instance. For example, unsafe use of signed values may cause crashes, lead to unexpected behavior, or lead to an exploitable security vulnerability. 

How do I register a project for Coverity Scan? 

Your project may already be registered with Coverity Scan, please check at [scan.coverity.com](https://scan.coverity.com/). If your project is not already listed, sign up and click on Add project and register your new project Finally fill out the resulting form and click Submit. 

Register your project with Coverity Scan by completing the project registration form found at [scan.coverity.com](https://scan.coverity.com/). Upon your completion of project registration \(including acceptance of the Scan User Agreement\) and your receipt of confirmation of registration of your project, you will be able to download the Software required to submit a build of your code for analysis by Coverity Scan. You may then download the Software, complete a build and submit your Registered Project build for analysis and review in Coverity Scan. Coverity Scan is only available for use with open source projects that are registered with Coverity Scan. 

To be considered an open source project, your project must meet all of the following criteria \(adopted from the [Open Source Initiative](http://opensource.org/docs/definition.php) definition of open source\): 

1. Your project must be freely redistributable. Your project license terms must not restrict any party from selling or giving away the project as a component of an aggregate software distribution containing programs from several different sources. The license terms must not require a royalty or other fee for such sale. 
2. Your project license terms must include a license to the project source code. Your project must include source code, and must allow distribution in source code as well as compiled form. Where some form of a product is not distributed with source code, there must be a well-publicized means of obtaining the source code for no more than a reasonable reproduction cost preferably, downloading via the Internet without charge. The source code must be the preferred form in which a programmer would modify the program. Deliberately obfuscated source code is not allowed. Intermediate forms such as the output of a preprocessor or translator are not allowed. 
3. Users must be able to make and distribute modified and derivative versions of your project. Your project license terms must allow for user modifications and derived works, and must allow modifications and derived works to be distributed under the same terms as the license of the original software. 
4. Integrity of your project source code may be restricted. Your project license terms may restrict source-code from being distributed in modified form only if the license allows the distribution of "patch files" with the source code for the purpose of modifying the program at build time. Your license terms must explicitly permit distribution of your project built from modified source code. Your license terms may require derived works to carry a different name or version number from the original project. 
5. No Discrimination Against Persons or Groups. Your project license terms must not discriminate against any person or group of persons. 
6. No Discrimination Against Fields of Endeavor. Your project license terms must not restrict anyone from making use of your project in a specific field of endeavor. For example, it may not restrict your project from being used in a business, or from being used for genetic research. 
7. Project license rights must apply to distribution of your project. The rights attached to your project must apply to all to whom your project is redistributed without the need for execution of an additional project license by those parties. 
8. Your project license terms must not limit use of your project to a specific product or distribution. The rights attached to the project must not depend on your project being part of a particular software distribution. If your project is extracted from that distribution and used or distributed within the terms of your license terms, all parties to whom your project is redistributed should have the same rights as those that are granted in conjunction your original project distribution. 
9. Your project license terms must not restrict other software. Your project license terms must not place restrictions on other software that is distributed along with your project. 
10. Your project license terms must be technology-neutral. No provision of your project license terms may be predicated on any individual technology or style of interface. 

Projects initiated and maintained by for-profit corporations, or projects with license terms outside the foregoing guidelines, may be approved at Synopsys's discretion. 

If my project is already registered in Scan, how do I get an account? 

If your project is already a Registered Project in Scan, but you are not yet a registered user of Scan, you can  [register with Scan](https://scan.coverity.com/users/sign_up), and upon registration, you can click on Add Project, find your Registered Project in the project table, and request access to the Registered Project of your choice. You will be granted access subject to approval by the Registered Project owner or Scan administrator. 

What is the frequency for build submissions to Coverity Scan? 

The number of weekly builds per project are as follows: 

* Up to 28 builds per week, with a maximum of 4 builds per day, for projects with fewer than 100K lines of code 
* Up to 21 builds per week, with a maximum of 3 builds per day, for projects with 100K to 500K lines of code 
* Up to 14 builds per week, with a maximum of 2 build per day, for projects with 500K to 1 million lines of code 
* Up to 7 builds per week, with a maximum of 1 build per day, for projects with more than 1 million lines of code 

Once a project reaches the maximum builds per week, additional build requests will be rejected. You will be able to re-submit the build request the following week.   
Please contact [scan-admin@coverity.com](mailto:scan-admin@coverity.com) if you have any special requirements. 

What are the terms applicable to my use of Scan? 

Your use of Scan, the analysis provided in connection with the Scan service, and any software provided by Synopsys for your use of Scan are subject to the terms and conditions of the Coverity Scan User Agreement, which may be found [here](https://scan.coverity.com/policy). Your use of Coverity Scan constitutes your acceptance of the terms and conditions of the Scan User Agreement, the Scan Terms of Use, and any additional terms and conditions stated in your email \(delivered to you upon successful registration of your project\). 

Who may be granted access to a Registered Project? 

Generally, access to the detailed analysis results for most Registered Projects is granted only to members of the Registered Project approved by the Registered Project administrator, to ensure that potential security defects in the Registered Project may be resolved before the general public sees them. 

Coverity Scan uses the Responsible Disclosure approach. Scan provides the analysis results to the project developers only, and do not reveal details to the public until an issue has been resolved. For a thorough discussion of Responsible Disclosure, you can refer to comments by [Bruce Schneier](http://www.schneier.com/), or [Matt Blaze](http://www.crypto.com/), or the  [Wikipedia article on Full Disclosure](http://en.wikipedia.org/wiki/Full_disclosure) 

Since projects that do not resolve their outstanding defects are leaving their users exposed to the consequences of those flaws, Synopsys will work to encourage a project to resolve all of their defects. Synopsys may set a deadline for the publication of all the analysis results for a project. 

In the discussion of Full Disclosure and Responsible Disclosure, focus has always been on the topic of handling individual coding issues where the impact is somewhat well understood. In the case of automated code testing tools, the best practices have not been discussed. Testing tools may find large numbers of issues, and those counts include a range of different levels of impact. Since the results require triage by a developer, they can sometimes languish - including those defects whose security implications are exposing end-users' systems. In order to push for those issues to be resolved, in the same spirit as the individual issue disclosure policies, Synopsys may set planned publication dates for the full analysis results of a project. Projects may negotiate with us about the date, if they are making progress on resolving the outstanding issues. 

Does Coverity Scan work with Eclipse Foundation projects? 

Registered Projects, which are also part of Eclipse Foundation, can participate in the Coverity Scan service by using the Coverity Scan plugin on the Hudson server. This plugin sends build and source code management information to Coverity Scan server. Coverity Scan server builds and analyzes the code in the cloud for Registered Projects which are part of Eclipse Foundation, and makes results available online. 

Manual Steps: 

* Add Coverity Scan plugin to your build process  
* Register your project with Coverity Scan to get the Project token 
* Sign-up or Sign-in to Coverity Scan 
* Register your project with Coverity Scan. Project name should be the same as in Eclipse job. 
* After registering your project, copy the "Project token" found under "Project settings" tab 
* Enter the "Project token" and notification email in Coverity Scan plugin 

Background process: 

* Coverity Scan plugin will send the information about your build environment to Coverity Scan server, when you build your project in Hudson Server. 
* Coverity Scan server builds, analyzes and commits the results into Scan database, and results will be available online 
* Summary of the defects found during the analysis is available on Hudson server under "Build History" 
* Login to Coverity Scan to view or triage the defects. 
* Any contributor of the project can register with Coverity Scan to get access to the analysis result. 

Supported Environment for Coverity Scan Hudson plugin: 

* Single SCM / single builder. 
* On one SCM it supports one single repository or location 
* Source Code Management System: 
* SVN 
* Git 
* CVS  
* Builders  
* Ant 
* Maven 
* shell  
* single line commands,  
* multi line commands should be set in a build.sh or similar file 

Why is Synopsys providing the Scan service? 

Coverity Scan began in collaboration with Stanford University with the launch of Scan occurring on March 6, 2006. During the first year of operation, over 6,000 software defects were fixed across 50 C and C++ projects by open source developers using the analysis results from the Coverity Scan service. 

The project was initially launched under a contract with the Department of Homeland Security to harden open source software which provides critical infrastructure for the Internet. The National Cyberspace Strategy document details their priorities to: 

· Identify and Remediate Existing Vulnerabilities; and 

· Develop Systems with Fewer Vulnerabilities and Assess Emerging Technologies for Vulnerabilities 

Those priorities include sub-elements to: 

· Secure the Mechanisms of the Internet 

· Improve the Security and Resilience of Key Internet Protocols 

· Reduce and Remediate Software Vulnerabilities 

· Assess and Secure Emerging Systems 

DHS had no day-to-day involvement in the Scan project, and the three year contract was completed in 2009. 

The result has been overwhelming. With over 6,000 defects fixed in the first year - averaging over 16 fixes every day of the year, recognition of benefits from the Scan service has been growing steadily. Requests for access to the results and inclusion of additional projects have shown that the open source community recognizes the benefits of Scan. 

In response, Synopsys is continuing to fund the Scan beyond the requirements of the DHS contract, which expired in 2009. New registered users will continue to be able to register projects and be given access to the Scan analysis results on an ongoing basis \(time and resources permitting\). 

Commenting 

Code and comments 

In-code documentation 

2 ways to accomplish – commenting and self documenting code 

Comments are ignored by compilers but also by developers 

Self documentation is a part of the code 

Documenting in code 

* Documenting is key to understanding, now and later 
* Self documenting code get updated dynamically 
* Comments provide context that code cannot 
* Both forms are likely necessary 

Version Control Systems 

Version control allows developers to maintain incremental backups 

Allows for separation of code for development, testing and production 

Even more powerful when used to integrate team contributions 

Commits 

Store the newest version of the code-base 

Allows inclusion of descriptive notes \(‘commit message’\) 

Can be used for traceability 

Branching 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

GitHub and GitLab 

* 2 primary providers of remote git repository 
* Generally very similar in capability 
* Allows for push / pull and webhook functionality 

Version Control 

* Effectively a must on modern software development 
* Store backups with contextual history 
* Connect changes to bug tracking 
* Allows multiple developers to work on the same project at once 

[https://guides.github.com/introduction/git-handbook/](https://guides.github.com/introduction/git-handbook/) 

Build Process 

Simple approach using the IDE or command line to compile and execute 

Simple, effective, no prior preparation needed 

Repeatability, consistency, errors are all concerns at the command line 

Understanding and modifiability are issues in an IDE 

Automated Build 

Develop files which control the build process 

Invoke tool commands to accomplish common tasks 

Some primary options – Gradle, Maven, Ant 

Make and Ant 

Traditional tools with rich history and extensive documentation 

Ant primarily used for java builds and various files system tasks 

Make – the original – portable and language – independent  

Gradle and Maven 

Both are expandable and maintainable build tools 

Maven improved on Ant; Gradle incorporates benefits from both 

Make Example 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Ant Example 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif) 

Build Process 

Modern build tools provide reproducible tasks on demand 

Make was the beginning and is still used widely, especially for C/C++ 

Ant provided the first ‘modern’ build tool 

Maven and Gradle are the prevailing build tools for Java 

Intro to Make 

[https://www.gnu.org/software/make/](https://www.gnu.org/software/make/) 

GNU Make 

GNU Make is a tool which controls the generation of executables and other non-source files of a program from the program's source files.  

Make gets its knowledge of how to build your program from a file called the makefile, which lists each of the non-source files and how to compute it from other files. When you write a program, you should write a makefile for it, so that it is possible to use Make to build and install the program. 

Capabilities of Make 

* Make enables the end user to build and install your package without knowing the details of how that is done -- because these details are recorded in the makefile that you supply.  
* Make figures out automatically which files it needs to update, based on which source files have changed. It also automatically determines the proper order for updating files, in case one non-source file depends on another non-source file. 

As a result, if you change a few source files and then run Make, it does not need to recompile all of your program. It updates only those non-source files that depend directly or indirectly on the source files that you changed.  

* Make is not limited to any particular language. For each non-source file in the program, the makefile specifies the shell commands to compute it. These shell commands can run a compiler to produce an object file, the linker to produce an executable, ar to update a library, or TeX or Makeinfo to format documentation.  
* Make is not limited to building a package. You can also use Make to control installing or deinstalling a package, generate tags tables for it, or anything else you want to do often enough to make it worth while writing down how to do it.  

Make Rules and Targets 

A rule in the makefile tells Make how to execute a series of commands in order to build a target file from source files. It also specifies a list of dependencies of the target file. This list should include all files \(whether source files or other targets\) which are used as inputs to the commands in the rule.  

Here is what a simple rule looks like:  

target:   dependencies ... 

          commands 

          ... 

When you run Make, you can specify particular targets to update; otherwise, Make updates the first target listed in the makefile. Of course, any other target files needed as input for generating these targets must be updated first.  

Make uses the makefile to figure out which target files ought to be brought up to date, and then determines which of them actually need to be updated. If a target file is newer than all of its dependencies, then it is already up to date, and it does not need to be regenerated. The other target files do need to be updated, but in the right order: each target file must be regenerated before it is used in regenerating other targets.  

Advantages of GNU Make 

GNU Make has many powerful features for use in makefiles, beyond what other Make versions have. It can also regenerate, use, and then delete intermediate files which need not be saved.  

GNU Make also has a few simple features that are very convenient. For example, the -o file option which says \`\`pretend that source file file has not changed, even though it has changed.'' This is extremely useful when you add a new macro to a header file. Most versions of Make will assume they must therefore recompile all the source files that use the header file; but GNU Make gives you a way to avoid the recompilation, in the case where you know your change to the header file does not require it.  

However, the most important difference between GNU Make and most versions of Make is that GNU Make is free software.  

Makefiles And Conventions 

We have developed conventions for how to write Makefiles, which all GNU packages ought to follow. It is a good idea to follow these conventions in your program even if you don't intend it to be GNU software, so that users will be able to build your package just like many other packages, and will not need to learn anything special before doing so.  

These conventions are found in the chapter [\`\`Makefile conventions'' \(147 k characters\)](https://www.gnu.org/prep/standards/html_node/Makefile-Conventions.html#Makefile-Conventions) of the [GNU Coding Standards \(147 k characters\)](https://www.gnu.org/prep/standards.html).  

Downloading Make 

Make can be found on the main GNU ftp server: [http://ftp.gnu.org/gnu/make/](http://ftp.gnu.org/gnu/make/) \(via HTTP\) and [ftp://ftp.gnu.org/gnu/make/](ftp://ftp.gnu.org/gnu/make/) \(via FTP\). It can also be found on the [GNU mirrors](https://www.gnu.org/prep/ftp.html); please [use a mirror](http://ftpmirror.gnu.org/make/) if possible. 

Documentation 

[Documentation for Make](https://www.gnu.org/software/make/manual/) is available online, as is [documentation for most GNU software](https://www.gnu.org/manual/). You may also find more information about Make by running info make orman make, or by looking at /usr/share/doc/make/, /usr/local/doc/make/, or similar directories on your system. A brief summary is available by running make --help. 

Mailing lists 

Make has the following mailing lists: 

* [bug-make](https://lists.gnu.org/mailman/listinfo/bug-make) is used to discuss most aspects of Make, including development and enhancement requests, as well as bug reports. 
* [help-make](https://lists.gnu.org/mailman/listinfo/help-make) is for general user help and discussion. 

Announcements about Make and most other GNU software are made on [info-gnu](http://lists.gnu.org/mailman/listinfo/info-gnu) \([archive](http://lists.gnu.org/archive/html/info-gnu/)\). 

Security reports that should not be made immediately public can be sent directly to the maintainer. If there is no response to an urgent issue, you can escalate to the general[security](http://lists.gnu.org/mailman/listinfo/security) mailing list for advice. 

Getting involved 

Development of Make, and GNU in general, is a volunteer effort, and you can contribute. For information, please read [How to help GNU](https://www.gnu.org/help/). If you'd like to get involved, it's a good idea to join the discussion mailing list \(see above\). 

Test releases 

Trying the latest test release \(when available\) is always appreciated. Test releases of Make can be found at [http://alpha.gnu.org/gnu/make/](http://alpha.gnu.org/gnu/make/) \(via HTTP\) and[ftp://alpha.gnu.org/gnu/make/](ftp://alpha.gnu.org/gnu/make/) \(via FTP\). 

Development 

For development sources, issue trackers, and other information, please see the [Make project page](http://savannah.gnu.org/projects/make/) at [savannah.gnu.org](http://savannah.gnu.org/). 

Translating Make 

To translate Make's messages into other languages, please see the [Translation Project page for Make](http://translationproject.org/domain/make.html). If you have a new translation of the message strings, or updates to the existing strings, please have the changes made in this repository. Only translations from this site will be incorporated into Make. For more information, see the [Translation Project](http://translationproject.org/html/welcome.html). 

Maintainer 

Make is currently being maintained by Paul Smith. Please use the mailing lists for contact. 

A third-party analysis of Apache Ant. 

[https://www.softwaretestinghelp.com/apache-ant-selenium-tutorial-23/](https://www.softwaretestinghelp.com/apache-ant-selenium-tutorial-23/) 

A quick look at Ant and Maven, with a much longer view into Gradle. 

[https://www.journaldev.com/7971/gradle](https://www.journaldev.com/7971/gradle) 

Gradle is a project build and automation tool for java based applications; something like ivy, ant and maven. Build tools help us to reduce our development and test time and hence increase productivity. 

Table of Contents\[[hide](https://www.journaldev.com/7971/gradle)\] 

* [1 Gradle](https://www.journaldev.com/7971/gradle#gradle) 
* [1.1 Drawbacks of Ant](https://www.journaldev.com/7971/gradle#drawbacks-of-ant) 
* [1.2 Advantages of Maven](https://www.journaldev.com/7971/gradle#advantages-of-maven) 
* [1.3 Drawbacks of Maven](https://www.journaldev.com/7971/gradle#drawbacks-of-maven) 
* [1.4 What is Gradle?](https://www.journaldev.com/7971/gradle#what-is-gradle) 
* [1.5 Gradle advantages](https://www.journaldev.com/7971/gradle#gradle-advantages) 
* [1.6 Why we need to choose Gradle?](https://www.journaldev.com/7971/gradle#why-we-need-to-choose-gradle) 
* [1.7 What is Gradle’s Motto?](https://www.journaldev.com/7971/gradle#what-is-gradles-motto) 
* [1.8 Gradle Install](https://www.journaldev.com/7971/gradle#gradle-install) 

Gradle 

Grunt and Gulp are two popular build and automation tools for javascript projects like NodeJS or jQuery. Gant is a build tool mainly used for Groovy based applications. SBT stands for Scala Build Tool. SBT is mainly used for Scala based applications. 

Play 

Unmute 

Loaded: 34.61% 

Remaining Time -10:05 

Fullscreen 

![Shape VDO.AI](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACEAAAAhCAYAAABX5MJvAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAA7SURBVFhH7c6xDcAwDMAw//90gxTRDV7ISaPmWzbX6zUmYiImYiImYiImYiImYiImYiImYiIm8k/smzni2/DiyCw3zQAAAABJRU5ErkJgggAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==)

Skip Ad 

Now-a-days, most of the java projects are using either maven or gradle build tools because of their benefits when compared to ant. 

Before discussing about Gradle, first we will go through some shortcomings of ant and maven. Then we will discuss about why we need Gradle build tool to our projects. 

Drawbacks of Ant 

The following are main drawbacks of using ant build tools in our project. 

1. We need to write ant build scripts using XML. If we want to automate a complex project, then we need to write a lot of logic in XML files. 
2. When we execute complex and large project’s ant build, it produces a lot of verbose at console. 
3. There is no built-in ant project structure. Since we can use any build structure for our projects, new developers find it hard to understand the project struct and build scripts. 
4. It is very tough to write some complex logic using if-then-else statements. 
5. We need to maintain all jars with required version in version control. There is no support for dependency management. 

Because of these many drawbacks, now-a-days most of the projects have restructured and they are using maven build tool. Even though Maven provides the following benefits compare to ant, but still it has some drawbacks. 

Advantages of Maven 

1. Maven is an expressive, declarative, and maintainable build tool. 
2. All maven projects follow pre-defined structure. Even new developers find it easy to understand the project structure and start development quickly. 
3. We don’t need to maintain all jars with required version in version control. Maven will download all required jars at build time. Maven support for dependency management is one of the best advantage it has over ant. 
4. Maven gives us very modularized project structure. 

Drawbacks of Maven 

1. Maven follows some pre-defined build and automation lifecycle. Sometimes it may not fit to our project needs. 
2. Even though we can write custom maven life cycle methods, but it’s a bit tough and verbose. 
3. Maven build scripts are a bit tough to maintain for very complex projects. 

Maven has solved most of the ant build tool issues, but still it has some drawbacks. To overcome these issues, we need to use Gradle build tool. Now we can start our discussion on Gradle. 

What is Gradle? 

Gradle is an opensource build and automation tool for java based projects. Using Gradle, we can reduce project development time and increase productivity. 

Gradle is a multi-language, multi-platform, multi-project and multi-channel build and automation software. 

Gradle advantages 

Gradle will provide the following advantages compared to ant and maven. That’s why all new projects are using Gradle as build tool. 

1. Like Maven, Gradle is also an expressive, declarative, and maintainable build Tool. 
2. Just like maven, Gradle also supports dependency management. 
3. Gradle provides very scalable and high-performance builds. 
4. Gradle provides standard project layout and lifecycle, but it’s full flexibility. We have the option to fully configure the defaults. This is where it’s better than maven. 
5. It’s very easy to use gradle tool and implement custom logic in our project. 
6. Gradle supports the project structure that consists of more than one project to build deliverable. 
7. It is very easy to integrate existing ant/maven project with Gradle. 
8. It is very easy to migrate from existing ant/maven project to Gradle. 

Gradle combines most of the popular build tool plus points into a single build tool. 

In simple terminology, Gradle is built by taking all the good things from ant, maven, ivy and gant. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

That means Gradle combines best features of all popular build tools: 

* Ivy and ant power and flexibility 
* Maven’s easy to use, lifecycle management and dependency management 
* Gant’s build scripts 

NOTE: Gant is a Groovy based build system that internally uses ant tasks. In Gant, we need to write build scripts in Groovy, but no XML. Refer it’s [official website](https://gant.github.io/) for more information. 

Why we need to choose Gradle? 

1. Gradle’s build scripts are more readable, expressive and declarative. 
2. Gradle’s build scripts are written in simple Groovy, no XML. That means it use it’s own DSL based on Groovy script. 
3. It’s highly scalable for complex multi-module projects. 
4. Unlike Maven’s pom.xml, No need to write boilerplate XML Code 
5. It provides plugins for most of the IDEs like Eclipse, IntelliJ IDEA, Spring STS Suite etc. 
6. It is very easy to maintain even for multi-module complex projects. 

What is Gradle’s Motto? 

“Make the impossible possible, make the possible easy, and make the easy elegant”. 

By reading the Gradle’s Motto, we can understand that main goal and advantages of Gradle build tool. 

As of now, Gradle works as build and automation tool for the following projects. 

* Java/Scala/Groovy Based Projects 
* Android Projects 
* C/C++ Projects 
* JavaScript Based Projects 

Now we are clear that Gradle is the best build and automation tool to use in our projects. We are going to use Gradle in my [Spring Boot Tutorial](https://www.journaldev.com/7969/spring-boot-tutorial). As of today, Gradle’s latest and stable version is 4.1 released on 07-Aug-2017. We are going to use this version to run our examples. 

Gradle official website: [https://gradle.org/](https://gradle.org/) 

Gradle Install 

Please follow the following steps to install Gradle in Windows systems. 

1. Download latest Gradle software from https://gradle.org/ by clicking “Download Gradle 2.4” button as shown below 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Once download is successfully, we can observe a zip file as shown below 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

1. Extract zip file into local file system 

Observe Gradle Home directory: 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Observe Gradle BIN directory: 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

1. Set the following System Variables 

set GRADLE\_HOME=D:\gradle-2.4   
set PATH=D:\gradle-2.4\bin;%PATH% 

1. Open CMD Prompt and check the Setup is done successfully or not. 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

We can use either of the following two commands to know the Gradle version. 

D:\&gt;gradle -v 

Or 

D:\&gt;gradle --version 

By observing this output at Command Prompt as shown in above screenshot, we can say that Gradle installation is successful. 

A good comparison of the three tools, including some code examples 

[https://technologyconversations.com/2014/06/18/build-tools/](https://technologyconversations.com/2014/06/18/build-tools/) 

Test Selection 

Overall Goal – Select the minimum number of tests which identify defects better than random testing 

Definitions 

Test case 

Test data 

Test suite 

SUT 

Actual output 

Expected output 

Oracle 

Code Coverage 

Manual testing 

Automated testing 

Test Selection 

Test Adequacy 

Who should select tests? 

Developer: 

* Understands the system 
* Will test it gently 
* Driven by deadlines 

Tester: 

* Must learn the system 
* Will attempt to break it 
* Driven by ‘quality’ 

Numerous Approaches 

Manual testing 

Exception testing 

Boundary testing 

Randomized testing 

Coverage testing 

Requirements testing 

Specification testing 

Safety testing 

Security testing 

Performance testing 

Randomized testing 

Using randomized input values to identify defects in isolated code 

Works quite well in finding defects 

Automation of test generation allows many random tests to be run 

Code Coverage 

Using coverage metrics to identify code not covered 

Helps discover use cases and execution paths missed in test planning 

Generate tests cases to meet coverage criteria 

Requirements Testing 

End to end tests which highlight common and important user actions 

Written without knowledge of code structure 

Helps determine when you are ‘done’ 

Much more info… 

Just a few examples of test selection approaches 

Many of those listed have more in-depth lectures 

See Coursera courses in software testing 

Test Selection 

Finding the smallest number of tests that find the most defects 

Variety of methods, many of them using automated means 

Can be used together eg. randomized coverage testing 

Significant research in the area is on-going 

More specific definition and discussion of code coverage. 

[https://www.guru99.com/code-coverage.html](https://www.guru99.com/code-coverage.html) 

Why use Code Coverage 

* It helps you to measure the efficiency of test implementation 
* It offers a quantitative measurement.  
* It defines the degree to which the source code has been tested. 

Code Coverage Methods 

Following are major code coverage methods  

* Statement Coverage 
* Decision Coverage 
* Branch Coverage 
* Toggle Coverage 
* FSM Coverage  

Statement Coverage 

What is Statement Coverage?  

Statement coverage is a white box test design technique which involves execution of all the executable statements in the source code at least once. It is used to calculate and measure the number of statements in the source code which can be executed given the requirements.  

Statement coverage is used to derive scenario based upon the structure of the code under test.  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

In [White Box Testing](https://www.guru99.com/white-box-testing.html), the tester is concentrating on how the software works. In other words, the tester will be concentrating on the internal working of source code concerning control flow graphs or flow charts.  

Generally in any software, if we look at the source code, there will be a wide variety of elements like operators, functions, looping, exceptional handlers, etc. Based on the input to the program, some of the code statements may not be executed. The goal of Statement coverage is to cover all the possible path's, line, and statement in the code.  

Let's understand this with an example, how to calculate statement coverage.  

Scenario to calculate Statement Coverage for given source code. Here we are taking two different scenarios to check the percentage of statement coverage for each scenario.  

Source Code: 

Prints \(int a, int b\) {                       ------------  Printsum is a function  

    int result = a+ b;  

    If \(result&gt; 0\) 

    Print \("Positive", result\) 

    Else 

    Print \("Negative", result\) 

    }                                        -----------   End of the source code  

Scenario 1: 

If A = 3, B = 9  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

The statements marked in yellow color are those which are executed as per the scenario  

Number of executed statements = 5, Total number of statements = 7  

Statement Coverage: 5/7 = 71%  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Likewise we will see scenario 2,  

Scenario 2: 

If A = -3, B = -9  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

The statements marked in yellow color are those which are executed as per the scenario.  

Number of executed statements = 6  

Total number of statements = 7  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Statement Coverage: 6/7 = 85%  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

But overall if you see, all the statements are being covered by 2nd scenario's considered. So we can conclude that overall statement coverage is 100%.  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

What is covered by Statement Coverage? 

1. Unused Statements 
2. Dead Code 
3. Unused Branches 
4. Missing Statements 

Decision Coverage 

Decision coverage reports the true or false outcomes of each Boolean expression. In this coverage, expressions can sometimes get complicated. Therefore, it is very hard to achieve 100% coverage.  

That's why there are many different methods of reporting this metric. All these methods focus on covering the most important combinations. It is very much similar to decision coverage, but it offers better sensitivity to control flow.  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Example of decision coverage 

Consider the following code-  

Demo\(int a\) {                        

     If \(a&gt; 5\) 

    a=a\*3 

     Print \(a\) 

    } 

Scenario 1: 

Value of a is 2  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

The code highlighted in yellow will be executed. Here the "No" outcome of the decision If \(a&gt;5\) is checked.  

Decision Coverage = 50%  

Scenario 2: 

Value of a is 6  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

The code highlighted in yellow will be executed. Here the "Yes" outcome of the decision If \(a&gt;5\) is checked.  

Decision Coverage = 50%  

| Test Case   | Value of A   | Output   | Decision Coverage   |
| :--- | :--- | :--- | :--- |
| 1   | 2   | 2   | 50%   |
| 2   | 6   | 18   | 50%   |

Branch Coverage 

In the branch coverage, every outcome from a code module is tested. For example, if the outcomes are binary, you need to test both True and False outcomes.  

It helps you to ensure that every possible branch from each decision condition is executed at least a single time.  

By using Branch coverage method, you can also measure the fraction of independent code segments. It also helps you to find out which is sections of code don't have any branches.  

The formula to calculate Branch Coverage:  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Example of Branch Coverage 

To learn branch coverage, let's consider the same example used earlier 

Consider the following code  

Demo\(int a\) {                        

     If \(a&gt; 5\) 

    a=a\*3 

     Print \(a\) 

    }                                        

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Branch Coverage will consider unconditional branch as well  

| Test Case   | Value of A   | Output   | Decision Coverage   | Branch Coverage   |
| :--- | :--- | :--- | :--- | :--- |
| 1   | 2   | 2   | 50%   | 33%  |
| 2   | 6   | 18   | 50%   | 67%  |

Advantages of Branch coverage: 

Branch coverage Testing offers the following advantages:  

* Allows you to validate-all the branches in the code  
* Helps you to ensure that no branched lead to any abnormality of the program's operation  
* Branch coverage method removes issues which happen because of statement coverage testing  
* Allows you to find those areas which are not tested by other testing methods 
* It allows you to find a quantitative measure of code coverage  
* Branch coverage ignores branches inside the Boolean expressions  

Condition Coverage 

Conditional coverage or expression coverage will reveal how the variables or subexpressions in the conditional statement are evaluated. In this coverage expressions with logical operands are only considered.  

For example, if an expression has Boolean operations like AND, OR, XOR, which indicated total possibilities.  

Conditional coverage offers better sensitivity to the control flow than decision coverage. Condition coverage does not give a guarantee about full decision coverage  

The formula to calculate Condition Coverage:  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Example:  

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

For the above expression, we have 4 possible combinations  

* TT 
* FF 
* TF 
* FT 

Consider the following input  

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>X=3&#x202F;</p>
        <p>Y=4&#x202F;</p>
      </th>
      <th style="text-align:left">(x&lt;y)&#x202F;</th>
      <th style="text-align:left">TRUE&#x202F;</th>
      <th style="text-align:left">Condition Coverage is &#xBC; = 25%&#x202F;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>A=3&#x202F;</p>
        <p>B=4&#x202F;</p>
      </td>
      <td style="text-align:left">(a&gt;b)&#x202F;</td>
      <td style="text-align:left">FALSE&#x202F;</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

Finite State Machine Coverage 

Finite state machine coverage is certainly the most complex type of code coverage method. This is because it works on the behavior of the design. In this coverage method, you need to look for how many time-specific states are visited, transited. It also checks how many sequences are included in a finite state machine.  

Which Type of Code Coverage to Choose 

This is certainly the most difficult answer to give. In order to select a coverage method, the tester needs to check that the  

* code under test has single or multiple undiscovered defects  
* cost of the potential penalty 
* cost of lost reputation  
* cost of lost sale, etc.  

The higher the probability that defects will cause costly production failures, the more severe the level of coverage you need to choose.  

Code Coverage vs. Functional Coverage 

| Code Coverage  | Functional Coverage  |
| :--- | :--- |
| Code coverage tells you how well the source code has been exercised by your test bench.   | Functional coverage measures how well the functionality of the design has been covered by your test bench.   |
| Never use a design specification   | Use design specification   |
| Done by developers   | Done by Testers   |

Code Coverage Tools 

Here, is a list of Important code coverage Tools:  

| Tool Name  | Description   |
| :--- | :--- |
| [Coco](https://bit.ly/2FLrNAS)  | It is an Cross-platform and cross-compiler code coverage analysis for C, C++, SystemC, C\#, Tcl and QML code. Automated measurement of test coverage of statements, branches and conditions. No changes to the application are necessary Learn more about [coco](https://bit.ly/2FLrNAS)  |
| Cobertura  | It is an open source code coverage tool. It measures test coverage by instrumenting a code base and analyze which lines of code are executing and which are not executed when the test suite runs.   |
| Clover  | Clover also reduces testng time by only running the tests which cover the application code which was modified since the previous build.   |
| DevPartner  | DevPartner enables developers to analyze Java code for Code Quality and Complexity.   |
| Emma  | EMMA supports class, method, line, and base block coverage, aggregated source file, class, and method levels.   |
| Kalistick  | Kalistick is a third party application which analyzes the codes with different perspectives.   |
| CoView and CoAnt  | Coding Software is a code coverage tool for metrics, mock object creation, code testability, path & branch coverage, etc.   |
| Bullseye for C++  | BulseyeCoverage is a code coverage tool for C++and C.   |
| Sonar  | Sonar is an open code coverage tool which helps you to manage code quality.   |

Advantages of Using Code Coverage  

* Helpful to evaluate a quantitative measure of code coverage  
* It allows you to create extra test cases to increase coverage 
* It allows you to find the areas of a program which is not exercised by a set of test cases 

Disadvantages of Using Code Coverage 

* Even when any specific feature is not implemented in design, code coverage still report 100% coverage. 
* It is not possible to determine whether we tested all possible values of a feature with the help of code coverage 
* Code coverage is also not telling how much and how well you have covered your logic  
* In the case when the specified function hasn't implemented, or a not included from the specification, then structure-based techniques cannot find that issue.  

Summary 

* Code coverage is a measure which describes the degree of which the source code of the program has been tested 
* It helps you to measure the efficiency of test implementation 
* Five Code Coverage methods are 1.\) Statement Coverage 2.\) Condition Coverage 3\) Branch Coverage 4\) Toggle Coverage 5\) FSM Coverage 
* Statement coverage involves execution of all the executable statements in the source code at least once 
* Decision coverage reports the true or false outcomes of each Boolean expression 
* In the branch coverage, every outcome from a code module is tested 
* Conditional will reveal how the variables or subexpressions in the conditional statement are evaluated 
* Finite state machine coverage is certainly the most complex type of code coverage method 
* In order to select a coverage method, the tester needs to check the cost of the potential penalty, lost reputation, lost sale, etc.  
* Code coverage tells you how well the source code has been exercised by your test bench while Functional coverage measures how well the functionality of the design has been covered  
* Cobertura, JTest, Clover, Emma, Kalistick are few important code coverage tools 
* Code Coverage allows you to create extra test cases to increase coverage 
* Code Coverage does not help you to determine whether we tested all possible values of a feature 

An example of how to calculate the MC/DC code coverage for a test suite. 

[https://www.verifysoft.com/en\_example\_mcdc.html](https://www.verifysoft.com/en_example_mcdc.html) 

Minimum Acceptable Code Coverage 

A variety of standards for the minimum acceptable code coverage for software in various regulated industries, based on the importance of the software to the continued safe operation of the product. 

After looking at some of these, I hope you appreciate the FDA standard as much as I do. 

[https://www.bullseye.com/minimum.html](https://www.bullseye.com/minimum.html) 

Summary 

Code coverage of 70-80% is a reasonable goal for system test of most projects with most coverage metrics. Use a higher goal for projects specifically organized for high testability or that have high failure costs. Minimum code coverage for unit testing can be 10-20% higher than for system testing. 

Introduction 

Empirical studies of real projects found that increasing code coverage above 70-80% is time consuming and therefore leads to a relatively slow bug detection rate. Your goal should depend on the risk assessment and economics of the project. Consider the following factors. 

* Cost of failure. Raise your goal for safety-critical systems or where the cost of a failure is high, such as products for the medical or automotive industries, or widely deployed products. 
* Resources. Lower your goal if testers are spread thin or inadequately trained. If your testers are unfamiliar with the application, they may not recognize a failure even if they cover the associated code. 
* Testable design. Raise your goal if your system has special provisions for testing such as a method for directly accessing internal functionality, bypassing the user interface. 
* Development cycle status. Lower your goal if you are maintaining a legacy system where the original design engineers are no longer available. 

Many projects set no particular minimum percentage required code coverage. Instead they use code coverage analysis only to save time. Measuring code coverage can quickly find those areas overlooked during test planning. 

Defer choosing a code coverage goal until you have some measurements in hand. Before measurements are available, testers often overestimate their code coverage by 20-30%. 

Full Coverage Generally Impractical 

Although 100% code coverage may appear like a best possible effort, even 100% code coverage is estimated to only expose about half the faults in a system. Low code coverage indicates inadequate testing, but high code coverage guarantees nothing. 

In a large system, achieving 100% code coverage is generally not cost effective. Some reasons are listed below. 

* Some test cases are expensive to reproduce but are highly improbable. The cost to benefit ratio does not justify repeating these tests simply to record the code coverage. 
* Checks may exist for unexpected error conditions. Layers of code might obscure whether errors in low-level code propagate up to higher level code. An engineer might decide that handling all errors creates a more robust solution than tracing the possible errors. 
* Unreachable code in the current version might become reachable in a future version. An engineer might address uncertainty about future development by investing a little more effort to add some capability that is not currently needed. 
* Code shared among several projects is only partially utilized by the project under test. 

Generally, the tester should stop increasing code coverage when the tests become contrived. When you focus more and more on making the coverage numbers better, your motivation shifts away from finding bugs. 

Unit, Integration and System Testing 

You can attain higher code coverage during unit testing than in integration testing or system testing. During unit testing, the tester has more facilities available, such as a debugger to manipulate data and conditional compilation to simulate error conditions. 

Likewise, higher code coverage is possible during integration testing than in system testing. During integration testing, the test harness often provides more precise control and capability than the system user interface. 

Therefore it makes sense to set progressively lower goals for unit testing, integration testing, and system testing. For example, 90% during unit testing, 80% during integration testing, and 70% during system testing. 

Coverage Metrics 

The information in this paper applies to code coverage metrics that consider control structures independently. Specifically, these are: 

* statement coverage \(line coverage\) 
* basic block coverage 
* decision coverage \(branch coverage\) 
* condition/decision coverage 
* modified condition/decision coverage \(MCDC\) 

Although some of these metrics are less sensitive to control flow than others, they all correlate statistically at a large scale. 

Formal Standards 

DO-178B 

The aviation standard DO-178B requires 100% code coverage for safety critical systems. This standard specifies progressively more sensitive code coverage metrics for more critical systems. 

| Effect of System Failure  | Level  | Example  | Required Code Coverage  |
| :--- | :--- | :--- | :--- |
| Catastrophic  | A  | Crash  | 100% modified condition/decision coverage and 100% statement coverage  |
| Hazardous  | B  | Passenger fatality  | 100% decision coverage and 100% statement coverage  |
| Major  | C  | Passenger injury  | 100% statement coverage  |
| Minor  | D  | Flight plan change  | No code coverage requirement  |
| No effect  | E  | Entertainment system failure  | No code coverage requirement  |

These requirements consider neither the probability of a failure nor the cost of performing test cases. 

IEC 61508 

The standard IEC 61508:2010 "Functional Safety of Electrical/Electronic/Programmable Electronic Safety-Related Systems" recommends 100% code coverage of several metrics, but the strenuousness of the recommendation relates to the criticality. 

| Safety Integrity Level  | 100% entry points  | 100% statements  | 100% branches  | 100% conditions, MC/DC  |
| :--- | :--- | :--- | :--- | :--- |
| 1 \(least critical\)  | Highly Recommended  | Recommended  | Recommended  | Recommended  |
| 2  | Highly Recommended  | Highly Recommended  | Recommended  | Recommended  |
| 3  | Highly Recommended  | Highly Recommended  | Highly Recommended  | Recommended  |
| 4 \(most critical\)  | Highly Recommended  | Highly Recommended  | Highly Recommended  | Highly Recommended  |

The safety integrity level \(SIL\) relates to the probability of unsafe failure. Determining the SIL involves a lengthy risk analysis. 

This standard recommends but does not require 100% coverage. It specifies you should explain any uncovered code. 

This standard does not define the coverage metrics and does not distinguish between condition coverage and MC/DC. 

ISO 26262 

ISO 26262:2011 "Road vehicles -- Functional safety" requires measuring code coverage, and specifies that if the level achieved "is considered insufficient", then a rationale must be provided. The standard recommends different coverage metrics for unit testing than for integration testing. In both cases, the strenuousness of the recommendations relates to the criticality. 

For unit testing, three coverage metrics are recommended, shown in the table below. The standard does not provide definitions for these metrics. 

| Methods  | ASIL  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| A \(least critical\)  | B  | C  | D \(most critical\)  |  |
| Statement coverage  | highly recommended  | highly recommended  | recommended  | recommended  |
| Branch coverage  | recommended  | highly recommended  | highly recommended  | highly recommended  |
| Modified Condition/Decision Coverage  | recommended  | recommended  | recommended  | highly recommended  |

For integration testing, two metrics are recommended, shown in the table below. 

| Methods  | ASIL  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| A \(least critical\)  | B  | C  | D \(most critical\)  |  |
| Function coverage  | recommended  | recommended  | highly recommended  | highly recommended  |
| Call coverage  | recommended  | recommended  | highly recommended  | highly recommended  |

The standard defines function coverage as the percentage of executed software functions, and call coverage as the percentage of executed software function calls. 

The automotive safety integrity level \(ASIL\) is based on the probability of failure, effect on vehicle controllability, and severity of harm. The ASIL does not correlate directly to the SIL of IEC 61508. 

The code coverage requirements are contained in part 6 "Product development at the software level." 

ANSI/IEEE 1008-1987 

The IEEE Standard for Software Unit Testing section 3.1.2 specifies 100% statement coverage as a completeness requirement. Section A9 recommends 100% branch coverage for code that is critical or has inadequate requirements specification. Although this document is quite old, it was reaffirmed in 2002. 

Test Adequacy 

Overall Goal – Determine whether a test suite is adequate to ensure the correctness or desired level of dependability that we want for our software\* 

* this is very difficult 
* in fact for correctness it is generally impossible 

Approximating adequacy 

Instead of measuting adequacy directly we measure how well we have covered some aspect of the 

* program structure 
* program inputs 
* requirements 
* etc 

This measurement provides a way to determine \(lack of\) thoroughness of a test suite 

Adequacy criteria 

Adequacy criterion = set of test obligations 

A test suite satisfies an adequacy criterion if 

* all the tests success \(pass\) 
* every test obligation in the criterion is satisfied by at least one of the test cases in the test suite 
* Example; 
* The statement coverage adequacy criterion is satisfied by test suite S for program P if; 
* Each executable statement in P is executed by at least one test case in S and 
* The outcome of each test execution was ‘pass’ 

What do we know when a criterion is satisfied? 

If a test suite satisfies all the obligations in the criterion we have some evidence of its thoroughness 

* We do not know definitively that it is an effective test suite 
* Different criteria can be more or less effective 

You would not buy a house just because it’s ‘up to code’ but you might avoid if it’s not 

Where do test obligations come from? 

Functional – from software specifications 

Example: if spec requires robust recovery from power failure, test obligations should include simulated power failure 

Fault based – from hypothesized faults \(common bugs\) 

Example: check for buffer overflow handling \(common vulnerability\) by testing on very large inputs 

Model based – from model of system 

Models used in specification or design or derived from code 

Example: exercise all transitions in communication protocol model 

Structural – white or glass box: from code 

Example: traverse each program loop one or more times 

Coverage: is it useful or harmful? 

Measuring Coverage 

% of satisfied test obligations can be useful 

* Progress toward a thorough test suite 
* Trouble spots requiring more attention 

Or a dangerous seduction 

* Coverage is only a proxy for thoroughness or adequacy 
* Its easy to improve coverage without improving a test suite \(much easier than designing good test cases\) 
* The only measure that really matters is \(cost\) effectiveness 

Comparing Adequacy Criteria 

Can we distinguish stronger from weaker adequacy criteria? 

Empirical approach: study the effectiveness of different approaches to testing in practice 

* Issue: depends on the setting 
* Cannot generalize from on organization or project to another 

Analytical approach: describe conditions under which one adequacy criterion is provably stronger than another 

* Stronger = gives stronger guarantees 
* One piece of the overall ‘effectiveness’ question 

Goals for adequacy Criterion 

Effective at finding faults; 

* Better than random testing for suites of the same size 
* Better than other metrics with suites of similar size 

Robust to simple changes in program / input structure 

Reasonable in terms of the number of required tests and coverage analysis 

Vast area of software engineering research 

Primer not sufficient to gain full understanding 

Several other resources exist in the space to develop further understanding 

Additional Coursera courses are offered 

Test Adequacy 

* How to define a notion of ‘thoroughness’ of a test suite 
* Defined in terms of covering some information 
* Derived from many sources both simple and sophisticated 
* Code coverage likely the most common such adequacy criteria 

Test Driven Deployment 

* Flips the standard approach of ‘write code, write tests for the code’ 
* By writing the tests first, you avoid some developer bias 
* Gives you a check to know when you are done 

Process 

* Add some test\(s\) to the test suits 
* Execute all tests in the suite and confirm new test\(s\) fail 
* Develop code to introduce new functionality 
* Execute all tests in the suite and confirm new test\(s\) pass 
* Refactor 

Tests up front 

Focus on what the code should do, not how it will be implemented 

Tests are not thrown together at the last minute 

‘test-first students on average wrote more tests and tended to be more productive’ 

Test Drive Development 

* Develop tests up front then code until tests pass 
* Building tests before implementation allows focus on behaviour 
* Allows for incremental status updates 
* Key feature of many Agile approaches 

Deployment 

Continuous Integration 

* Automating quality controls work through tools 
* Each process runs and reports whenever a developer completes an action 
* Live reports give managers and developers visualization of quality 

Jenkins 

* The big player in continuous integration and automation servers 
* Plug ins determine the capabilities of the server 
* One of the readings is a link to more information on the Jenkins Pipeline 

Continuous Integration \(CI\) 

* Automated processes designed to aid post developments tasks 
* Automated testing allows for rejection of commits 
* Tasks could include code style checking, static analysis and more 
* Led to further improvements of the post dev process 

Jenkins – Getting Started 

[https://jenkins.io/doc/pipeline/tour/getting-started/](https://jenkins.io/doc/pipeline/tour/getting-started/) 

Getting started with the Guided Tour  

This guided tour introduces you to the basics of using Jenkins and its main feature, Jenkins Pipeline. This tour uses the "standalone" Jenkins distribution, which runs locally on your own machine. 

Prerequisites 

For this tour, you will require: 

* A machine with: 
* 256 MB of RAM, although more than 512MB is recommended 
* 10 GB of drive space \(for Jenkins and your Docker image\) 
* The following software installed: 
* Java 8 or 11 \(either a JRE or Java Development Kit \(JDK\) is fine\) 
* [Docker](https://docs.docker.com/) \(navigate to Get Docker at the top of the website to access the Docker download that’s suitable for your platform\) 

Download and run Jenkins 

1. [Download Jenkins](http://mirrors.jenkins.io/war-stable/latest/jenkins.war). 
2. Open up a terminal in the download directory. 
3. Run java -jar jenkins.war --httpPort=8080. 
4. Browse to http://localhost:8080. 
5. Follow the instructions to complete the installation. 

When the installation is complete, you can start putting Jenkins to work! 

Jenkins Pipeline 

[https://jenkins.io/doc/book/pipeline/](https://jenkins.io/doc/book/pipeline/) 

Pipeline  

Chapter Sub-Sections 

* [Getting started with Pipeline](https://www.jenkins.io/doc/book/pipeline/getting-started) 
* [Using a Jenkinsfile](https://www.jenkins.io/doc/book/pipeline/jenkinsfile) 
* [Running Pipelines](https://www.jenkins.io/doc/book/pipeline/running-pipelines) 
* [Branches and Pull Requests](https://www.jenkins.io/doc/book/pipeline/multibranch) 
* [Using Docker with Pipeline](https://www.jenkins.io/doc/book/pipeline/docker) 
* [Extending with Shared Libraries](https://www.jenkins.io/doc/book/pipeline/shared-libraries) 
* [Pipeline Development Tools](https://www.jenkins.io/doc/book/pipeline/development) 
* [Pipeline Syntax](https://www.jenkins.io/doc/book/pipeline/syntax) 
* [Pipeline Best Practices](https://www.jenkins.io/doc/book/pipeline/pipeline-best-practices) 
* [Scaling Pipelines](https://www.jenkins.io/doc/book/pipeline/scaling-pipeline) 
* [Pipeline CPS Method Mismatches](https://www.jenkins.io/doc/book/pipeline/cps-method-mismatches) 

Table of Contents 

* [What is Jenkins Pipeline?](https://www.jenkins.io/doc/book/pipeline/#overview) 
* [Declarative versus Scripted Pipeline syntax](https://www.jenkins.io/doc/book/pipeline/#declarative-versus-scripted-pipeline-syntax) 
* [Why Pipeline?](https://www.jenkins.io/doc/book/pipeline/#why) 
* [Pipeline concepts](https://www.jenkins.io/doc/book/pipeline/#pipeline-concepts) 
* [Pipeline](https://www.jenkins.io/doc/book/pipeline/#pipeline) 
* [Node](https://www.jenkins.io/doc/book/pipeline/#node) 
* [Stage](https://www.jenkins.io/doc/book/pipeline/#stage) 
* [Step](https://www.jenkins.io/doc/book/pipeline/#step) 
* [Pipeline syntax overview](https://www.jenkins.io/doc/book/pipeline/#pipeline-syntax-overview) 
* [Declarative Pipeline fundamentals](https://www.jenkins.io/doc/book/pipeline/#declarative-pipeline-fundamentals) 
* [Scripted Pipeline fundamentals](https://www.jenkins.io/doc/book/pipeline/#scripted-pipeline-fundamentals) 
* [Pipeline example](https://www.jenkins.io/doc/book/pipeline/#pipeline-example) 

This chapter covers all recommended aspects of Jenkins Pipeline functionality, including how to: 

* [get started with Pipeline](https://www.jenkins.io/doc/book/pipeline/getting-started) - covers how to [define a Jenkins Pipeline](https://www.jenkins.io/doc/book/pipeline/getting-started#defining-a-pipeline) \(i.e. your Pipeline\) through [Blue Ocean](https://www.jenkins.io/doc/book/pipeline/getting-started#through-blue-ocean), through the[classic UI](https://www.jenkins.io/doc/book/pipeline/getting-started#through-the-classic-ui) or in [SCM](https://www.jenkins.io/doc/book/pipeline/getting-started#defining-a-pipeline-in-scm), 
* [create and use a Jenkinsfile](https://www.jenkins.io/doc/book/pipeline/jenkinsfile) - covers use-case scenarios on how to craft and construct your Jenkinsfile, 
* work with [branches and pull requests](https://www.jenkins.io/doc/book/pipeline/multibranch), 
* [use Docker with Pipeline](https://www.jenkins.io/doc/book/pipeline/docker) - covers how Jenkins can invoke Docker containers on agents/nodes \(from a Jenkinsfile\) to build your Pipeline projects, 
* [extend Pipeline with shared libraries](https://www.jenkins.io/doc/book/pipeline/shared-libraries), 
* use different [development tools](https://www.jenkins.io/doc/book/pipeline/development) to facilitate the creation of your Pipeline, and 
* work with [Pipeline syntax](https://www.jenkins.io/doc/book/pipeline/syntax) - this page is a comprehensive reference of all Declarative Pipeline syntax. 

For an overview of content in the Jenkins User Handbook, see [User Handbook overview](https://www.jenkins.io/doc/book/pipeline/getting-started). 

What is Jenkins Pipeline? 

Jenkins Pipeline \(or simply "Pipeline" with a capital "P"\) is a suite of plugins which supports implementing and integrating continuous delivery pipelines into Jenkins. 

A continuous delivery \(CD\) pipeline is an automated expression of your process for getting software from version control right through to your users and customers. Every change to your software \(committed in source control\) goes through a complex process on its way to being released. This process involves building the software in a reliable and repeatable manner, as well as progressing the built software \(called a "build"\) through multiple stages of testing and deployment. 

Pipeline provides an extensible set of tools for modeling simple-to-complex delivery pipelines "as code" via the[Pipeline domain-specific language \(DSL\) syntax](https://www.jenkins.io/doc/book/pipeline/syntax). \[[1](https://www.jenkins.io/doc/book/pipeline/#_footnotedef_1)\] 

The definition of a Jenkins Pipeline is written into a text file \(called a [Jenkinsfile](https://www.jenkins.io/doc/book/pipeline/jenkinsfile)\) which in turn can be committed to a project’s source control repository. \[[2](https://www.jenkins.io/doc/book/pipeline/#_footnotedef_2)\] This is the foundation of "Pipeline-as-code"; treating the CD pipeline a part of the application to be versioned and reviewed like any other code. 

Creating a Jenkinsfile and committing it to source control provides a number of immediate benefits: 

* Automatically creates a Pipeline build process for all branches and pull requests. 
* Code review/iteration on the Pipeline \(along with the remaining source code\). 
* Audit trail for the Pipeline. 
* Single source of truth \[[3](https://www.jenkins.io/doc/book/pipeline/#_footnotedef_3)\] for the Pipeline, which can be viewed and edited by multiple members of the project. 

While the syntax for defining a Pipeline, either in the web UI or with a Jenkinsfile is the same, it is generally considered best practice to define the Pipeline in a Jenkinsfile and check that in to source control. 

Declarative versus Scripted Pipeline syntax 

A Jenkinsfile can be written using two types of syntax - Declarative and Scripted. 

Declarative and Scripted Pipelines are constructed fundamentally differently. Declarative Pipeline is a more recent feature of Jenkins Pipeline which: 

* provides richer syntactical features over Scripted Pipeline syntax, and 
* is designed to make writing and reading Pipeline code easier. 

Many of the individual syntactical components \(or "steps"\) written into a Jenkinsfile, however, are common to both Declarative and Scripted Pipeline. Read more about how these two types of syntax differ in [Pipeline concepts](https://www.jenkins.io/doc/book/pipeline/#pipeline-concepts) and [Pipeline syntax overview](https://www.jenkins.io/doc/book/pipeline/#pipeline-syntax-overview) below. 

Why Pipeline? 

Jenkins is, fundamentally, an automation engine which supports a number of automation patterns. Pipeline adds a powerful set of automation tools onto Jenkins, supporting use cases that span from simple continuous integration to comprehensive CD pipelines. By modeling a series of related tasks, users can take advantage of the many features of Pipeline: 

* Code: Pipelines are implemented in code and typically checked into source control, giving teams the ability to edit, review, and iterate upon their delivery pipeline. 
* Durable: Pipelines can survive both planned and unplanned restarts of the Jenkins master. 
* Pausable: Pipelines can optionally stop and wait for human input or approval before continuing the Pipeline run. 
* Versatile: Pipelines support complex real-world CD requirements, including the ability to fork/join, loop, and perform work in parallel. 
* Extensible: The Pipeline plugin supports custom extensions to its DSL \[[1](https://www.jenkins.io/doc/book/pipeline/#_footnotedef_1)\] and multiple options for integration with other plugins. 

While Jenkins has always allowed rudimentary forms of chaining Freestyle Jobs together to perform sequential tasks, \[[4](https://www.jenkins.io/doc/book/pipeline/#_footnotedef_4)\] Pipeline makes this concept a first-class citizen in Jenkins. 

Building on the core Jenkins value of extensibility, Pipeline is also extensible both by users with [Pipeline Shared Libraries](https://www.jenkins.io/doc/book/pipeline/shared-libraries) and by plugin developers. \[[5](https://www.jenkins.io/doc/book/pipeline/#_footnotedef_5)\] 

The flowchart below is an example of one CD scenario easily modeled in Jenkins Pipeline: 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Pipeline concepts 

The following concepts are key aspects of Jenkins Pipeline, which tie in closely to Pipeline syntax \(see the [overview](https://www.jenkins.io/doc/book/pipeline/%22%20/l%20%22pipeline-syntax-overview)below\). 

Pipeline 

A Pipeline is a user-defined model of a CD pipeline. A Pipeline’s code defines your entire build process, which typically includes stages for building an application, testing it and then delivering it. 

Also, a pipeline block is a [key part of Declarative Pipeline syntax](https://www.jenkins.io/doc/book/pipeline/#declarative-pipeline-fundamentals). 

Node 

A node is a machine which is part of the Jenkins environment and is capable of executing a Pipeline. 

Also, a node block is a [key part of Scripted Pipeline syntax](https://www.jenkins.io/doc/book/pipeline/#scripted-pipeline-fundamentals). 

Stage 

A stage block defines a conceptually distinct subset of tasks performed through the entire Pipeline \(e.g. "Build", "Test" and "Deploy" stages\), which is used by many plugins to visualize or present Jenkins Pipeline status/progress.\[[6](https://www.jenkins.io/doc/book/pipeline/#_footnotedef_6)\] 

Step 

A single task. Fundamentally, a step tells Jenkins what to do at a particular point in time \(or "step" in the process\). For example, to execute the shell command make use the sh step: sh 'make'. When a plugin extends the Pipeline DSL, \[[1](https://www.jenkins.io/doc/book/pipeline/#_footnotedef_1)\] that typically means the plugin has implemented a new step. 

Pipeline syntax overview 

The following Pipeline code skeletons illustrate the fundamental differences between [Declarative Pipeline syntax](https://www.jenkins.io/doc/book/pipeline/#declarative-pipeline-fundamentals)and [Scripted Pipeline syntax](https://www.jenkins.io/doc/book/pipeline/#scripted-pipeline-fundamentals). 

Be aware that both [stages](https://www.jenkins.io/doc/book/pipeline/#stage) and [steps](https://www.jenkins.io/doc/book/pipeline/#step) \(above\) are common elements of both Declarative and Scripted Pipeline syntax. 

Declarative Pipeline fundamentals 

In Declarative Pipeline syntax, the pipeline block defines all the work done throughout your entire Pipeline. 

Jenkinsfile \(Declarative Pipeline\) 

pipeline { 

    agent any  

    stages { 

        stage\('Build'\) {  

            steps { 

                //  

            } 

        } 

        stage\('Test'\) {  

            steps { 

                //  

            } 

        } 

        stage\('Deploy'\) {  

            steps { 

                //  

            } 

        } 

    } 

} 

|  | Execute this Pipeline or any of its stages, on any available agent.  |
| :--- | :--- |
|  | Defines the "Build" stage.  |
|  | Perform some steps related to the "Build" stage.  |
|  | Defines the "Test" stage.  |
|  | Perform some steps related to the "Test" stage.  |
|  | Defines the "Deploy" stage.  |
|  | Perform some steps related to the "Deploy" stage.  |

Scripted Pipeline fundamentals 

In Scripted Pipeline syntax, one or more node blocks do the core work throughout the entire Pipeline. Although this is not a mandatory requirement of Scripted Pipeline syntax, confining your Pipeline’s work inside of a node block does two things: 

1. Schedules the steps contained within the block to run by adding an item to the Jenkins queue. As soon as an executor is free on a node, the steps will run. 
2. Creates a workspace \(a directory specific to that particular Pipeline\) where work can be done on files checked out from source control.  Caution: Depending on your Jenkins configuration, some workspaces may not get automatically cleaned up after a period of inactivity. See tickets and discussion linked from [JENKINS-2111](https://issues.jenkins-ci.org/browse/JENKINS-2111) for more information. 

Jenkinsfile \(Scripted Pipeline\) 

node {   

    stage\('Build'\) {  

        //  

    } 

    stage\('Test'\) {  

        //  

    } 

    stage\('Deploy'\) {  

        //  

    } 

} 

|  | Execute this Pipeline or any of its stages, on any available agent.  |
| :--- | :--- |
|  | Defines the "Build" stage. stage blocks are optional in Scripted Pipeline syntax. However, implementing stageblocks in a Scripted Pipeline provides clearer visualization of each \`stage’s subset of tasks/steps in the Jenkins UI.  |
|  | Perform some steps related to the "Build" stage.  |
|  | Defines the "Test" stage.  |
|  | Perform some steps related to the "Test" stage.  |
|  | Defines the "Deploy" stage.  |
|  | Perform some steps related to the "Deploy" stage.  |

Pipeline example 

Here is an example of a Jenkinsfile using Declarative Pipeline syntax - its Scripted syntax equivalent can be accessed by clicking the Toggle Scripted Pipeline link below: 

Jenkinsfile \(Declarative Pipeline\) 

pipeline {  

    agent any  

    options { 

        skipStagesAfterUnstable\(\) 

    } 

    stages { 

        stage\('Build'\) {  

            steps {  

                sh 'make'  

            } 

        } 

        stage\('Test'\){ 

            steps { 

                sh 'make check' 

                junit 'reports/\*\*/\*.xml'  

            } 

        } 

        stage\('Deploy'\) { 

            steps { 

                sh 'make publish' 

            } 

        } 

    } 

} 

[Toggle Scripted Pipeline](https://www.jenkins.io/doc/book/pipeline/) \(Advanced\) 

|  | [pipeline](https://www.jenkins.io/doc/book/pipeline/syntax#declarative-pipeline) is Declarative Pipeline-specific syntax that defines a "block" containing all content and instructions for executing the entire Pipeline.  |
| :--- | :--- |
|  | [agent](https://www.jenkins.io/doc/book/pipeline/syntax#agent) is Declarative Pipeline-specific syntax that instructs Jenkins to allocate an executor \(on a node\) and workspace for the entire Pipeline.  |
|  | stage is a syntax block that describes a [stage of this Pipeline](https://www.jenkins.io/doc/book/pipeline/#stage). Read more about stage blocks in Declarative Pipeline syntax on the [Pipeline syntax](https://www.jenkins.io/doc/book/pipeline/syntax#stage) page. As mentioned [above](https://www.jenkins.io/doc/book/pipeline/#scripted-pipeline-fundamentals), stage blocks are optional in Scripted Pipeline syntax.  |
|  | [steps](https://www.jenkins.io/doc/book/pipeline/syntax#steps) is Declarative Pipeline-specific syntax that describes the steps to be run in this stage.  |
|  | sh is a Pipeline [step](https://www.jenkins.io/doc/book/pipeline/syntax#steps) \(provided by the [Pipeline: Nodes and Processes plugin](https://plugins.jenkins.io/workflow-durable-task-step)\) that executes the given shell command.  |
|  | junit is another a Pipeline [step](https://www.jenkins.io/doc/book/pipeline/syntax#steps) \(provided by the [JUnit plugin](https://plugins.jenkins.io/junit)\) for aggregating test reports.  |
|  | node is Scripted Pipeline-specific syntax that instructs Jenkins to execute this Pipeline \(and any stages contained within it\), on any available agent/node. This is effectively equivalent to agent in Declarative Pipeline-specific syntax.  |

SonarQube 

[https://www.sonarqube.org/](https://www.sonarqube.org/) 

SQALE Indices and Indicators 

[http://www.sqale.org/details/details-indices-indicators](http://www.sqale.org/details/details-indices-indicators) 

The SQALE Indices 

For any element of the source code portfolio, the SQALE Method defines the following set of indices: 

SQALE Characteristic indices: 

* SQALE Testability Index: STI 
* SQALE Reliability Index: SRI 
* SQALE Changeability Index: SCI 
* SQALE Efficiency Index: SEI 
* SQALE Security Index: SSI 
* SQALE Maintainability Index: SMI 
* SQALE Portability Index: SPI 
* SQALE Reusability Index: SRuI 

The SQALE Quality Index: SQI which measures the Technical Debt 

The SQALE Business Index: SBII which measures the importance of the debt 

Consolidated and density indices \(see the complete list in the definition document\) 

The SQALE Indicators 

The SQALE Method defines 4 synthesised indicators. They provide powerful analysis capabilities and support optimised decisions for managing source code quality and Technical Debt. 

SonarQube Open Source Project Hosting 

[https://sonarcloud.io/explore/projects](https://sonarcloud.io/explore/projects) 

ovirt-root on SonarCloud 

[https://sonarcloud.io/dashboard?id=org.ovirt.engine%3Aroot](https://sonarcloud.io/dashboard?id=org.ovirt.engine%3Aroot) 

Continuous Delivery / Continuous Deployment 

Continuous delivery provides automated builds that are ready to deploy 

Continuous deployment provides automated build and deploy 

Continuous integration is part of both processes 

![](https://c1-word-edit-15.cdn.office.net/we/s/hA3596C17DAD9A003_resources/1033/progress.gif)

Canary 

* Continuous pipeline are no simple feat 
* Many additional tools exist to aid in such automated systems 
* Canary helps deploy new code slowly to user groups incrementally 

Continuous Delivery / Deployment 

* That natural extension of continuous integration 
* Continuous delivery produces deployment ready releases 
* Continuous deployment automatically deploys new builds to uses 
* Vast array of tools which support this process 

Netflix’s Spinnaker 

[https://netflixtechblog.com/global-continuous-delivery-with-spinnaker-2a6896c23ba7](https://netflixtechblog.com/global-continuous-delivery-with-spinnaker-2a6896c23ba7) 

Spinnaker 

[https://www.spinnaker.io/guides/tutorials/videos/](https://www.spinnaker.io/guides/tutorials/videos/) 

Textbook in the field 

[https://martinfowler.com/books/continuousDelivery.html](https://martinfowler.com/books/continuousDelivery.html) 

In the late 90's I paid a visit to Kent Beck, then working in Switzerland for an insurance company. He showed me around his project and one of the interesting aspects of his highly disciplined team was the fact that they deployed their software into production every night. This regular deployment gave them many advantages: written software wasn't waiting uselessly before it was used, they could respond quickly to problems and opportunities, and the rapid turn-around led to a much deeper relationship between them, their business customer, and their final customers. 

In the last decade I've worked at ThoughtWorks and a common theme of our projects has been reducing that cycle time between idea and usable software. I see plenty of project stories and they almost all involve a determined shortening of that cycle. While we don't usually do daily deliveries into production, it's now common to see teams doing bi-weekly releases. 

Dave and Jez have been part of that sea-change, actively involved in projects that have built a culture of frequent, reliable deliveries. They and our colleagues have taken organizations that struggled to deploy software once a year, into the world of Continuous Delivery, where releasing becomes routine. 

The foundation for the approach, at least for the development team, is Continuous Integration \(CI\). CI keeps a development team in sync with each other, removing the delays due to integration issues. A couple of years ago Paul Duvall wrote the book on CI within this series. But CI is just the first step. Software that's been successfully integrated into a mainline code stream still isn't software that's out in production doing its job. Dave and Jez's book pick up the story from CI to deal with that 'last mile', describing how to build the deployment pipelines that turn integrated code into production software. 

This kind of delivery thinking has long been a forgotten corner of software development, falling into a hole between developers and operations teams. So it's no surprise that the techniques in this book rest upon bringing these teams together, a harbinger of the nascent but growing "devops" movement. This process also involves testers, as testing is a key element of ensuring error-free releases. Threading through it all is a high degree of automation so things can be done quickly and without error. 

Getting all this working takes effort, but benefits are profound. Long, high intensity releases become a thing of the past. Customers of software see ideas rapidly turned into working code that they can use every day. Perhaps most importantly we remove one of the biggest sources of baleful stress in software development. Nobody likes those tense weekends trying to get a system upgrade released before Monday dawns. 

It seems to me that a book that can show you how to deliver your software frequently and without the usual stresses is a no-brainer to read. For your team's sake, I hope you agree. 

Deployment best Practices 

[http://guides.beanstalkapp.com/deployments/best-practices.html](http://guides.beanstalkapp.com/deployments/best-practices.html) 

Introduction 

This guide is aimed to help you better understand how to better deal with deployments in your development workflow and provide some best practices for deployments. Sometimes a bad production deployment can ruin all the effort you invested in a development process. Having a solid deployment workflow can become one of the greatest advantages of your team. 

Before you start, I recommend reading our [Developing and Deploying with Branches](http://guides.beanstalkapp.com/version-control/branching-best-practices.html) guide first to get a general idea of how branches should be setup in your repository to be able to fully utilize tips from this guide. It’s a great read. 

Note on Development Branch 

In this guide you will see a lot of references to a branch called development. In your repository you can use master \(Git\), trunk \(Subversion\) or default \(Mercurial\) for the same purpose, there’s no need to create a branch specifically called “development”. I chose this name because it’s universal for all version control systems. 

Web Development Disclaimer 

Our team makes web applications exclusively \([Beanstalk](http://beanstalkapp.com/) and [Postmark](https://postmarkapp.com/)\), so we don’t have much experience when it comes to deploying something that’s not based in the internet. That’s why this guide will probably be more useful for a team like us. I’m sure you can apply some of the tips in other areas too, but if your deployment process drastically differs from the way web applications are usually deployed, be prepared for some clash of concepts in this guide. 

The Workflow 

Deployments should be treated as part of a development workflow, not as an afterthought. If you are developing a web site or an application, your workflow will usually include at least three environments: Development, Staging and Production. In that case the workflow might look like this: 

* Developers work on bugs and features in separate branches. Really minor updates can be committed directly to the stable development branch. 
* Once features are implemented, they are merged into the staging branch and deployed to the Staging environment for quality assurance and testing. 
* After testing is complete, feature branches are merged into the development branch. 
* On the release date, the development branch is merged into production and then deployed to the Production environment. 

Let’s take a closer look at each environment to see what are the most efficient way to deploy each one of them. 

Development Environment 

If you make web applications, you don’t need a remote development environment, every developer should have their own local setup. 

We noticed in Beanstalk that some teams have Development environments set up with automatic deployments on every commit or push. While this gives developers a small advantage of not installing the site or the application on their computers to perform testing locally, it also wastes a lot of time. Every tiny change must be committed, pushed, deployed, and only then it can be verified. If the change was made by mistake, a developer will have to revert it, push it, then redeploy. 

Testing on a local computer removes the need to commit, push and deploy completely. Every change can be verified locally first, then, once it’s more or less stable, it can be pushed to a Staging environment for proper quality assurance testing. 

We do not recommend using deployments for rapidly changing development environments. Running your software locally is the best choice for that sort of testing. 

Staging Environment 

Once the features are implemented and considered fairly stable, they get merged into the staging branch and then automatically deployed to the Staging environment. This is when quality assurance kicks in: testers go to staging servers and verify that the code works as intended. 

It is very handy to have a separate branch called staging to represent your staging environment. It will allow developers to deploy multiple branches to the same server simultaneously, simply by merging everything that needs to be deployed to the staging branch. It will also help testers understand what exactly is on staging servers at the moment, just by looking inside the staging branch. 

We recommend to deploy to the staging environment automatically on every commit or push. 

Production Environment 

Once the feature is implemented and tested, it can be deployed to production. If the feature was implemented in a separate branch, it should be merged into a stable development branch first. The branches should be deleted after they are merged to avoid confusion between team members. 

The next step is to make a diff between the production and development branches to take a quick look at the code that will be deployed to production. This gives you one last chance to spot something that’s not ready or not intended for production. Stuff like debugger breakpoints, verbose logging or incomplete features. 

Once the diff review is finished, you can merge the development branch into production and then initialize a deployment of the production branch to your Production environment by hand. Specify a meaningful message for your deployment so that your team knows exactly what you deployed. 

Make sure to only merge development branch into production when you actually plan to deploy. Don’t merge anything into production in advance. Merging on time will make files in your production branch match files on your actual production servers and will help everyone better understand the state of your production environment. 

We recommend always deploying major releases to production at a scheduled time, of which the whole team is aware of. Find the time when your application is least active and use that time to roll out updates. This may sound obvious, but make sure that it’s not too late, because someone needs to be around after the deployment for at least a few hours to monitor the application and make sure the deployment went fine. Urgent production fixes can be deployed at any time. 

After deployment finishes make sure to verify it. It is best to check all the features or fixes that you deployed to make sure they work properly in production. It is a big win if your deployment tool can send an email to all team members with a summary of changes after every deployment. This helps team members to understand what exactly went live and how to communicate it to customers. Beanstalk does this for you automatically. 

Your deployment to production is now complete, pop champagne and celebrate with your team! 

Rolling Back 

Sometimes deployments don’t go as planned and things break. In that case you have the possibility to rollback. However, you should be as careful with rollbacks as with production deployments themselves. Sometimes a rollback bring more havoc than the issue it was trying to fix. So first of all stay calm and don’t make any sudden moves. Before performing a rollback, answer the following questions: 

Did it break because of the code that I deployed, or did something else break? 

You can only rollback files that you deployed, so if the source of the issues is something else a rollback won’t be much help. 

Is it possible to rollback this release? 

Not all releases can be rolled back. Sometimes a release introduces a new database structure that is incompatible with the previous release. In that case if you rollback, your application will break. 

If the answer to both questions is “yes”, you can rollback safely. After rollback is done, make sure to fix the bug that you discovered and commit it to either the development branch \(if it was minor\) or a separate bug-fix branch. Then proceed with the regular bug-fix branch → staging; bug-fix → development → production integration workflow. 

Deploying Urgent Fixes 

Sometimes you need to deploy a bug-fix to production quickly, when your development branch is not ready for release yet. The workflow in that case stays the same as described above, but instead of merging the development branch into production you actually merge your bug-fix branch first into the development branch, then separately into production, without merging development into production. Then deploy the production branch as usual. This will ensure that only your bug-fix will be deployed to the Production environment without all the other stuff from the development branch that’s not ready yet. 

It is important to merge the bug-fix branch to both the development and production branches in this case, because your production branch should never include anything that doesn’t exist in your stable development branch. The development branch is where developers work all day, so if your fix is only in the production branch they will never see it and it can cause confusion. 

Automatic Deployments to Production? 

I can’t stress enough how important it is for all production deployments to be performed and verified by a responsible human being. Using automatic deployments for Production environment is dangerous and can lead to unexpected results. If every commit is deployed to your production site automatically, imagine what happens when someone commits something by mistake or commits an incomplete feature in the middle of the night when the rest of the team is sleeping? Using automatic deployments makes your Production environment very vulnerable. Please don’t do that, always deploy to production manually. 

Permissions 

Every developer should be able to deploy to the Staging environment. They just need to make sure they don’t overwrite each other’s changes when they do. That's exactly why the staging branch is a great help: all changes from all developers are getting merged into it so it contains all of them. 

Your Production environment, ideally, should only be accessible to a limited number of experienced developers. These guys should always be prepared to fix the servers immediately after a deployment went rogue. 

Conclusion 

We’ve been using this workflow in our team internally for many years to deploy Beanstalk and Postmark. Some of these things were learned the hard way, through broken production servers. These days our production deployments are incredibly smooth and don’t cause any stress at all. \(And we deploy to several dozens of servers simultaneously!\) We really hope this guide will help you streamline your deployments too. 

More Deployment Info 

[http://radar.oreilly.com/2009/03/continuous-deployment-5-eas.html](http://radar.oreilly.com/2009/03/continuous-deployment-5-eas.html) 

Beyond ‘Continuous’ 

[https://martinfowler.com/bliki/BlueGreenDeployment.html](https://martinfowler.com/bliki/BlueGreenDeployment.html) 

[https://martinfowler.com/bliki/CanaryRelease.html](https://martinfowler.com/bliki/CanaryRelease.html) 

