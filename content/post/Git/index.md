---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Git"
subtitle: "Version control Git."
summary: "Version control Git."
authors: [Arina O. Aristova]
tags: []
categories: []
date: 2022-05-07T15:37:13+03:00
lastmod: 2022-05-07T15:37:13+03:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

# Let's talk about version control Git.

***Version Control Systems (VCS)*** are used when several people work on one project. Usually, the main project tree is stored in a local or remote repository, to which access is configured for project participants. When making changes to the project content, the version control system allows you to fix them, combine changes made by different project participants, roll back to any earlier version of the project, if required.

In classical version control systems, a centralized model is used, assuming a single repository for storing files. Most version control functions are performed by a special server. The project participant (user) receives the version of files he needs before starting work through certain commands. After making changes, the user places the new version in the repository. At the same time, previous versions are not deleted from the central repository and you can return to them at any time.

Version control systems support the ability to track and resolve conflicts that may arise when several people work on a single file. You can merge (merge) changes made by different participants (automatically or manually), manually select the desired version, cancel the changes altogether or lock files for modification. Depending on the settings, the lock does not allow other users to get a working copy or prevents changing the working copy of the file by means of the OS file system, thus providing privileged access to only one user working with the file.

The Git version control system is a set of command-line programs. They can be accessed from the terminal by entering the git command with various options. Due to the fact that Git is a distributed version control system, a backup copy of the local storage can be made by simple copying or archiving.

