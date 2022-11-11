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


