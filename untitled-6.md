# Software Dev Processes Project 1

**Assignment Topic:**

As a software development professional, you will run into all kind of projects and situations within those projects. This assignment is designed to present you with a fictitious situation and ask you to recommend a software development approach suited to the situation. 

Here is the situation: 

Zenith Healthcare is a new company in the market and has launched its product two years ago. The product is loved by clients and is growing in popularity. The level of product demand was not anticipated, and the current system architecture cannot support the rising demand. To support the anticipated demand, the company needs to re-architect the system and provide the exact same functionality. Thus, the requirements from the client perspective are very well known and do not need to change. What needs to be changed in the system to support the growing demand is also well understood. The product has 4, fairly independent components. All 4 components need to be re-architected. Out of the 4, one of them has caused the most pain and the organization could benefit greatly if that component could be replaced first with a new, highly scalable architecture. The work of migrating to a new platform is a tedious job and the deployment of a new system will involve a lot of external communication, managing customer expectations, etc.

The technical architect and one project manager will be working from the corporate headquarters in Germany, but most of the team who will be doing the coding for the migration will be offshore in Belarus. The testing team will also be in Belarus.

What software development methodology would you suggest for this situation and why? 

* Step 1: Start analyzing the scenario by **identifying the characteristics** of this situation and **specify the logic** behind the selection of characteristics. For example, you may identify "User Needs Unknown" as a characteristic based on statement X, Y and Z in the scenario.
* Step 2: **Select a model** that best fits the characteristics you identified in step 1. **Justify your choice** by providing by the logic behind your selection. For example, you may say that since the scenario has characteristics X and Y, models A and B are potential candidates. Additionally, since the scenario has characteristic Z, model A is the best option.

Imagine that you were the lead or project manager for this project. For the selected model, take us through a simulated / fictitious journey on how this project will be completed all the way from defining requirements to deployment. You are free to make up characters as you feel appropriate to fit your story. Please watch the video on" Model Selection" to get an idea. The video stays at high level, but you can go in further details as you feel necessary. In your story, please make sure to talk about artifact and practices followed by the team on this project.

Assume that you are the quality lead or technical lead on this project. What kind of testing would you suggest the team to do? Be sure to justify your answer. To answer this question, first list down the key things from the use case above that are really important. For e.g. scalability, performance, usability, integration between components etc. After that, identify what type of testing would you want the team to do to make sure that upgraded product is high quality and deployed defect free. Please refer to the "Testing and Verification" section in module 2. Also, please watch following videos to learn about various types of testing methods: [https://www.coursera.org/learn/software-processes/lecture/G30EZ/software-testing-perspectives](https://www.coursera.org/learn/software-processes/lecture/G30EZ/software-testing-perspectives)

Continuing your role as a quality lead or technical lead for the project. Write a few example of test cases or a descriptive narrative for what you expect the testing team to use when testing this product. Please refer to the "Testing and Verification" section in module 2. Feel free to make assumptions about the functionality of the system to come up with a scenario.

**My Assignment View**

To begin as the requirements from the client are well known in part from the outset we can use the V model methodology as what is required is defined from the outset, but with testing we know it has a ‘tedious’ element to it being able to implement early on will allow bugs and fixes to be done early which would help speed up testing. Understanding the full requirements of the client the main point being that they current system architecture does not support the company’s plan for scaling up and increased demand but they do know that they want the same functionality but perhaps may not know to the full extent they wish the future architecture to look just that is needs to be ‘highly scalable’.

There are 4 components that make up the architecture and there is a known pain point and this should be the first part of the solution worked upon.

Using the SCUM and Kanban frameworks would be my approach as the principles and properties can be set in advance, the backlog can be prioritized by the team lead and work with the QA’s and developers in order to develop the requirements, and design to present back to the college before implementation and verification is done. Being flexible is the key so concepts should be taken from the SCRUM methodology, using SCRUM daily meetings will give focus to what has been done so far and what will be done daily, but perhaps without the need to do it on a 1-4 schedule, this would also help work collaborate with the teams in Germany and Belarus in order to understand what they are working on today and achieved the previous day.

I would use the incremental model so that the components could be build in parts and so that there is continuous feedback. As there are just 4 components these may well overlap and being adaptive to each of them. This will allow the ‘pain’ component can be delivered early and gain feedback from this increment to improve the other 3 components. The company then could benefit first by having this component delivered first and define future incremental components

Software coupling will need to be tight in order to ensure that the connection between the components remains strong and the cohesion is also maintained should any inheritance be done from the existing architecture

The project manager should coordinate with the technical architect in terms of building as the majority of the testing will be done in Belarus. Testing and verification should be run in parallel with the existing system, although not favoured by the client the testing team will be able to ensure that bugs and issues are found whilst the new architecture is tested before. Using event based model so to feed in the various components into 1 central point which can be managed by the project manager.

Implementation and deployment should be done for each component when ready, with running both architectures in parallel this should avoid the need to rollback so as a minimum holding the old/original in hot failover once the new components are ready for release will prevent failure for the client.

Due to the clients demands and wishes being agile and lean is the key with the delivery, keeping the development cycles short will help build the right product to allow the client to scale and bring to market quickly. Challenges of 2 offshored teams can be negated by working collaboratively and using the scrum principles to ensure everyone is on track and to identify areas that may be dropping behind and to allow the testing team time to perform what they need to for a tedious task.

