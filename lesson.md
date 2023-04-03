## Brief

### Preparation

Familiarize with GitFlow, GitHub Flow and Trunk Base Development. Git CLI commands will be used in this lesson.

### Lesson Overview

This lesson aims to help learners understand the concepts of the common branching strategies and tell the differences between them. The lesson will also simulate GitHub flow where learners will be making changes to a code base and create pull request to the remote branch.

---

## Self-studies check-in:

**Q1: What is the difference between GitFlow and GitHub Flow?**

A: GitFlow uses `main` branch while GitHub flow uses `master` branch.

B: GitFlow uses `develop` branch while GitHub flow does not.

C: GitFlow uses HotFix branch while GitHub flow does not.

D: GitFlow uses pull request while GitHub flow does not.

**Q2: Trunk Based Development do not use feature or hotfix branches.**

A: True

B: False

---

## Part 1 - GitFlow vs GitHub Flow vs Trunk Based Development

### GitFlow
1. Start development by branching out a `feature` branch from the `develop` branch
1. Complete and test new feature in the `feature` branch
1. Merge `develop` branch into the `feature` branch to solve potential conflicts
1. Create a pull request from the `feature` branch to the `main` branch
1. Create a `release` branch from the `develop` branch
1. Perform fixes on `release` branch
1. Once stable, merge `release` branch into the `main` branch
1. Merge `main` branch into `develop` branch to kickstart new features

<img src='https://wac-cdn.atlassian.com/dam/jcr:8f00f1a4-ef2d-498a-a2c6-8020bb97902f/03%20Release%20branches.svg?cdnVersion=535' width='50%' />


### GitHub Flow
> Do everything without a `develop` branch.
1. Start development by branching out a `feature` branch from the `main` branch
1. Complete and test new feature in the `feature` branch
1. Merge `master` branch into the `feature` branch to solve potential conflicts
1. Create a pull request from the `feature` branch to the `main` branch
1. Create a `release` branch from the `master` branch
1. Perform fixes on `release` branch
1. Once stable, merge `release` branch back into the `main` branch

<img src="https://i0.wp.com/build5nines.com/wp-content/uploads/2018/01/GitHub-Flow.png" width="50%" />

### Trunk Based Development
> All developments must be small batch iterations and is directly pushed into the `main` (trunk) branch. 

Trunk Based:

<img src="https://cloud.google.com/static/architecture/devops/images/devops-tech-trunk-based-development-typical-trunk-timeline.svg" width="50%" />

Non-trunk Based:

<img src="https://cloud.google.com/static/architecture/devops/images/devops-tech-trunk-based-development-typical-non-trunk-timeline.svg" width="50%" />

---

## Part 2 - Case Study

Learners are given with a few scenarios. In a group of 3, the team is expected to suggest one branching strategy that is most applicable to the scenario and justify it by explaining the "why". Include any other assumptions that influence your team's decision.

After discussing the scenario, end with the final question posted at the end of this section.

---
### Scenario One - A Utility Mobile App

The utility app is a paid app. The team has received multiple feedbacks from the public about feature request and bug fixes. The team has produced a priority list to work on them. The priority of the feature releases have been frequently encountered changes. Such as, a feature might be planned to release in version 1.2.1, may be disrupted and change to a later release at times.

```
Your answer here
```

---
### Scenario Two - A Market Penetrating Product

A tech product company is planning to penetrate the market with their tech product developed in-house. They have spent money on marketing and advertisement, exciting the public users in anticipating the next release. There are also sales and account personnel meeting with potential customers to give demo. Not all latest features are included in the demo. 

```
Your answer here
```

---

### Scenario Three - A System Integration Project

At a system integrator company, the team received an A-Z requirements from a customer that has recently been signed off. There is a fixed set of requirements, timeline, and given manpower to complete the project.

```
Your answer here
```

---
Final Question: How these branching strategies affect DevOps?
```
Your answer here
```
---

## Part 3 - Simulate a GitHub Flow

In this section, we will simulate a simplified GitHub flow using [this](https://github.com/su-ntu-ctp/6m-software-4.1-lesson-exercise) sample repository.

Step 1: Fork the repository

Step 2: Create a new branch `Feature-<your initial>-test` (the goal is ensuring all branches are unique).

Step 3: Clone the forked repository to your local machine

```sh
git clone <url>
```

Step 4: Check out your branch locally
```sh
git checkout <branch name>
```

Step 5: Edit the `readme.md` file

Step 6: Add, commit and push changes to the forked repository
```
git add .
git commit -m "type a meaningful message here"
git push origin <branch name>
```

Step 7: Go to `https://github.com/your_username/6m-software-4.1-lesson-exercise` to create a Pull Request from your branch to the `main` branch of `https://github.com/su-ntu-ctp/6m-software-4.1-lesson-exercise`.

Step 8: Instructor to demonstrate merging the pull request into the `main` branch.
