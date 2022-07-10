# Oakville Dynamics FRC Robotics Git/GitHub Flight Rules

This document will cover all the basic usages of Git, and the platform GitHub, as well as general practice implementations and keeping good documented code and treating such repositories as cleanly and orderly as possible.

## Table of Contents

- [Oakville Dynamics FRC Robotics Git/GitHub Flight Rules](#oakville-dynamics-frc-robotics-gitgithub-flight-rules)
  - [Table of Contents](#table-of-contents)
  - [FAQ](#faq)
    - [Q: What is this document?](#q-what-is-this-document)
    - [Q: Can there be a section on _x_?](#q-can-there-be-a-section-on-x)
    - [Q: Will there be any coverage on using a Git terminal or a Git client that has a GUI?](#q-will-there-be-any-coverage-on-using-a-git-terminal-or-a-git-client-that-has-a-gui)
    - [Q: I notice an error, can I fix it?](#q-i-notice-an-error-can-i-fix-it)
  - [Basics of Git](#basics-of-git)
    - [What is Git?](#what-is-git)
    - [How do I save changes?](#how-do-i-save-changes)
    - [What is GitHub?](#what-is-github)
    - [How do I work with other people?](#how-do-i-work-with-other-people)
    - [How do I get my code to be on the main branch?](#how-do-i-get-my-code-to-be-on-the-main-branch)
    - [Simplified definitions](#simplified-definitions)
  - [General Process from start to finish](#general-process-from-start-to-finish)
  - [Commits](#commits)
    - [Structure](#structure)
    - [Writing a good commit](#writing-a-good-commit)
      - [Examples of good commits](#examples-of-good-commits)
      - [Examples of bad commits](#examples-of-bad-commits)
    - [When to make a commit](#when-to-make-a-commit)
    - [Commit != Push](#commit--push)
  - [Branches](#branches)
    - [Managing branches](#managing-branches)
    - [When to merge a branch](#when-to-merge-a-branch)
      - [Pull Requests](#pull-requests)
      - [Merging directly into main](#merging-directly-into-main)

## FAQ

### Q: What is this document?

This document provides a structure for anything that you should do when operating Git, GitHub, or any codebase within the organization.

Following this document or the guidelines of this document when things do go wrong can help you in the process of things breaking, or if you want to sharpen your Git skills

There will also be examples used from archived repositories from competitions past to ensure consistency.

### Q: Can there be a section on _x_?

There can if there is enough of a reason to include in the basic Git Flight Rules or if is important and not currently covered by the current set of Flight Rules.

For you to suggest a section:

1. Create an issue on the repository
2. Write a descriptive and source of this new added section
   1. If you already have made the additions and you want to submit them, you can submit a pull request and have the changes review
3. Wait for an official and orderly response to include the new section into the Flight Rules.

### Q: Will there be any coverage on using a Git terminal or a Git client that has a GUI?

There will be basic inclusions of getting basic operations on how to deal with Git and GitHub in a specific client. For the time being, this set of flight rules will only have documentation on how to use GitHub Desktop, which is a free Git client that anyone can download on Windows and macOS.

Basic commands will also be included on how to run basic commands into a Git terminal as a reference.

### Q: I notice an error, can I fix it?

Create an issue, if you want to fix it yourself you can make a pull request. Make sure you lint the project with `markdownlint` to ensure formatting documents.

## Basics of Git

### What is Git?

Git is a tool that allows for code to be saved in a manner where there is versioning, such as `v0.1`, `v0.2.1`, etc., and is self containing. No extra folders that have to be renamed, it does the job for you.

### How do I save changes?

When you want to save a change that you have made, it is called a `commit`. A commit tracks the changes that you have made to what was previously there, and keeps a running history of every single change on every single line.

Saving with Ctrl+S/⌘+S just saves normally, this does not save in Git. You need to tell Git to commit those changes, therefore it is saved in Git.

### What is GitHub?

Git is merely the tool, but GitHub is the "Google Drive" of code, where you can share your code with others and work on it simultaneously. This location is called a `repository`.

Once your code is committed, you can `push` your changes to GitHub, where everyone that has access to your code can work off of your changes.

### How do I work with other people?

To have others code on your local machine to test and tweak, you can `pull` from GitHub, which just pulls all the changes made to your computer.

All you need to work with people on GitHub is a GitHub account.

Think of a tree, there are branches on a tree, it all stems back into the main branch that is the source of the whole tree. This can be translated into a repository, a `branch` is a clone of the main branch on the tree, or another branch entirely, and is separate. This is helpful when working with others as new features or fixing bugs can be tested in its own sandbox.

### How do I get my code to be on the main branch?

You can combine branches back into the main branch either with a merge or a pull request.

### Simplified definitions

- Git
  - A special tool that saves all changes for all code written from history
- GitHub
  - Google Drive for code, you can share and collabrorate online with just sending a link and browse others code for inspiration and brainstorming
- Commit
  - A savepoint for code
- Push
  - Submitting your code to a GitHub repository, so others can look and collaborate on your changes
- Pull
  - Retrieving changes made from a GitHub repository, if someone were to make changes and you want to be current and up to date on what you are working on
- Repository
  - If GitHub is Google Drive for code, A repository is a Google Doc for code
- Branch
  - Separate copies of the main code, can be used to add new features, fix bugs, or other major changes

## General Process from start to finish

This section outlines what actions should be done when clocking in to work and clocking out when work is finished for the day.

1. Pull changes from current robotics repository
2. Ask around what everyone is working on as well as what needs to be done for you if progress has been made, check chats if there has been mentions of you or code to get working or added
3. Make changes
4. Commit changes
5. Repeat steps 3-4 until packing up
6. Push all changes to repository

Once you have pushed everything to the repository, others are able to view work and can work with your code if you are absent from a build session or working remotely.

## Commits

Commits are logs of changes that are submitted. Each commit has a title, a hash of the commit, and optionally a description. Once a commit is finished you can push it to a remote repository, such as GitHub if you want others to view your code. The process of making a commit involves these steps:

1. Saving work in your editor/IDE if not already saved
2. Open your Git client
3. Add your files to staging
4. Write a title and description of the work that you did
5. Commit changes
6. Push changes

### Structure

Each commit has a defined title and an optional description. This will contain all notes, changes, fixes, removals, etc. to not only yourself, but other contributors.

### Writing a good commit

A good title in Git when looking at a list of changes is helpful for others to look at without diving into the codebase to look at each line that was modified. A title can include a general overview of what changes were made in a condensed form.

A good commit title should:

- Be 72 characters or less
- A small but general summary of changes
- Does not end with a period
- Use the commit message to list in detail how changes are made.
- Capitalized the beginning of the title

It should also make sense in a sentence, such as: If applied, this commit will `<subject line here>`

For example, A commit may be titled `Update time function, Gradle libraries, refactor async methods`.

A good commit should also have a good message of what work has been completed. If someone were to go to a single commit but didn't want to look at all the code that has been added, modified, or removed, this is where the message of a commit comes in.

A good commit message should:

- List in-depth how changes have been made, such as why a change has been made
- Bullet points can be used to list changes as well
- Capitalize each bullet point and paragraphs
- Free of gramatical and spelling errors

If a commit referrs to an issue, you can add a reference to a commit, and with GitHub there can be a link that resolves to an issue.

#### Examples of good commits

Each section of new commits will show a link to the specific commit on the GitHub repostitory, as well as including the title as well as a description on what the commit is in detail.

This can be both informative as well as accurate to include as good enough detail as what could be changed for a better commit.

Commit quality is subjective and can change from one person to the next, but a general rule of thumb is more detail in the commit the better.

[OakvilleDynamics/FRC-Robot-Code @ main+b079758b82340762c84e5c892e3d886e596baba9](https://github.com/OakvilleDynamics/FRC-Robot-Code/commit/b079758b82340762c84e5c892e3d886e596baba9)

> **Changed power values, started combine reworking, more changes**
>
> - Added constants for values that will never be changed, such as motor values for the port
> - Manifested Combine subsystems and commands
> - Reduced the maximum power output by the drive motors to 40%, or 0.4
> - Added some debugging statements for joysticks on the contollers
>
> The combine subsystems and commands do not work as of yet. The tank drive might also be changed out to another type of drive.

| Why this commit is considred 'good'     | Why this commit is considered 'bad'                                                                  |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Decscriptive title                      | Title does not have proper formatting                                                                |
| Outlined all changes made into a commit | Bullet points are not needed or misplaced unless rapid-firing minor changes or outlining new feature |
| Included a general summary              |                                                                                                      |

[OakvilleDynamics/FRC-Robot-Code @ main+4fc20f1eacd7f24ec28d91ea85d9e6c8477f7e79](https://github.com/OakvilleDynamics/FRC-Robot-Code/commit/4fc20f1eacd7f24ec28d91ea85d9e6c8477f7e79)

> **Major changes to controls, pneumatics, and combine systems**
>
> AUTHORING CREDITS: Flamingpuffins <flamingpuffins@gmail.com>
>
> - Controls are now working properly, as it was only grabbing the release state, not the pressed state
> - All pneumatics (Ramp and Button Press) are working properly
> - Inverted and slightly sped up the combine spin
> - Changed the combine port
> - Added some basic debugging to the subsystems
> - Formatting fixes
>
> There is some unfinished code that exists in the TankDrive as a speed curve, this is left in for future working

| Why this commit is considered 'good'                                       | Why this commit is considered 'bad'             |
| -------------------------------------------------------------------------- | ----------------------------------------------- |
| Title introduces the changes properly                                      | Title is a bit vague                            |
| Consise bulleted list                                                      | Some of the list could be written as paragraphs |
| Outlines possible future fixes or other changes that need to be made       |                                                 |
| Mentions proper authoring credits if someone else did not write the commit |                                                 |

[OakvilleDynamics/ohsrobotics-gameelement-2020-2021 @ main+ce6691de5e4d6e9645453f6234126ba30baecf82](https://github.com/OakvilleDynamics/ohsrobotics-gameelement-2020-2021/commit/ce6691de5e4d6e9645453f6234126ba30baecf82)

> **Changing behavior when button is pressed early and minor changes**
>
> Instead of deduction a point when pressing the button too early, the behavior has been changed to reset the timer for the team itself.
>
> Minor changes:
>
> - Documentation is completed
> - Properly formatted code
> - Small refactoring to cleanup repeated code, as well as making some variables that do not change constant

| Why this commit is considered 'good'         | Why this commit is considered 'bad'                  |
| -------------------------------------------- | ---------------------------------------------------- |
| Explained new behavior changes in the commit | Mention of minor changes is a bit vague in the title |
| Minor changes is concise and specific        | Title is not in "proper" formatting                  |

#### Examples of bad commits

Bad commits are easy to find and pick apart. These examples of such commits are where there are recorded bad commits.

Lack of detail or massive changes with something basic to describe the changes are very bad.

[OakvilleDynamics/ftc-app-9328-2018-2019 @ master+884e043d48c206649db44a68512df3e32d53ab7d](https://github.com/OakvilleDynamics/ftc-app-9328-2018-2019/commit/884e043d48c206649db44a68512df3e32d53ab7d)

> **v0.1**
>
> Working

| Why this commit is considered 'good'               | Why this commit is considered 'bad'         |
| -------------------------------------------------- | ------------------------------------------- |
| If versioning changes, this is at least an attempt | Commit title is vague                       |
|                                                    | Description has nothing on what has changed |

[OakvilleDynamics/FRC-Robot-Code @ main+621d4859cdc0f75acfda69f11ddf8a2606ef74a5](https://github.com/OakvilleDynamics/FRC-Robot-Code/commit/621d4859cdc0f75acfda69f11ddf8a2606ef74a5)

> **Cats Are Pretty Neat**
>
> Cats Are Pretty Neat + Turtles are cool!

| Why this commit is considered 'good' | Why this commit is considered 'bad'   |
| ------------------------------------ | ------------------------------------- |
|                                      | Not at all relevant to the repository |

### When to make a commit

Git only takes responsibility with your changes once you have made a commit. If you forget to make a change, and something happens with your project, then work can be lost. It is highly recommended to commit as often and as early as you can **locally**. Once you have finished your changes and are ready to push, you can squash them into one single commit or push them all into the repository on GitHub.

You should commit when a change that you make still compiles, such as changing a variable name, extracted a method, or changed a conditional statement. Following this is process is committing early, and committing often.

### Commit != Push

A commit is just a log of changes on a repository, a push uploads your changes to GitHub or another repository. This is important as just committing those changes you've made are not automatically synced up to GitHub for others to look at and work on.

If you are clocking out for the night and you have commits that needs to be pushed, you should push them before you clock out. This is important as others can look at the work you have done, as well as if the computer you have worked on stops working, the changes you have made are not permanently lost.

## Branches

Branches allow you to develop features, fix bugs, or safely experiment with new ideas in a contained area of your repository. You can create branches of branches, and you can merge branches back into the main branch of the repository. Branches can be named anything, however they should be descriptive as to what is being done in the branch.

You can have an infinite amount of branches, as well as you can create "folders" of branches when you create a branch with the format of `[name-of-folder]/[name-of-branch]`, such as `feature/computer-vision`, `bugfix/gradlerio`, etc.

In a regular development environment, you have folders of branches that encompass lots of the changes as well as two main branches, which are considered the `main` branch or `dev` branch.

The `main` branch is the main branch, this should always be the stable branch, as this is what is considered 'production' and general uses. Commits directly to the `main` branch are frowned upon unless starting a repository and getting things all setup for others or yourself to start working.

The `dev` branch is the main development branch. This is where your new features or fixes are made, and this is considered stable but not 'production-ready'. This is due to new features and fixes can possibly have adverse effects on already existing environments. New features and fixes should be based off of this branch unless needed to be dispatched immediately. These features or fixes should be their own branches with a folder referencing the type of implementation. Once new feature is merged into the `dev` branch, you can pull request it into the `main` branch if everything is all stable and ready for a general release.

Folders should be mainly comprised of overarching types of changes, such as `feature/` or `bugfix/`, as those are used to tell what the branch is supposed to be. A good example for a new feature is if someone was adding a feature to use a webcam for computer vision, a branch could be called `feature/computer-vision`, or if you were fixing a bug with power levels being too high or too low for a motor, a branch can be called `bugfix/motor-power`.

A lifecycle of a branch is as follows:

1. A new branch is created off of lastest `dev`
2. Work is gone into new branch, adding or changing, or removing code as needed
3. Once new branch is complete, merge branch into `dev`, and delete the created branch
4. Once branch is merged into `dev` and ready for a general production release, create a pull request to `main` outlining all changes made
5. Once the pull request is approved, it will be merged into `main`, and a commit will be made with all the changes
6. Merge `main` back into `dev` for sanity checking

### Managing branches

You should only have branches when you are fixing a bug, developing a new feature, or for experimentation. Once the task is done, you can merge it into the main branch.

The reason to have a separate branch for developing bugfixes, features, or implementing new ideas is to have the main branch as stable as possible. The main branch is what will most often be used in production environments, as well as if other features or bugfixes are needing to be developed, the main branch can be used as a good baseline for developing the feature or bugfix.

### When to merge a branch

Merging a branch is to be performed when the feature, bugfix, or other work that has been done is complete, stable, and is ready to deploy. This can either be done in one of two processes, either a pull request or just directly merging into the main branch.

#### Pull Requests

Making a pull request is what many companies use as a check for software development. This adds a code review process to vet whether or not a branch is going to be approved into the main branch. You can offer critiques or other notes to go back and improve on, or you can approve the merge.

Once approved you can merge it into the main branch. There can be automated tools that also check for code quality, styling, or other issues.

This method is recommended for working on big multi-developer projects, as well as to get into the habit of processes from employers and general sanity checking if code will actually work.

A pull request should be treated as a commit, where you can describe what changes have been made and why this should be merged if this is a new feature to be added.

#### Merging directly into main

Merging directly into the main branch is also an option, this is useful if you are the single developer working on a project, however if you are working on a project with multiple developers then things can get messy very quick with merge conflicts, things breaking, and other nasty issues that can creep out and ruin a merge.

This method is not recommended unless you're a single devloper working on a project.
