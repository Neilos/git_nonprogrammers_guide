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

Git is most commonly used to track software projects, but it can be used to track changes to almost any electronically stored document or collection of documents. For example, the drafting and redrafting of many books have been managed using git.
