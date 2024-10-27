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