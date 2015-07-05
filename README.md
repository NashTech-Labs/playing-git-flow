# playing-git-flow
This repository shows the basic usage and effect of git-flow operations

git-flow are a set of git extensions to provide high-level repository operations for Vincent Driessen's branching model. It has attracted a lot of attention because it is very well suited to collaboration and scaling the development team.
Key Features:

    Git flow provides excellent command line help and output
    Git-flow is a merge based solution. It doesn't rebase feature branches
    One of the great things about GitFlow is that it makes parallel development very easy, by isolating new development from finished work
    Collaboration make it easier for two or more developers
    Better support for release staging area
    Support for emergency fixes at any time of development

Prerequisites:

    Need a working git installation. To install it check Installing Git
    Need a working git repository. We can use it in existing projects, but let's start a new repository: playing-git-flow

Installing git-flow:

Choose your platform:

    Mac OS X
    Linux (and Unix, etc.): We are using Ubuntu machine. So that install with below command

$ apt-get install git-flow

    Windows

Initialize git-flow:

Start using git-flow by initializing it inside an existing git repository:

You'll have to answer a few questions regarding the naming conventions for your branches.
It's recommended to use the default values.

$ git flow init

Which branch should be used for bringing forth production releases?
   - master
Branch name for production releases: [master] 
Branch name for "next release" development: [develop] 

How to name your supporting branch prefixes?
Feature branches? [feature/] 
Release branches? [release/] 
Hotfix branches? [hotfix/] 
Support branches? [support/] 
Version tag prefix? [] 
Hooks and filters directory? [/knoldus/playing-git-flow/.git/hooks] 

git-flow is just a wrapper around existing git commands, so the init command doesn't change anything in your repository other than creating branches for you. If you don't want to use git-flow anymore, there's nothing to change or remove, you just stop using the git-flow commands.

If you run git branch after setting up, you'll notice that you switched from the master branch to a new one named develop.

$ git branch
* develop
  master

The develop branch is intended to be the default branch where most of the work will happen, and the master branch keeps track of production-ready code. So instead of working in the master branch, you'll use git push origin develop to push new code to your repository from now on.
Feature branches: Let's start working with git-flow feature

    Start a new feature branchgit-flow makes it easy to work on multiple features at the same time by using feature branches. To start one, use feature start with the name of your new feature like below example: I have a github issue to update readme with git-flow information. So I am going to start new feature branch with that particular issue.

$ git flow feature start issue#1
Switched to a new branch 'feature/issue#1'

Summary of actions:
- A new branch 'feature/issue#1' was created, based on 'develop'
- You are now on branch 'feature/issue#1'

Now, start committing on your feature. When done, use:

     git flow feature finish issue#1

As the output already explains, you're now on a new branch you can use to work on your feature. Use git like you normally would, like add your development code and commit it on the same feature branch.



