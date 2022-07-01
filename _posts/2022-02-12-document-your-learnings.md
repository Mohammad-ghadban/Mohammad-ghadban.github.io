---
layout: post
title: Effective journaling on your blog
subtitle: How to document your learning in markdown
categories: Markdown
tags: [Markdown, journaling, blog]
---
Push to Github
Once you have made the changes you want to commit to your website, open a terminal. If you are in VSCode, you can do that by clicking on Terminal > New Terminal at the top of your screen. Now a terminal will open at the bottom of your screen (it might have been opened already).

Being in your projects root repository, you can now compare the state of the repository on your computer with the state of the repo that is available online, by typing:

git status
If no change shows up, you might have forgotten to save your file/changes.

To add all the modified or new files to the staging area, type:

git add .
The .signals that you want to stage all changes. You can also select individual changes by passing concrete file names instead.

Now, commit your changes providing a brief description.

git commit -m "this is a note to myself and others dealing with the repository; it describes my changes"
Now it is time to push the changes to your remote repository.

git push origin main
Done! Congratulations!