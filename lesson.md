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

<Insert scenario 1 - learners to propose a branching strategy>

<Insert scenario 2 - learners to propose a branching strategy>

Question: How these branching strategy affect DevOps?

---

## Part 3 - Simulate a GitHub Flow

<Prepare a repo to work on this>
