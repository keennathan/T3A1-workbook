# NathanKeen_T3A1

# Q1	Provide an overview and description of a standard source control process for a large project:
For a large software project, a **standard source control process** should be structured, collaborative, and adaptable to ensure code quality, stability, and team efficiency.  Here's an overview of a typical process that leverages modern version control best practices:  

1. **Central Repository Setup:**  
    * Establish a **central code repository** on a distributed version control system like *Git*.  This serves as the "single source of truth" for all project code.  
    * Define a **main branch**(e.g. `main`, `master`, or `trunk`) to maintian the stable, production ready version of the software.  This branch reflects the latest version of the code that has passed all the testing stages and is ready for deployment.  
    * Create **developement branches** that represents various lines of active developement, such as features, releases, or bug fixes.  


2. **Branching Strategy:**  
    * Branching is key in managing concurrent workstreams across a large team.  Use a structured branching model to avoid conflicts and maintain clear workflows: 

        * **Feature Branches:**   

            - Each new feature,bug fix, or task is developed on its own branch(e.g. `feature/new-login-page`).  
            - Developers create a branch from the main or developement branch, keeping changes isolated until the feature is reeady.  
            - Combine feature branches with **feature flags** to deploy code incrementally and control the release of features in production without modifiying the main codebase.  

        * **Release Branches:**  
            - Used to prepare for a software release, starting from the main branch(e.g. `release/1.0`).  
            - All final changes and critical fixes for a release are applied here, ensuring stability and quality before deployment.  
            - After deployment, changes are merged back into the main branch and potentially into other release branches for maintenance.  

        * **Hotfix Branches:**  
            - Used to address critical production issues quickly.  These branches are created directly from the main branch(e.g. `hotfix/urgent-issue`) and merged back after fixes are tested.  

        * **Task Branches:**  
            - For agile teams, task or issue branches(e.g. `task/JIRA-123`) are tied to specific user stories or bugs tracked in a tool like Jira, providing better traceability and alignment with project management.  

3. **Pull Requests and Code Reviews:**
    * Developers submit **pull requests** to merge their branch into the main or developement branch.  
    * Code reviews are mandatory before merging, ensuring quality control and adherence to coding standards.  
    * Pull requests should be detailed descriptions of changes, relevent issue numbers, and testing results to facilitate effective reviews.  

4. **Continuous Integration(CI) and Automated Testing:**  
    * Implement a *CI pipeline* that automatically builds and tests new code when changes are pushed to any branch.  
    * Use automated tests to validate code quality, minimise integration issues, and ensure compatibility across branches.  
    * Successful CI tests signal that a branch is safe to merge, failing tests alert developers to conflicts or issues that must be resolved.  

5. **Merging and Integration:**  
    * Encourage frequent merging to keep branches up-to-date with the latest changes from the main branch and prevent large, complex merges later.  
    * Use *fast-forward* or *squash merges* for clean histories in the main branch and to make tracking changes easier.  
    * Developers regularly **pull updates** from the main branch to ensure their branch remains compatible and up-to-date.  

6. **Traceability and Documentation:**  
    - Maintain clear commit messages and link changes to issue tracking systems like Jira.  
    - Annotated histories help developers understand changes, root causes of issues, and long-term design evolution, making it easier to work effectively with legacy code or plan new features.  

7. **Release Management and Deployment:**  
    - **Release branches** undergo thorough testing and QA to ensure that code is production-ready.  
    - Implement *tagging* to mark specific releases(e.g. `v1.0`, `v1.1`), making rollbacks easier if needed.  
    - Deploy from release branches or main branches based on the project’s deployment strategy, using *continuous delivery(CD)* practices where applicable.  

8. **Post-Deployment Support:**  
    - After deployment, use hotfix branches to address urgent issues while keeping the main branch stable.  
    - Merge hotfixes into release and main branches to maintain consistency.  

## Summary 
A standard source control process for a large project is centered around structured branching, disciplined merging, rigorous testing, and collaborative workflows.  It ensures that changes are controlled, traceable, and integrated smoothly across development teams, enabling efficient scaling, faster development cycles, and reliable software delivery.  

### references 
* https://www.atlassian.com/git/tutorials/what-is-version-control  
* https://www.atlassian.com/agile/software-development/branching  
* https://www.dell.com/en-au/blog/best-practices-for-scaling-version-control-in-the-large-enterprise/


# Q2	What are the most important aspects of quality software?

Quality software is defined by how well it meets user requirements, performs its intended functions, and adapts to evolving needs.  It plays a crucial role in achieving business goals,improving user satisfaction,and ensuring long term success.  The following identifies the key aspects of quality software, based on fundamental software quality metrics and attributes.  These aspects encompass operational efficiency, transitional adaptability and ease of maintenance, offering a holistic perspective on what makes software effective and reliable.  
<br> 
![software characteristics](docs/softwareCharacteristics.png)

## Usability
Usability is a fundamental aspect of quality software, focusing on how easy and intuitive the software is for users.  Quality software should have a clean, user-friendly interface that requires minimal effort to navigate and understand.  When usability is prioritised, users are more likely to engage with the software, promoting user satisfaction and loyalty.  Strong usability not only drives higher adoption rates but also enhances customer retention and creates a positive user experience.  

* **Example:**
    - Consider a mobile app that features a clear, intuitive layout, allowing users to easily find and use its main features, such as browsing products, adding items to a cart, and completing a purchase within a few clicks.  This kind of user-friendly design promotes seamless interaction and satisfaction.

## Functionality  
Functionality ensures that the software performs as intended, delivering all required features and capabilities.  Quality software should be capable of executing its tasks accurately and reliably.  Functional software meets user expectations by offering a complete toolkit of features, making it effective for both individual users and businesses alike.  Functionality is integral to providing value, as it determines how well the software fulfills its core objectives.  

* **Example:**
    - An e-commerce platform that offers a well-designed checkout process illustrates good functionality. It consistently guides users through the necessary steps, allowing them to complete transactions smoothly and without errors.  

## Reliability
Reliability is the ability of software to perform consistently under specified conditions, handling faults and exceptions effectively.  Reliable software minimises system failures, data loss, and unexpected crashes, ensuring users can depend on it to complete tasks.  It promotes user trust, as it assures users that the software will work as intended, even in challenging environments.  Reliability is particularly critical for maintaining high levels of customer satisfaction and reducing downtime.  

* **Example:**
    - A cloud storage service that automatically backs up user data while handling potential errors gracefully without losing files demonstrates high reliability.  Users can trust that their files will be safe and accessible even during network interruptions.  

## Performance
Performance measures how efficiently software operates, including response times, processing speed, and resource utilisation.  High-performance software maximises system resources while maintaining optimal speed, even when handling large amounts of data or traffic.  Performance is crucial for providing a seamless user experience, as it affects how quickly users can complete tasks and interact with the software.  Efficient software also reduces operational costs, making it a vital component of business success.  

* **Example:**
    - A database management system that maintains fast query response times, even when handling large datasets, exemplifies strong performance.  Users can access and manage data quickly, improving productivity and overall satisfaction.  

## Security
Security is one of the most important aspects of quality software, given the increasing risks of cyber threats.  Quality software must protect user data and system resources from unauthorised access, ensuring confidentiality, integrity, and authenticity. It should include secure coding practices, encryption, and robust access controls to safeguard data. Strong security measures build user trust, prevent breaches, and ensure compliance with legal and regulatory requirements.  

* **Example:**
    - A banking app implementing two-factor authentication ensures secure access to accounts. This measure prevents unauthorised access, reinforcing users’ trust in the app’s ability to protect sensitive financial information.  

## Maintainability
Maintainability refers to the ease with which software can be updated, modified, and enhanced.  Quality software should have clear documentation, modular code, and a well-structured design that facilitates modifications.  It should be adaptable to evolving requirements and technological changes, minimising disruptions during updates. Maintainability reduces long-term costs, improves the efficiency of updates, and supports the software’s continued relevance.  

* **Example:**
    - A content management system with a modular codebase allows developers to add new features or make changes without disrupting existing functionality.  This setup supports ongoing improvements and helps maintain the software’s relevance in changing environments.  

## Flexibility
Flexibility measures the software’s ability to adapt to new requirements, technologies, or business processes.  Quality software is designed to accommodate changes, whether in business rules, regulations, or user needs.  It should allow for extensions, integrations, and modifications without compromising its core functionality.  Flexibility is vital for ensuring long-term usability, as it enables software to evolve with user demands and market trends.  

* **Example:**
    -  A project management tool that allows users to customise workflows, add new task types, and integrate various communication tools like Slack or Microsoft Teams without requiring significant changes to the underlying codebase.  This capability supports diverse team structures and evolving project requirements.  

## Scalability
Scalability is the capacity of software to handle increased workloads or expanded functionalities while maintaining performance.  Quality software should be designed to support both vertical scalability (adding resources to a single system) and horizontal scalability (adding more systems).  Scalable software can accommodate growth in user base, data volume, and functionality, making it a valuable asset for businesses aiming to expand or adapt quickly to changing market conditions.  

* **Example:**
    - A cloud-based customer relationship management system that can accommodate an expanding number of users and customer data without affecting response times demonstrates strong scalability.  

## Reusability
Reusability involves designing software components that can be reused in other projects or contexts.  Quality software includes common components, modules, or libraries that facilitate code reuse, reducing development time and costs.  Reusability supports faster iterations, streamlined development processes, and consistent functionality across multiple software solutions.  

* **Example:**
    - A library of standardised, well-documented APIs that can be used across multiple projects, reducing development time and ensuring consistency, is a prime example of reusability in software.  

## Testability
Testability is the ease with which software can be tested to ensure it functions correctly. Quality software is designed to allow for comprehensive testing, with clear criteria for validating its performance.  High testability reduces the risk of undetected bugs, ensures code quality, and enables quicker bug fixes.  It is critical for maintaining overall software reliability, as it helps developers identify and resolve issues before they affect users.  

* **Example:**
    - An application with automated unit tests and clear testing criteria allows developers to quickly identify and resolve issues during the development phase, enhancing the overall quality of the software.  

## Conclusion
The most important aspects of quality software encompass a blend of operational efficiency, adaptability, and ease of maintenance.  Usability, functionality, reliability, performance, security, maintainability, flexibility, scalability, reusability, and testability are crucial for delivering a robust software solution that aligns with user needs and business goals. By focusing on these aspects, software developers can ensure high-quality software that not only meets immediate requirements but also supports long-term growth, user satisfaction, and business success.

### references  
* https://www.softwaretestinghelp.com/what-are-the-quality-attributes/ 
* https://www.geeksforgeeks.org/software-engineering-characteristics-of-good-software/  
* https://www.softwaresuggest.com/blog/characteristics-of-good-software/
* https://getdx.com/blog/software-quality-metrics/  

# Q3	Outline a standard high level structure for a MERN stack application and explain the components




# Q4	A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?





# Q5	With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges






# Q6	With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature






# Q7	Explain control flow, using an example from the JavaScript programming language






# Q8	Explain type coercion, using examples from the JavaScript programming language







# Q9	Explain data types, using examples from the JavaScript programming language






# Q10	Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language






# Q11	Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language






# Q12	Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language