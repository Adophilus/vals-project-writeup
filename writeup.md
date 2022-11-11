# CHAPTER 1
# INTRODUCTION

## 1.1 Background Study

The dissemination of information could prove to be arduous feat. Even in this era, in which the world could be considered as a global village, information intended to reach the populace, many a time, end up missing a few minorities. Some key factors to consider when passing information include:
- speed
- cost
- confidentiality
- reliability
- accuracy
- accessibility 

It would please you to know that all these factors where considered when building this project. For this project, we implemented an information dissemination system we call "Notice Board". Just like a traditional notice board, ours is a virtual replica of it (with a lot of improvements). All the factors to consider when passing information were incorporated and implemented in this project.

- Speed: in the present technology age. Most of the targets of this project are believed to be in possession of a smart phone. Being a virtual platform, the only limit to the speed is the latency on the clients and that of our servers. A lot of work was put into making the delivery of our service as fast as possible. So, in theory, making use of Notice Board on a fast network would make the app work blazingly fast.

- Cost: the cost of communication is a very important factor to consider when communicating. The cost of internet services (presently) is the least it has ever been. Needless to say that consumers would have no issues making use of Notice Board.

- Confidentiality: it is very important that information meant for a receipient is not accessible to outsiders. Over the years,  methods such as encryption, which makes use of cryptography have been employed to ensure the security of information. Notice Board makes use of the secure encryption algorithm known as bcrypt, with a decent iteration count as well a secure salt to ensure the security of notices. Normally, the encryption system of a project should not be revealed. This makes it much harder for it to be attacked by bad actors. But for the sake of this project, the full implementation details would be bared out to the judges in order for them to evaluate it properly. Notices posted on the platform are "scoped" to departments and faculties. The term "scoped", in the context of this project, means that only those in the respective sectors would have access to the respective resource (s).

- Reliability: reliability in this context refers to the ability to have access to data stored in the app without any alteration or modification. In the past, reliability of data was ensured by making copies on the hard disk of machines. Nowadays, there are more sophisticated technologies suited for handling this task. The solution we chose to employ was databases. Particularly a NoSQL database known as PouchDB. This database solution stores data in "versions". In simple terms, mutations to the database are placed "one above the other" -- with the previous state still intact.

- Accuracy: in this information age, there's a lot of news flying around the internet. It is very difficult to say for sure if, the piece of information you have is accurate or not. The common way information is validated in the present day is if an accredited source posts a corresponding information. In our implementation of the project, Notice Board, only admins are permitted to post information. So it is a one-to-many information broadcasting platform. This way, the information ought to be accredited, so long as the process of picking admins is conducted properly.

- Accessibility: like most other networking platforms, Notice Board is freely accessible to all members registered under it's user's organization/institution. So long as the consumer has access to (stable) internet access, he/she can always access it with any modern web browser of their choice.

## 1.2 Statement of Problem

Understanding people’s use of telecommunications, their take up of new innovations and the social consequences of this can sometimes be enhanced by considering people’s communication problems. Such problems can sometimes be experienced at an individual level, as in the amount of spam some people receive over the Internet. However, the main emphasis of this section is on problems experienced in organizations such as schools, especially in relation to the dissemination of informoation to a fairly large audience. This is because many of the examples given emerged from article posted by the well known enterprise corporation, Mitefcee -- Marcin Nowak, (2022). Top 7 Communication Problems in the Workplace. [Mitefcee]. Mitefcee. Through empirical studies, this focused mainly on the school as a unit of analysis, although this could now be expanded to consider interactions with other social institutions.

## 1.3 Aims and Objectives

This project aims at develping software that enables members of an institution to have access to the latest and information pertinnent to their specific department. The users (admins) of this software should be able to create, delete and modify notices which can then be broadcast to all other members (students) for viewing. Through this heirachy of control, a model for information dissemination is well defined and can be implemented in code. The specific objectives include:
- To design a system a responsive user interfaace for the users.
- To develop a comprehensive dashboard for the users.
- To create a database for the system.
- To build APIs for the system.
- To implement the information dissemination model in the system.

## 1.4 Scope of the study

Due to the prohibitive cost associated with the platforms where the project is hosted, we are going to limit the sepation of components of the project as much as possible. In a typical (enterprise level) project, infrastructure and services consumed by a project such as this one (database services, hosting servies, caching services, load balancing and server setup) are usually separated beause it is much easier for separate teams to manage them efficiently. But, this is not to say that the project is sub-standard. No, not at all. It only means that all the requirements of the project were bundled into a single package.

## 1.5 Limitations of the study

The major limitation of this project was the high cost of managing the live version of the project on the world wide web (the internet). Besides the high cost of management, power supply was also an issue faced while undertaking this project. Beyond these issues, there are no more problems with regards to the implementation of the project.

## 1.6 Significance of study

This is aimed at developing a software system that will enhance the propagation of information between members of an institution or organization. It employs the use of modern web technologies to implement the business logic. This allows members to have easy access to the platform and easily interact with the platform. In addtion to that, the model of operation the project employs, ensures, among other things, the accuracy and accessibility of the project to end users.

## 1.7 Organization of work
This project work is organized into five chapters, Chapter one discusses the Introduction of the Project, Problem Statement, and the specific Aim and Objectives, It also discussed about the Scope of the work covered, Limitations of the Study, and  Significance of Study, In the Chapter two we elaborated the literature review and the overview of information broadcast systems, we also discussed history of communication and information broadcast systems, improvement of communication systems and the internet as a  technological enabler in improving upon the previous methods of communication. In Chapter three we discussed on the Research Methodology, Methodology adopted, the Tools and Materials used to obtain information for the project work. Chapter four discusses the Design and Implementation of the project and also the choice of development tools, Finally Chapter five which is the last chapter comprises of the Summary, Recommendation, and Conclusion of the project.

# CHAPTER 2: LITERATURE REVIEW

## 2.1 Conceptual Framework

### 2.1.1 Overview of Information Broadcast Systems

Broadcasting is the distribution of data or information to a dispersed audience via any electronic mass communications medium, but typically one using the electromagnetic spectrum (radio waves), in a one-to-many model. Broadcasting began with AM radio, which came into popular use around 1920 with the spread of vacuum tube radio transmitters and receivers (Wikipedia). An information broadcast system is, in essence, a platform that enables the users to easily distribute information to a dispersed audience.

### 2.1.2 History of Communication and Information Broadcast Systems

Radio is the first 'modern' media form, and had a huge impact on the history of the 20th century. For the first time information could be broadcast, ie it could be received by anyone with the right equipment, without wires. The birth of radio ushers in the era of mass communications. Many people have likened the explosion in radio in the 1920s to what is happening with the internet today - lots of enthusiasts setting up their 'broadcast slot' and sharing their knowledge with similar people. Wireless communication has really come full circle, as more and more people turn to mobile phones and handheld computers that can receive internet 'transmissions'. As with the recording of images (in the 19th century they were recorded on metal plates, now they are recorded on metal plates that make up DVDs and computer hard drives) the broadcast of information has come full circle. The idea of television (i.e. sending and receiving images along wireless technology) was first bouncing around in the 1870s, but it did not become a reality until the 1920s. It is very difficult to name one person as 'the inventor of television' as different scientists all over the world invented different components to combine into what we understand today as 'TV technology'. The first of these was Vladimir K. Zworykin, who in 1921 invented a device that would convert patterns of light into electronic impulses. He was followed by Scotsman, John Logie Baird, who produced the first television set in 1924, but it showed only shadows. Also in 1924, Philo Farnsworth, an American, came up with the concept of broadcast television. By 1928 engineers had managed to create a crude receiver set and camera, and this went on show at the World's Fair - the first public viewing of television. However, the opportunities presented by TV were clear to many before this, and both the BBC and CBS were established in 1927. These two technologies really opened up a whole lot of possibilities with regards to information broadcast sysems. In the present day, information is distributed over the bedrock of modern civilization -- the internet. Through the internet (and any internet capable device of course), information dispersal has become seamless compared to the ancient methods employed in the past.

## 2.2 Theoretical Framework

### 2.2.1 Previous Research on Information Broadcast Systems
Much research has been done on information broadcast systems. One particular one which seems very interesting is The Impact of **Information and Communication Technology on Radio and News Reporting by ABUAD**. The research detalils ket concepts regarding information broadcast systems using the FM radio as their abstraction of an information broadcast system. This chapter reviews some of their studies and their main findings. We will also be making reference to their model of an information broadcast system -- the FM radio.

### 2.2.2 FM (Frequency Modulation)
Frequency Modulation (FM) is a method of impressing data onto an alternating-current (AC) wave by varying the instantaneous frequency of the wave. This scheme by be used by both analog and digital data. In analog, FM, the frequency of the AC signal wave also called the carrier varies in a continuous manner while in digital FM, the carrier frequency shifts abruptly rather than continuously leaving the number of possible carrier frequency states toe power of two 
(2) as compared to the analogue whose frequency carriers are infinite.

### 2.2.3 Radio
A radio is communication over distance where sounds are converted to electromagnetic wave and sent to a receiver that transfers the waves back to sounds. It can also be defined as the transmission and reception of electromagnetic wave of radio frequency, especially those carrying sound messages.

### 2.2.4 Review of Related Studies
The two works reviewed are:
- Technological Determinism theory and media practitioners perception of cultural impact of Information and Communication Technologies on developing nations by Levi Nwodu(2004)
- Information and Communication Technologies for sustainable livelihood by http//egov.gor. sglegont actionplanning.htm(website). The first work to be reviewed is journals by Levi Nwodu, 2004, published in Nigeria.

## 2.3 Empirical Framework
Empirical studies of information broadcast systems, ansd using a widely used user-friendly design to increase efficiency is recognized to have high significance on information dissemination.

Researchers have shown different perspectives and concepts related to information systems by implementing technologies of the modern trends. The consulted research papers gave insights on information broadcast systems (using the radio as an abstraction) in genral, as well as some technical details regarding its mode of operation.

Finally, the paper made mention of communication technologies which could be used to further develop the present mode of operation.

# CHAPTER THREE
# RESEARCH METHODOLOGY

## 3.1 Research Methodology Overview

A research methodology is a systematic approach of well-define procedure that should be followed in carrying out a true research project. An adequate suitable methodology used helps to ensure that a thorough study of the present system is carried out, thus helping the project researcher to completely understand the modus operandi of the present existing system so as to know how the new system should be structured and functionalities needed in it to address the seemingly, existing problems discovered. This also helps to know if there should be total overhauling of the existing system or if the only improvement should be made.

Many different methodologies have been used in designing a model. The methods can be summarized into several categories which includes:

- **Waterfall Model**: This model follows a sequential order which ensures that a phase is completed before another phase begins. This system model emphasizes planning at the early stage, its used in project where all the system requires are known and in addition, its intensive documentation and planning make it work well for projects in which quality control is a major concern. (Mishra, 2015).
The phases of waterfall model are: Requirements, Design, Implementation, Testing, and Maintenance.
Hence, for the aforementioned reason we will not adopt waterfall model. 

- **Prototyping Model**: Prototyping Model is a software development model in which prototype is built, tested, and reworked until an acceptable prototype is achieved. It also creates base to produce the final system or software. It works best in scenarios where the project's requirements are not known in detail. It is an iterative, trial and error method which takes place between developer and client.

Prototyping Model has six SDLC phases as which include:
Requirements gathering and analysis, Quick design, build a Prototype, Initial user evaluation, refining prototype, and Implement Product and Maintain.

#### Advantages of the Prototyping Model
- Users are actively involved in development. Therefore, errors can be detected in the initial stage of the software development process.
Missing functionality can be identified, which helps to reduce the risk of failure as Prototyping is also considered as a risk reduction activity.
- Helps team member to communicate effectively.
- User satisfaction exists because the user can feel the product at a very early stage.
- There will be hardly any chance of software rejection.

#### Disadvantages of the Prototyping Model
- Prototyping is a slow and time taking process.
- The cost of developing a prototype is a total waste as the prototype is ultimately thrown away.
- Prototyping may encourage excessive change requests.
- Sometimes customers may not be willing to participate in the iteration cycle for the longer time duration.
- Poor documentation because the requirements of the customers are changing.
- Due to the fact that the cost of developing a prototype is a waste and it also slows the processing time, we will not adopt this model as methodology that will be used in building this project.

- **Spiral Model**: is a risk-driven software development process model. It is a combination of waterfall model and iterative model. Spiral Model helps to adopt software development elements of multiple process models for the software project based on unique risk patterns ensuring efficient development process.
Each phase of spiral model begins with a design goal and ends with the client reviewing the progress. The development process in Spiral model in SDLC, starts with a small set of requirements and goes through each development phase for those set of requirements. The software engineering team adds functionality for the additional requirement in every-increasing spirals until the application is ready for the production phase.

The phases of spiral model are:    
 Planning, Risk Analysis, Engineering, and Evaluation.


#### Advantages of Spiral Model
- Additional functionality or changes can be done at a later stage.
- Cost estimation becomes easy as the prototype building is done in small fragments.
- There is always a space for customer feedback.
- Development is fast and features are added in a systematic way in Spiral development
- Continuous or repeated development helps in risk management.

#### Disadvantages of Spiral Model
- Risk of not meeting the schedule or budget.
- Spiral development works best for large projects only also demands risk assessment expertise.
- Spiral software development is not advisable for smaller project, it might cost them a lot.
- Documentation is more as it has intermediate phases.
- For its smooth operation spiral model protocol needs to be followed strictly.

Spiral model is specifically for large project development due to its cost effective. For the purpose of this project spiral model will not be the best methodology to adopt. 

- **RAD Model**: RAD Model or Rapid Application Development model is a software
development process based on prototyping without any specific planning. In RAD
model, there is less attention paid to the planning and more priority is given to the development tasks. It targets at developing software in a short span of time. It focuses on input-output source and destination of the information. It emphasizes on
delivering projects in small pieces; the larger projects are divided into a series of smaller projects. The main features of RAD modeling is that it focuses on the reuse of templates, tools, processes, and code.

RAD modeling has following phases:
Business Modeling, Data Modeling, Process Modeling, Application Generation, and Testing and Turnover.

#### Advantages of RAD Model:
- Flexible and adaptable to changes.
- It is useful when you have to reduce the overall project risk.
- It is easier to transfer deliverables as scripts, high-level abstractions and intermediate codes are used.
- Due to code generators and code reuse, there is a reduction of manual coding.
- Each phase in RAD delivers highest priority functionality to client.

#### Disadvantages of RAD Model:
- It can't be used for smaller projects.
- Not all application is compatible with RAD.
- Reduced features due to time boxing, where features are pushed to a later version to finish a release in short period.
- If developers are not committed to delivering software on time, RAD projects can fail. 
- Requires highly skilled designers or developers.
- Progress and problems accustomed are hard to track as such there is no documentation to demonstrate what has been done.
- RAD Model is a methodology that is not situatable for small project work and does not incorporate documentation in the developing a model. For this reason, we won’t adopt it.

## 3.2 Methodology Adopted
A software development methodology or system development methodology is a frame work that is used to structure, plan and control the process of developing an information system. Hence, after duly considering the above methodologies the Agile Methodology is adopted because agile methodology is a software development methodology that is more responsive to customer needs than the traditional methods such as the waterfall development model. The waterfall development model is similar to a wide and slow-moving value stream, and halfway through the project, 100% of the requirements are typically 50% done. However, for agile development, 50% of requirements are typically 100% done halfway through the project. This methodology has a strong collaborative style of working, and its approach. Agile is designed to accommodate change and the need to produce software faster.
Agile values individuals and their relationships and interactions over tools, it features customer collaboration throughout the development process, it responds to change instead of following a set-in-stone plan, and focuses on presenting working software rather than documentation.  

### 3.2.1 Stages of Agile Methodology
Customer needs are changing at a rapid pace, particularly in software development. Agile development embraces constant change through an iterative approach to technology design and development. The Agile lifecycle adds structure to what is a fluid and flexible method of delivering a working product.
The 5 stages of the Agile System Development Life Cycle (SDLC) are;
Project Initiation: The first stage in the life cycle of agile software development. Often referred to as the inception or envision phase, this initial stage is about discussing the project vision and the ROI justification. This is a high-level feasibility discussion and does not delve into the specific details. During this step, you should identify team members and determine the time and work resources are required to complete the project. Taking stock of resources is crucial to determining economic feasibility for project approval.

Planning: This speculative phase is when the Agile lifecycle really takes shape for the team. Release planning is where the team gets together with their sponsor or product owner and identifies exactly what they are looking for. They discuss how this will be made possible by building the backlog at the story level. A good way to think about stories is how the end-user might describe the feature or product. A story should include the type of user, what they want from the product and why. The business opportunity in a wider context should be considered here. This will impact how viable the project is in a functional and financial sense and should be estimating the risks and developing milestones with an initial release plan. Planning is only complete when your backlog is complete and you have prioritized the items based on business value and dependency.

- **Development**: Once the requirements have been defined based on feedback from the product owners and stakeholders, the actual work begins. Agile product development delivers high quality working products in incremental phases, sprints, or iterations. Developers start building the first iteration of the product with the aim of having a working, usable product at the end of the sprint. This is far from the final version and will undergo a number of revisions so it should only include minimum functionality. This functionality can be expanded on in future iterations of the Agile lifecycle.

- **Production**: Your product has now been deployed and is being used by final end-users. It is important to closely monitor these early stages for bugs or defects missed in testing. A handover with relevant training should take place between the production and support teams. These final processes and handovers can vary depending on the type of product you are outputting. The production phase typically ends when the product is ready to be retired.

- **Retirement**: The final stage of the Agile lifecycle. The product is now at the ‘end of life’ stage and will be pulled from production and decommissioned (sometimes referred to as ‘sunsetting’). Customers are notified and informed about migration to newer releases or alternative options. Products are retired for a number of reasons. In most cases, it is because a newer release is being deployed and (or) the older release is no longer being supported. In this case, some final, minor software updates may be made to the newer system. It could also be retired because the product is not cost-effective within the current business model and therefore phased out.

### 3.2.2 Differences between Agile and Waterfall 
The agile model focuses on an iterative and incremental approach to software development, whereas in the Waterfall model, software development takes place sequentially from the start to end. 
You’d have to break down an agile project into individual models. But you won’t have to do that in the Waterfall approach.
Customers get early and frequent access to your working product in the agile approach. They can give you feedback accordingly and let you change your future work plan. On the other hand, customers will get access to the product only when it’s finished if you follow the Waterfall approach.
Agile development is excellent for small projects as you can complete them fast. The Waterfall method is great for large projects because you can make more accurate estimations and complete the plan accordingly.
There is less planning in Agile development in comparison to Waterfall development.

### 3.2.3 Agile Methodology Steps 
The following are steps involved in Agile Methodology:
SCRUM: SCRUM is a framework that focuses on empowering teams to work together. It is a heuristic. It focuses on adjusting to factors that fluctuate and continuous learning. It understands that a team doesn’t necessarily know everything at the start of the task. Scrum is based on the strategies of rugby teams. It focuses on enhancing the collaboration in a team by dividing it into smaller ones, just like a rugby team does. In a rugby team, it has different groups of players who have specific responsibilities. Scrum has three primary artifacts that are an increment, a sprint backlog, and a product backlog. 

### 3.2.4 Advantages of Agile Methodology
Agile today stands as one of the most popular approaches to project management because of its flexibility and evolutionary nature. Its advantages include;

- Superior quality product
- Customer satisfaction
- Better control
- Improved project predictability
- Reduced risks
- Increased flexibility
- Continuous improvement
- Improved team morale
- More relevant metrics.

## 3.3 Data Gathering Techniques 
A thorough investigation of the current system was made in order to obtain detailed fact about the application area to be redesigned. Investigation also covers looking at the functional requirement of the system and finding out whether the requirements and objective of the present system are big achieved.

### 3.3.1 Interviewing
In view to investigation, students were investigated and a mini-poll was made on a small sample size of 50 students. This method yields the most profitable result as it is obtained by physical contact. The essential element of the interview is obtained directly and in a short time than when other methods are employed sice the interviewer is with the interviewed. This immediate feedback gives the opportunity to ask ambiguous questions and hence, obtain responses.

### 3.3.2 Use of Secondary data
Internal and external data is expected to be collected, in order to give a clear understanding of this project study. 
Internal sources of data included but not limited to making use of the school library, surverying students, and inductive reasoning.
External sources of data included Commercial journals, Text books, Research reports, Government publications and the internet to access vital resources for the purpose of the project.

## 3.4 Tools and Materials
For effective design and implementation of this flexible call center solution for MSMEs, there are key tools and materials that was put together;

### 3.4.1 HTML
HTML (Hypertext Markup Language) is the code that is used to structure a web page and its content. This project is a web-based project and html was strictly used to structure the web pages for the project 

### 3.4.2 CSS (BOOTSTRAP)
CSS (Cascading Style Sheets) is the language we use to style an HTML document. CSS describes how HTML elements should be displayed. CSS helps to beautify the web pages and makes it look more presentable. 
BOOTSTRAP is a CSS frame work that helps in making the web pages responsive on different screen size. This project is designed to be accessible from any device and bootstrap is used, to give it a better user experience.  

### 3.4.3 JavaScript (Vue.js)
JavaScript, often abbreviated as JS, is a programming language that is one of the core technologies of the World Wide Web, alongside HTML and CSS. As of 2022, 98% of websites use JavaScript on the client side for webpage behavior, often incorporating third-party libraries. The
Third-party library used in the implementation of the user interface in this project is Vue.js which is a modern web development framework for developing reactive web apps.

### 3.4.4 PouchDB
PouchDB is an open-source JavaScript database inspired by Apache CouchDB that is designed to run well within the browser. PouchDB was created to help web developers build applications that work as well offline as they do online.

### 3.4.5 NodeJS
Node.js is a platform built on Chrome's JavaScript runtime for easily building fast and scalable network applications. Node. js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient, perfect for data-intensive real-time applications that run across distributed devices.

# CHAPTER FOUR
# DESIGN AND IMPLEMENTATION

This chapter depicts how the system is designed; it shows the input and output requirement of the system, the hardware and software requirement and other requirements. It shows a system flowchart that shows how operations are carried out. 

## 4.1 User and System Requirements
System requirements are the building blocks used to build systems; they describe what the system “shall do.” System requirements are classified as either functional or non-functional requirements.  A functional requirement specifies something that a user needs to perform their work. Non-functional requirements specify all the remaining requirements not covered by the functional requirements. While user requirements, often referred to as user needs, describe what the user does with the system, such as what activities that users must be able to perform

### 4.1.1 Functional Requirements

#### Admin Management

- The system will allow an admin to set it up
- The system will allow an admin to login
- The system will allow an admin to post (scoped) notices
- The system will allow an admin to modify posted notices
- The system will allow an admin to view notices
- The system will allow an admin to delete notices

#### User Management
- The system will allow students to sign up
- The system will allow students to login
- The system will allow a student to view notices relevant to them

#### Non-Functional Requirements
#### Usability 
- The system must be easy to use by both Admins and Users such that they do not need to read an extensive number of manuals.
- The system must be quickly accessible by both Admins and Users.
- The system must be intuitive and simple in the way it displays all relevant data and relationships.
- The menus of the system must be easily navigable by the Admins with buttons that are easy to understand. 

#### Reliability 

- The System must give accurate caller status to the admin continuously. Any inaccuracies are taken care by the regular confirming of the actual levels with the levels displayed in the system.
- The System must successfully add any response given by the users to the database and Admins dashboard.
- The system must provide a password enabled login to the Admin to avoid any foreign entity changing the data in the system.
- The system should provide the Admins updates on completion of requested processes and if the requested processes fail, it should provide the user the reason for the failure.
- The system should not update the data in any database for any failed processes.
-- Performance 
- The system must not lag, because the Users using it don’t have down-time to wait for it to complete an action.
- The system must complete updating the databases, setting up the occasions successfully every time the Admin requests such a process.
- All the functions of the system must be available to the Admins and     Users every time the system is turned on.
- The calculations performed by the system must comply according to     the norms set by the user and should not vary unless explicitly changed by the user.

#### Implementation 
- The System User Interface is built using Bootstrap 4 and Vue.js.
- The Programming is done in Sublime Text 3.
- The Database is implemented using PouchDB.

#### Interfacing
- The system must offer an easy and simple way of viewing Admin dashboard
- The system must be able to display all notices relevant to users on the admin dashboard.

### 4.1.3    Software Requirements
- The software requirements are basically for both the server and clients. The server side requires
NodeJS, whereas the clients require only the web browsers. 
The following are the list
- Operating System version: Windows 7 or higher (32- or 64-bit operating system)
- Front-End Tools: Sublime Text 3
- Back-End Tools:  NodeJS
- Database Tools: PouchDB
- Technology: JavaScript

### 4.1.4 Hardware Requirements
In the cost of the design, the software developed needed the following hardware for an effective and efficient operation of the new system. 
- IBM Intel or Microsoft compatible computers.
- Processor: Pentium 2.0 GHz or above
- Memory: 2GB RAM or above
- Hard Disk: 250GB or above 
- Display -5VGA
- Keyboard: Standard Windows Keyboard
- Mouse: Two or Three Button Mouse

## 4.2 System Model
System modeling is the process of developing abstract models of a system, with each model presenting a different view or perspective of that system. It is about representing a system using some kind of graphical notation, which is now almost always based on notations in the Unified Modeling Language (UML). Models help the analyst to understand the functionality of the system, they are used to communicate with customers (Khan, 2011).

### 4.2.1 System Use Case
A use case diagram is the primary form of system/software requirements for a new software program underdeveloped. Use cases specify the expected behavior (what), and not the exact method of making it happen (how). A key concept of use case modeling is that it helps us design a system from the end user's perspective

[Use case for Admin](./imgs/use-case-admin.png)
**Use case for Admin**

[Use case for User](./imgs/use-case-user.png)
Use case for User

## 4.3  System Architecture 
A system architecture is a Conceptual model that defines the structure, behavior, and more views of a system. An architecture description is a formal description and representation of a system, organized in a way that supports reasoning about the structures and behaviors of the system (Jaakkola, 2011).

### 4.3.1 System Flowchart
A flowchart is a diagram that depicts a process, system or computer algorithm. They are widely used in multiple fields to document, study, plan, improve and communicate often complex processes in clear, easy-to-understand diagrams. The system flow diagram is a visual representation of all processed in sequential order, it is a graphical representation of the relation between all the major parts or step of the system. To develop a more accurate system, the flowchart cycle below was developed, validation is always performed every time a user tries to login and if the validation result is not satisfying, the user cannot login. After the development converges, the system will be tested and some quantitative measurement will be computed to determine if the design works well, the factors that affect its performance would also be analyzed, and incremental modifications will be performed accordingly.

## 4.4 Data Modeling
A data model an abstract model that organizes data description, data semantics, and consistency constraints of data. The data model emphasizes on what data is needed and how it should be organized instead of what operations will be performed on data. It is like an architect's building plan, which helps to build conceptual models and set a relationship between data items.


## 4.5 Implementation
This is the system of laying down direction and principles to be followed in other to achieve the desired goals and objectives. Precisely, implementation involves the practical method of putting into functioning all theoretical design and getting the system into implementation or operation.
 
### 4.5.1 Setting up the developmental environment 
Before building applications, there is a need to prepare the development environment with each technology, and tools to aid development and debugging, technologies to be used in this project as stated in the software requirements include NodeJS environment, modern web browser and API.

## 4.6 System testing
System testing is an important element of software quality assurance and represents the ultimate review of specification, design and coding.  There are rules that can serve as testing objectives.  They are; Testing is a process of executing a program with the intent of finding an error. A good test case is one that has high probability of finding an undiscovered error. A successful test is one that uncovers an undiscovered error.
Unit Testing:   In testing this system, the individual functions and modules were put to the test independently.  By following this strategy all, the errors in coding were identified and corrupted.  This method was applied in combination with the white and black box testing techniques to find the errors in each module.

- **Integration Testing**: Again, this software testing strategy has different approach in which integration is carried out from the top-level module to the bottom and the bottom-up approach in which integration is carried out from the low-level module to the top. The modules are tested using the bottom-up approach by introducing stumps for the top-level functions.
 This test used to identify the errors in the interfaces, the errors in passing the parameters between the functions and corrects them. 

- **Acceptance Testing**:  Acceptance testing is sometimes performed with realistic data of the client to demonstrate that the software is working satisfactorily.  It includes database features like integrity, consistency, security and validity.

## 4.7 System Deployment
There several methods of deploying a system, these includes;
- Direct Cutover
- Parallel Operation
- Phased Operation
- Pilot Operation
- For this particular system, parallel Operation was chosen because the parallel operation changeover method requires that both the old and the new system operates fully for a specified period. When users are satisfied that the new system operates correctly, the old system is terminated.

# CHAPTER FIVE
# SUMMARY, CONCLUSIONS AND RECOMMENDATIONS

## 5.1 Summary
Information communications systems is one of the most important foundations for building a society. Social media platforms have been on the rise in recent years and the trend would not stop anytime soon.

## 5.2 Conclusions
It has been a great pleasure for us to work on this exciting and challenging project. This project proved good for us as it provided practical knowledge of not only programming, in web-based application and no some extent Windows Application and NodeJS environment, but also about all handling procedure related with “Notice Board”. It also provides knowledge about the latest technology used in developing web enabled application and client server technology that will be great demand in future. This will provide better opportunities and guidance in future in developing projects independently. The benefits derived from this work cannot be over emphasized as tremendous amount of new knowledge was revealed and acquired in the course of study for this project work. 
In spite of the constraints encountered during the implementation of this project, the aim of the project is well accomplished.

## 5.3 Recommendation
Based on the objectives of this project and experience gained during its design and implementation, I wish to the following recommendation for future improvement of information systems. 
Information systems should incorporate a sleek and user friendly design in order to captivate users and make them stay longer on the platform. This system will be useful since it is computerized and will promote effective, efficient and improve service delivery. The use of this software developed for users will make their work easier.

# REFERENCES

Afe Babalola University, Uyo, "The Impact of Information and Communication Technologies" pp.  8-13. 
Research in Computer and Communication Engineering, vol. 3, no. 3, pp. 665–688.
Moon, Y., Leung, C., Yuen, K., Ho, H., & Yu, X, (2000), “A CRM model based on voice over IP”, Canadian Conference on Electrical and Computer Engineering. Conference Proceedings. Navigating to a New Era (Cat. No.00TH8492), pp. 464-468.
Khan, A.I., Qurashi, R. J and Khan, U. A. (2011). 'A Comprehensive Study of Commonly Practiced Heavy and Light Weight Software Methodologies ', IJCSI International Journal of Computer Science Issues, 8(4), pp. [Online]. Available at: https://arxiv.org/ftp/arxiv/papers/1111/1111.3001.pdf
V. C. Buyut, S. H. Siadat, 2008, “2008 International Conference on Computer and Electrical Engineering, pp. 419-423.
A. Bhondge, A. Bhatkar, 2015, “Interactive Voice Response System by Using Asterisk”,International Journal of Innovative 
A. Bhondge, A. Bhatkar, S. Fender, S. Thakre, M. Goel, (2015), “Interactive Voice Response System by Using Asterisk”,International Journal of Innovative Research in Computer and Communication Engineering, vol. 3, no. 3, pp. 665–688.
Wenqing Zhang 2017 IOP Conf. Ser.: Earth Environ. Sci. 100 012073, "Research on the Integration of IT Network Technology and TV Production and Broadcasting System", pp 3-4.
