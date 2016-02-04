# Collaborative working with github - for non-programmer beginners


## How do you track changes to directories (i.e. the documents they contain)

### The traditional way (without a version control software)

  * How do you know who created a particular version of a document (file created  by times are not reliable because the time a file was first saved on the   current device is not necessarily the actual creation date)?
    - Use an appropriate naming convention (rarely adhered to in large teams)
  * How do you know when a document version was created (file created by times  are not reliable because the person who saved the file on the current device   is not necessarily the original author)?
    - Use an appropriate naming convention (rarely adhered to in large teams)
  * How do you revert to an earlier version of a document?
    - Keep a copy of the earlier version, and delete later versions (but then  you can't go back to the deleted versions).
  * How do you keep a track of changes
    - Use track changes feature if using MS office, or you can't
  * How do you prevent public read access to a document
    - Store it in a restricted drive
  * How do you prevent public write access to a document whilst allowing read   access
    - password protect it (if using MS Office) or you can't
  * How do you require approval changes to the master version of a document
    - Password proted it (if Office document) and/or store it in a restricted   drive, which only certain people have access to.
  * How do you know who changed a document last (file modified dates are not  reliable)
    - Restrict write access to one person. That person is the person who amended it (unless that person person changes over time, in which case you're screwed.
  * How do you circulate a version of a document to a group of people?
    - email? slack? Or present at a meeting
  * How do you get feedback from a group of people?
    - email? slack? Comments (if using MS Office) or review together in a meeting
  * How do you record who approved changes to a document?
    - A change log, manually maintained.
  * How do you handle multiple simultaneous updates to a file?
  - Last change overwrites earlier changes, with no way to pick and choose particular changes made by other people.

### A better way

Alternatively, use a version control system like subversion, MS sharepoint, or ... git.


## What is git?

Git is version tracking system (aka a version control system), particularly well suited to collaborative working.

Git was created in 2005 by Linux developers (including the famous Linus Torvalds) to manage collaborative development of Linux.


## What is git used for?

Git is most commonly used to track software projects, but it can be used to track changes to almost any text based documents (or collection of such documents). For example, the drafting and redrafting of books has been helped by using git.


## What is a git repository?

"Git repository" is a term used to refer to a directory (aka folders) you've asked git to track. (Technically the git repository is a hidden sub-folder within the directory, which git uses to track the changes to that directory, but in everyday usage this distinction is unimportant.)

Tracking directories does not alter the way you use them.

Git repositories (aka tracked directories) are also sometimes called "repos": short for repositories.

With git you can:
  * save a version of the directory (without cluttering the directory up with lots of extra files)
  * view the history of changes to files and directories
    - who made exactly what changes
    - when changes were made
  * revert changes you don't want



## Do I need to use terminal commands to use git?

No, just use Github and Github Desktop, which are user friendly intefaces to git, the underlying system.

There are numerous advanced things you can only do from the command line in a terminal window, but these are rarely needed by non-developers.



## Terminology quick translation

**Normal English     =>  Git/Github terminology**

a tracked directory                            =>  a repository (aka a repo)
download a directory from github               =>  clone repository (aka clone)
a version                                      =>  a version
save a set of changes and create a new version =>  commit changes
a set of changes that created a version        =>  a commit
a tag for one or more sets of changes          =>  a branch
a change proposal                              =>  a pull request
a comment on proposed changes                  =>  a comment
approve/accept proposed changes                =>  merge branch
reject proposed changes                        =>  close pull request
sync with github                               =>  fetch (aka sync)
publish/upload to github                       =>  push
get other people's changes                     =>  pull


## What is Github?

Github is a a website for publishing/sharing git repositories.

Github also provides it's own workflow for collaborating on changes to repositories: i.e. reviewing and approving changes. This was one of the unique selling point that has made github so popular.

Through Github, teams of people can
 * upload/download copies of directories to share them with others and to use as a backup directory.
 * view/navigate directories and files you have access to in a similar way to how you view and navigate files and directories on your local computer
 * view the history of changes to files and directories
    - who made exactly what changes
    - when changes were made
    - who commented on the changes, when they commented, and what they said
    - who approved the changes and when
 * submit a change proposal
    - showing line by line what changes are being proposed
    - proposals can have a description of and justification for the changes
 * review proposed changes
    - see exactly what changes are being proposed
    - see the stated reasons for the changes
    - comment on changes (including commenting line by line)
    - reply to other comments
 * formally accept or decline proposed changes
 * apply various restrictions on access to directories (paid accounts only)

(Github even allows you to change text files on its site, but only if you want: you don't have to do this).



## The Github Workflow

1. Make changes to a repository (aka a git tracked directory)
2. Create/select a



## How to install Github desktop

Go to https://desktop.github.com/
Click "Download"



## How to download an entire repository from Github

Remember that repositories are simply directories tracked by git, and github repositories are just copies of directories, stored on github, and tracked by git.


## Step 1: Select a github repository to download

The git term for downloading a repository from github is "cloning".
Choose "Clone repository" from the file menu

All the repositories you have access to on github are listed.
You can search by repository name.
Select the repository you want (only the ones you have access to are shown)


## Step 2: Download

Click the "Clone [repository name]" button. Remember that the git term for downloading a repository from github is "cloning".
Choose where to download (aka clone) the repository to.
Click Clone button



## How to the see the history of changes

Every time a new version of the directory is stored, git records something called a "commit". Each commit is a record of the changes (i.e. changes to the files) that were associated with the creation of a new version of the directory. You can view the changes associated with each version by examining the history (aka the commit history).


### Step 1: Select a label name (aka branch)

Remember that the git term for a label is "branch"
Remember that changes you store (aka commit) are associated with a label you set up. (Even if you forget to associate them with a label your changes still get labelled with the "master" label).
Remember also that git's name for labels is "branch".

Select the label (aka branch) you're interested in from the drop down at the top of the screen.


### Step 2: View the history

Select "History" from the "View" menu.

When you first select history, only the most recent change associated with the selected label (aka branch) is shown.

Click the button "View Branch" to see all the earlier changes.

On the left of the screen are the list of commits associated with the selected label (aka branch); newest changes appear at the top.


### Step 3: View changes for a commit

Click a commit to see the set of changes included in that commit.

The exact changes included in the selected commit will appear on the right of the screen. Lines that have been removed show in red and lines that have been added show in green.



## Label your changes

The first thing you should do, before you even commit to any changes, is create a label for your changes.

As you store your directory changes you will associate them with this label, and then later that label will be applied to the change proposal that you submit for approval by your colleagues.

In git, the proper term for a label like this is a "branch".


### Step 1: Naming your new label (aka branch)

Select "New Branch" from the "File" menu

Enter a meaningful name that briefly encapsulates what your changes will be about.


### Step 2: Make sure you're starting "from" master

The "master" label/branch always points to the current master version of the directory. The current master version of the directory contains all the the approved changes to date.

Make sure the "from" field says "master". This tells git that you are intending your changes to be applied to the master version of the directory (and not some other random version).


### Step 3: Finish creating the label (aka branch)

Click the "Create Branch" button

Now you've created your label for the set of changes you are intending, the changes you make and any new directory versions created as a result of those changes will automatically be associated with that label/branch. This will be useful later when you come to submit your changes for approval.


### Step 4: Publish you label

Click the "Publish" button in the top right corner of the screen.



## Make the changes you want


### Step 1: Sync with Github

Make sure that you're up-to-date with everyone else's changes, by syncing with github. The git term for syncing is "fetching". (Sync regularly to avoid problems that can only be fixed on the command line.)

Click the Sync button.


### Step 2: Select your label

Always remember that changes you store in git must always be associated with a label (aka a branch).

In the drop down at the top of the screen, select the label (aka branch) to which you want to associate your changes. It is important that you select the correct label: i.e. the one that corresponds to the directory version you want to make amendments to. If you've just created a label: that one.


### Step 3: Get other people's changes

If other people have made any changes using the same label as you're using (aka on the same branch) you should combine their changes with your work by "pulling" in changes.

The select "Pull" from "Repository" menu.


### Step 4: Change files as required

Change any files as you would normally, and save them as you would normally.



## Store changes (aka make a commit) and a new version of the directory


### Step 1: Review this current set of changes

Select "Uncommitted changes" from the "View" menu.

On the left of the screen are a list of files that have been changed.
Select a file, and then, on the right of the screen, are the details of the changes to that file. Lines that have been removed are shown in red and lines that have been added are shown in green.

Make sure you're happy with all the changes before carrying on.


### Step 2: Store changes (aka make a commit)

The git term for storing a set of changes is "committing the changes". At the same time git stores the changes, a new version of the directory is also stored.

Fill in the form at the bottom left of the page to store (aka commit) your changes.

  1. Enter a short description of the changes in the "Summary" field. It is best practice to use the *present imperative tense* (e.g. "add such and such", "Make it clear that this is that", "Remove unnecessary lines about such and such")
  2. Enter a longer description in the "description" field. It is best practice to outline the actual reasons for these changes here.
  3. Click the button "Commit to [branch name]".

The changes you've made are now stored (aka committed), and git has also stored a new version of the directory, which you can return to at a later date if you want.



## Publish and backup your changes to github

The git term for publishing your changes is "pushing".

Make sure you the right lable (aka branch) is selected.
Then click the "publish" button in the top left of the screen.



## Open the repository on GitHub

Select "View on GitHub" from the "Repository"
The repository will open on github in your browser.



## Create a change proposal (aka a pull request)

Github allows you to propose changes so that others in your team can review, comment, and either accept or reject.

The github term for a change proposal is a "pull request".


### Step 1: Start new pull request

On GitHub click the button "New pull request"


### Step 2: Select the label (aka branch)

At the top of the screen in the "compare: master" select box select your label.


### Step 3: Review the changes

Scroll down to review the changes: line by line or commit by commit. If you're happy continue.


### Step 4: Write a description

Write a description of the changes, including any reasons why you think the changes are necessary.


### Step 5: Create pull request

Click the button "Create pull request"



## Review change proposal (aka pull request)

On GitHub, click the pull requests tab and click the pull request you want to use

See acomments (only still relevant comments) from people on the comments tab.

Review the changes, one commit at a time on the commits tab, or review the changes file by file and line by line on the Files Changes tab.


### How to leave inline comments

On Github, on the pull request screen, when reviewing the changes file by file and line by line on the "Files Changed" tab, hover over a line and click the plus(+) sign to add an inline comment about that part of the changes.


### How to leave a general comment on all the changes

On Github, on the pull request screen, on the conversation tab fill in the add comment form to add a general comment (e.g. "Looks good to me", "Rubbish. Don't talk to me ever again")


### How to make amendments to the change proposal (aka pull request)

The change proposal (aka pull request) is entirely amendable. Just make more commits against the label (aka branch) and publish them and the new changes will show up against the pull request.

Github is even clever enough to hide comments that are made obsolete by subsequently published changes.



### Approve or reject a change proposal (aka pull request)

When you're sure everyone has finished commenting and adjusting the amendments accordingly you can choose to accept the change or reject it.


## How to accept

The GitHub term for accepting a change proposal and incorporating the changes into the master version of the directory is "merging the branch to master".

On Github, on the pull request screen, on the conversation tab click the "Merge pull request" button


## How to reject

You can reject a change proposal by closing the pull request

On Github, on the pull request screen, on the conversation tab, click the
"Close pull request" button to reject the changes.

