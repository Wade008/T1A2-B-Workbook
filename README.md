# **T2A1-A - Workbook**  
**Name:** Wade Doolan  
**Student number:** 12678  

<hr>   

## **Question 1:**  

*Describe the architecture of a typical Flask application.*  


<hr>  

## **Question 2:**  

*Identify a database management system (DBMS) commonly used in web applications (including Flask) and discuss the pros and cons of this database.*  


<hr>  

## **Question 3:**  

*Discuss the implementation of Agile project management methodology.*  

In general, the agile project management approach outlines a set values and principles upon which specific agile project management methodologies are based. These values include placing more importance on:
- People and communication rather than processes;
- Properly functioning software over documentation;
- Customer focused behaviour rather than contractual requirements; and
- adapting to change over a strict plan. 

(Aipm.com.au, 2022)  

More specifically, the agile approach to project management is iterative and involves regular releases of the software product being developed, with customer feedback integrated into each release. The agile approach can be grouped into two broad project management methodologies, scrum and kanban (Atlassian, 2022). The most notable difference between the two approaches is that scrum uses fixed length iterations of work called sprints to address each item in a prioritised list of tasks, while kanban is focused more on getting things done as quickly as possible and bases the work iterations on team capacity (Atlassian, 2022a). Regardless of which agile method is used, implementation will follow the same general process 

**1. Project planning:** this is where the following is determined:
- The end goal,   
- The value of the product to the organisation or client
- How the product will be developed. 
- A general project scope can be developed here, but it needs to remain flexible.

**2. Product creation roadmap:** At this stage a list of features that will make up the end product is developed. This list of features will be added to a backlog or to-do list. At a later stage each feature in the backlog will be built by the team as part of each sprint.

**3. Release planning:** In contrast to the waterfall project management approach, where there is one final release date, the agile method involves product features being released at the end of shorter development cycles (aka sprints). At the release planning stage a high level feature release plan is developed; however, since agile is flexible, this plan is subject to change and the release dates are reassessed at the beginning of each sprint.  

**4. Sprint planning:** This takes place before each sprint and involves meeting to determine resource allocation, how tasks will be achieved and task load distribution. A visual outline of workflow during the sprint is required to ensure the team is able to identify and remove any potential roadblocks.  

**5. Daily stand-ups:** short (max. 15 minute) meeting are held daily throughout each sprint. They involve each team member briefly discussing what they achieved the day prior and what they intend to achieve that day. 

**6. Sprint review and retrospective:** This stage involves holding two meetings:  
-  *Sprint review* - This involves meeting with the product stakeholders to show them the finished feature. This meeting is designed to ensure constant communication with the stakeholders, to build the relationship and ensure any product issues are dealt with early.  
- *Sprint retrospective* - This involves meeting with team members to discuss what went well and what could have been done better during the sprint. It is also important to discuss if the task load was too heavy or light and to highlight what was accomplished.

(Workfront.com, 2020)



<hr>  

## **Question 4:**  

*Provide an overview and description of a standard source control workflow.*  

While there are a number of version control systems available, this question will be answered in the context of the Git and GitHub source control system. A source control workflow is an agreed process upon which the flow of code changes are applied during development. Notably, there are several common approaches to source control workflow, including centralised workflow, feature branch workflow and forking workflow (Atlassian, 2022c). The following is based on the feature branch workflow.

### Overview  
**The feature branch workflow** involves developing each feature on a dedicated branch, separate to the main branch holding the main codebase. This approach allows developers to work on a product feature, collaborate and review the new feature code before it is ultimately merged onto the main codebase. This approach can protect the main code from potential faults and facilitates continues development (Atlassian, 2022b). 

 ### Description   
 The general process below can be followed for feature development workflow.  

 Note: It's assumed a remote GitHub repository has been created and has a main branch that holds the latest code. It's also assumed that all developers in the team have full access to the remote GitHub repo.  

 A developer has been assigned a task to develop a new feature for a product under development. 
 
 1. On their local machine they ensure their copy of the main code base is up-to-date. Whilst on the main branch, they can do this using a ```git pull``` or other commands like ```git fetch origin``` and ```get reset --hard origin/main```.  
 2. Still local, create a new branch and give it the name of the feature to be developed. For example, ```git checkout -b new-menu-feature```.  
 3. Develop the feature code on the feature branch, making regular commits with the usual commands: ```git add .```, ```git commit -m "message"```. It's also important to push the feature branch to the remote repository. This allows other team members to view/review the progress of the feature branch. For example, ```git push -u origin new-menu-feature```.
 4. Other team members might review the commits. Changes are made locally in response to any feedback and then pushed back up to the remote feature branch. 
 5. When the developer has finished developing the feature they commit their recent changes locally and push back up to the remote feature branch. They then file a pull request to merge the new branch onto the main codebase. This triggers a review by other developers, including one or more senior developers to review the code before it is merged into the main branch.
 6. Once all feedback regarding the new feature has been addressed and the pull request has been accepted, the developer (on their local machine) can merge the feature branch into the main codebase. This can be done by moving to the main branch, updating the local main inline with the remote (central) version and merging the feature branch onto the main branch. For example the following commands can be used to achieve this.   
    - Move to the main branch:```git checkout main```    
    - update the local version of main inline with the central version: ``` git pull```
    - merge the local feature branch onto local main: ```git pull origin new-menu-feature```
    - pushing all updates back to the central repository: ```git push```  
(Atlassian, 2022b)


