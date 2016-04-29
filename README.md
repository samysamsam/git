# Git

## What is Git?
Git is a "Version Control System" that allows people to work together on the same project. It's clever "diffing" strategies helps avoid the confusion that tends to happen when multiple people are editing the same file.

## Why do we use it?
- Central source of truth
- We can sync our local version of a project with other versions
- Ensures against file corruption
- Allows multiple people to work on the same project at the same time
- We can rollback to previous versions easily
- We can work safely on potentially breaking changes to the project
- Encourages documenting smaller, modular changes

## How does it work?
Git uses "repositories" to track changes to a project over time. The repository is a collection of all the files and folders that make up a project as well as a list of all the changes that have happened in the project.

A good way of thinking about a repository is like a tree. Each tree has a singular trunk which in git is known as the "master branch" but usually just referred to as "master". You can create additional "branches" that stem off of the master branch—which is usually a good idea when working on a new feature of your project.

When "branching" you tell git which branch you'd like to start with (usually master) as well as the name of your new branch. Git will make a copy of that branch for you so you can make changes to your project without worrying about how your changes affect the master branch. When you're happy with all the changes you've made on your branch you can try to "merge" you changes back into the master branch.

"Merging" is kinda like reverse-branching. It lets you copy across all the changes from one branch into another. At the end of the merge you still have the two branches but now all the changes from one branch are in the other.

The first thing you'll do when working with an existing repository is "clone" into it. "Cloning" copies the current state of the directory to a new location that you specify. Usually this means creating a "local" copy of the directory that we can work on.

## Getting started
[https://git-scm.com/download](Download git)

## Exercise 1: Forking
1. Fork this repo by heading to [http://github.com/codewheel/git/](http://github.com/codewheel/git/) and clicking on the button in the top right of the screen that says "Fork".
2. GitHub should now redirect you to your own version of this repository located under http://github.com/USERNAME/git where USERNAME is your GitHub username.
3. Copy the link to your forked git repository by clicking the "Copy to Clipboard" icon visible beside the two download links.
4. Open the Terminal application on your computer
5. If you already have a Development directory you can `cd` into it
6. If you don't yet have a directory or folder for all your development files you can create one by doing the following:
  - Type `cd ~` and hit enter. "cd" stands for "change directories" so here we are asking the terminal to change directory to "~" which is just a shortcut to our root level user directory.
  - Next we'll create a development directory by typing `mkdir Development` and hitting enter. "mkdir" stands for "make directory" which is really just the same thing as creating a new folder.
  — Now that we have a Development directory we can change directories into it by typing `cd Development` and hitting enter. Your prompt should now have the location of your current directory as "~/Development"
7. Now we are in your development folder we are going to "clone" into our forked repository which simply means we will have a local version of the directory we can make changes to. Go ahead and type `git clone ` then paste in the location of our forked repository and press enter.
