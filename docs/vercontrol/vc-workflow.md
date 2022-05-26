# Version control workflow
In this doc you can find general information 

## Table of contents
- [Making changes to the code](#making-changes-to-the-code)
    - [Branches](#branches)
    - [Commits](#commits)
    - [Pull Requests](#pull-requests)
    - [Quality Assurance](#quality-assurance)
        - [Bugs in production](#bugs-in-production)

## Making changes to the code
In order to make changes to the code and start contributing to achieve tasks we need to do, we follow a set of rules, based on [GitHub Flow branch strategy](https://www.bmc.com/blogs/devops-branching-strategies/#:~:text=What%20is%20a%20branching%20strategy,used%20in%20the%20development%20process.).

When a new implementation needs to be done **you must checkout from main** branch into a new branch that will be your development.

**Main** branch **MUST BE NOT** touched in any case presented. If a change is done within main, this must be reverte to the last Pull Request merge done.

### Branches
Name of the branches must be descriptive for the feature/implementation that will be done. We use [PascalCase](https://techterms.com/definition/pascalcase) notation for branch naming.

### Commits
Once important progress has been done a commit must be done. The commit message must be related to every change within the files that are being staged. In most of the cases, more commits mean a more readable and understandable code review; or in other words: **commits must be the atomic part of code changing**.

### Pull Requests
When development for a feature is done, a pull request must be done. This pull request must be descriptive and should contain any relavant information related to the changes done.

Ran tested cases must be included, in order to deliver Quality Assurance.

*The more information, the better*.

At least one reviewer must be assigned to the pull request. Once the code review and testing are done, the pull request can be completed.

### Quality Assurance
We ensure the deliver of this by reviewing code and testing any pull request (at least by 1 dev). Every test case must be documented (at least list all of them into the PR or GitHub discussion).

Before putting into production big changes, users should test new changes done.

#### Bugs in production
If a bug is found by the user and the test case was not included into the PR or discussion, the developer that made this changes should resolve this issue. Otherwise, if the problem was included in test cases, the dev that ran this test case should resolve the bug.

For bugs resolving, a *HotFix* branch must be opened.