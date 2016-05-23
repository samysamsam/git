# Git

## What is Git?
Git is a "Version Control System" that allows people to work together on the same project. It's clever "diffing" strategies helps avoid the confusion that tends to happen when multiple people are editing the same file. It also helps us keep track of all of the changes made over the course of a project’s life.

## Why do we use it?
- Central source of truth
- We can sync our local version of a project with other versions
- Ensures against file corruption
- Allows multiple people to work on the same project at the same time
- We can rollback to previous versions easily
- We can work safely on potentially breaking changes to the project
- Encourages documenting smaller, modular changes

## How does it work?
Git uses "repositories" to track changes to a project over time. A repository is a collection of all the files and folders that make up a project as well as a list of all the changes that have happened in the project.

A good way of thinking about a repository is like a tree. Each tree has a singular trunk which in git is known as the "master branch" but usually just referred to as "master". You can create additional "branches" that stem off of the master branch—which is usually a good idea when working on a new feature of your project.

When "branching" you tell git which branch you'd like to start with (usually master) as well as the name of your new branch. Git will make a copy of that branch for you so you can make changes to your project without worrying about how your changes affect the master branch. When you're happy with all the changes you've made on your branch you can try to "merge" you changes back into the master branch.

"Merging" is kinda like reverse-branching. It lets you copy across all the changes from one branch into another. At the end of the merge you still have the two branches but now all the changes from one branch are in the other.

The first thing you'll do when working with an existing repository is "clone" into it. "Cloning" copies the current state of the directory to a new location. Usually this means creating a "local" copy of the directory that we can work on.

When working locally git helps us to focus on our work by tracking changes to a branch in three different areas:
- "Working Directory" which holds all the actual files of our branch
- "Index" which acts as a staging area for making notes about the changes before we commit them
- "HEAD" which points to the last commit that we made

## Getting started
[Download git](https://git-scm.com/download)

## Exercise 1: Forking
1. Fork this repo by heading to [http://github.com/codewheel/git/](http://github.com/codewheel/git/) and clicking on the button in the top right of the screen that says "Fork".
2. GitHub should now redirect you to your own version of this repository located under http://github.com/USERNAME/git where USERNAME is your GitHub username.

## Exercise 2: Cloning
1. Copy the link to your forked git repository by clicking on the green "Clone or download" button then copying the url of the repository or by simply clicking the "Copy to Clipboard" icon.
2. Open the Terminal application on your computer.
3. If you don't yet have a directory or folder for all your development files you can create one by doing the following:
  - Type `cd ~` and hit enter. "cd" stands for "change directories" so here we are asking the terminal to change directory to "~" which is just a shortcut to our root level user directory.
  - Next we'll create a development directory by typing `mkdir Development` and hitting enter. "mkdir" stands for "make directory" which is really just the same thing as creating a new folder.
4. Change directories into your development folder by typing `cd ~/Development` and hitting enter. Your prompt should now have the location of your current directory as "~/Development".
6. Now we are in your development folder we are going to "clone" into our forked repository which simply means we will have a local version of the directory we can make changes to. Go ahead and type `git clone`, then a space, then paste in the location of your forked repository before hitting enter.

## Exercise 3: Committing
1. If all went to plan you we should now have a new folder in our "Development" directory called `git`. Change directories into it by typing `cd git` and hitting enter. This is our "Working Directory". If we open up `git` in the finder we can see that it contains a single file named `README.md`.
2. Open up `README.md` file. You'll notice it has a strange way of formatting paragraphs, titles and lists. That's because this file is a markdown file.
3. Scroll to the bottom of the file and add your name on a new line to the list of successful gitters visible at the bottom of the list.
4. Open up your Terminal application again. You should still be in the `git` folder but if you aren't you can simply change directories into it by typing `cd ~/Development/git` and hitting enter.
5. Now we'll commit the changes we made to our local version of the `README.md` file. First we need to add the file to git's staging area or "Index". We can add all the files that have changed in our working directory by typing `git add .`. We could also just add one file `git add PATH/TO/FILE` where "PATH/TO/FILE" would be replaced by the location of the file we want to add. Let's add our file by typing `git add README.md` and hitting enter.
6. Great now our README file is in the staging area and ready to be committed. Every commit we make is accompanied by a short "commit message" about the changes we have made. A good commit message should let other people working on the project know what changes to the files you made and why you made them. For now we can type `git commit -m "Added my name to list of successful gitters"` and hit return. "-m" here stands for "message" and the quotations marks around the message lets git know when the message starts and when it ends.

## Exercise 4: Pushing
1. Although we have now committed our updated README file to the HEAD of our local version of the repository, nobody else will be able to see our changes until we let the "remote" repository know about the changes we've made. In this case we can share our changes by "pushing" them "up" to the repository we made on GitHub in exercise 1.
2. To tell git where we want the commit we firstly need to say which remote repository we want to receive our changes as well as the branch that they belong to. By default git calls the original location that we cloned the repository from the "origin" remote. We've made all our changes on the "master" branch so to let GitHub know about the changes we simply need to type `git push origin master` and hit enter.
3. Now if we reload our repository on GitHub and scroll down to the bottom we should see our name added to the list of successful gitters.

## Successful gitters
- Sam Margalit
