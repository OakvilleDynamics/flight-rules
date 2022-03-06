# GitHub Flight Rules

*Work in progress*

## FAQ

### What is this document?

This document provides a structure for anything that you should do when operating Git, GitHub, or any codebase within the organization.

Following this document or the guidelines of this document when things do go wrong can help you in the process of things breaking, or if you want to sharpen your Git skills

There will also be examples used from archived repositories from competitions past to ensure consistency.

## Commits

Commits are logs of changes that are submitted. Each commit has a title, a hash of the commit, and optionally a description. Once a commit is finished you can push it to a remote repository, such as GitHub if you want others to view your code. The process of making a commit involves these steps:

1. Saving work in your editor/IDE if not already saved
2. Open your Git client
3. Add your files to staging
4. Write a title and description of the work that you did
5. Commit changes
6. Push changes

### Writing a good commit

A good title in Git when looking at a list of changes is helpful for others to look at without diving into the codebase to look at each line that was modified. A title can include a general overview of what changes were made in a condensed form.

A good commit title should:

* Be 72 characters or less
* A small but general summary of changes
* Does not end with a period
* Use the commit message to list in detail how changes are made.
* Capitalized the beginning of the title

It should also make sense in a sentence, such as: If applied, this commit will `<subject line here>`

A good commit should also have a good message of what work has been completed. If someone were to go to a single commit but didn't want to look at all the code that has been added, modified, or removed, this is where the message of a commit comes in.

A good commit message should:

* List in-depth how changes have been made, such as why a change has been made
* Bullet points can be used to list changes as well
* Capitalize each bullet point and paragraphs
* Free of gramatical and spelling errors

If a commit referrs to an issue, you can add a reference to a commit, and with GitHub there can be a link that resolves to an issue.

### Examples of good commits

[OakvilleDynamics/FRC-Robot-Code @ main+b079758b82340762c84e5c892e3d886e596baba9](https://github.com/OakvilleDynamics/FRC-Robot-Code/commit/b079758b82340762c84e5c892e3d886e596baba9)

>**Changed power values, started combine reworking, more changes**
>
>- Added constants for values that will never be changed, such as motor values for the port
>- Manifested Combine subsystems and commands
>- Reduced the maximum power output by the drive motors to 40%, or 0.4
>- Added some debugging statements for joysticks on the contollers
>
>The combine subsystems and commands do not work as of yet. The tank drive might also be changed out to another type of drive.

[OakvilleDynamics/FRC-Robot-Code @ main+4fc20f1eacd7f24ec28d91ea85d9e6c8477f7e79](https://github.com/OakvilleDynamics/FRC-Robot-Code/commit/4fc20f1eacd7f24ec28d91ea85d9e6c8477f7e79)

>**Major changes to controls, pneumatics, and combine systems**
>
>AUTHORING CREDITS: Flamingpuffins <flamingpuffins@gmail.com>
>
>- Controls are now working properly, as it was only grabbing the release state, not the pressed state
>- All pneumatics (Ramp and Button Press) are working properly
>- Inverted and slightly sped up the combine spin
>- Changed the combine port
>- Added some basic debugging to the subsystems
>- Formatting fixes
>
>There is some unfinished code that exists in the TankDrive as a speed curve, this is left in for future working

[OakvilleDynamics/ohsrobotics-gameelement-2020-2021 @ main+ce6691de5e4d6e9645453f6234126ba30baecf82](https://github.com/OakvilleDynamics/ohsrobotics-gameelement-2020-2021/commit/ce6691de5e4d6e9645453f6234126ba30baecf82)

>**Changing behavior when button is pressed early and minor changes**
>
>Instead of deduction a point when pressing the button too early, the behavior has been changed to reset the timer for the team itself.
>
>Minor changes:
>- Documentation is completed
>- Properly formatted code
>- Small refactoring to cleanup repeated code, as well as making some variables that do not change constant

### Examples of bad commits

[OakvilleDynamics/ftc-app-9328-2018-2019 @ master+884e043d48c206649db44a68512df3e32d53ab7d](https://github.com/OakvilleDynamics/ftc-app-9328-2018-2019/commit/884e043d48c206649db44a68512df3e32d53ab7d)
>**v0.1**
>
>Working

[OakvilleDynamics/FRC-Robot-Code @ main+621d4859cdc0f75acfda69f11ddf8a2606ef74a5](https://github.com/OakvilleDynamics/FRC-Robot-Code/commit/621d4859cdc0f75acfda69f11ddf8a2606ef74a5)

>**Cats Are Pretty Neat**
>
>Cats Are Pretty Neat + Turtles are cool!

