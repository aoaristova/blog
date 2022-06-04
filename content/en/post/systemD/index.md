---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "SystemD"
subtitle: "What is an initialization system? And for what?"
summary: "A bit about SystemD"
authors: [Arina O. Aristova]
tags: []
categories: []
date: 2022-05-14T05:17:42+03:00
lastmod: 2022-05-14T05:17:42+03:00
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

In UNIX-like operating systems, and in Linux in particular, after the kernel is loaded, the initialization of the Linux system, services, and components begins. The initialization process is responsible for this, it is started by the kernel after the end of the boot and has a PID of 1, it is also executed while the system is running. But about everything in order! 

# What is an initialization system? 

Even when we just start the operating system, literally open, for example, a terminal, a large number of processes are already running. Although we did not launch them manually, they were launched automatically by other programs. 

Each of our actions in the operating system, in fact, is some kind of program. For example, just logging in, launching the browser, and so on. To make all this happen, certain processes are started. Such programs are called daemons.

That is, it turns out that in order for the same login to be performed or to the browser, certain daemons must work. In turn, in order for them to work, they must be somehow launched by someone or something. This is what the INITIALIZATION SYSTEM is designed for!

There are various Linux initialization systems: SYSTEM V INIT, OPENRC, RUNINIT, UPSTART. But I'm going to talk about SystemD today. This initialization system was first introduced by default in Fedora 15, and is now already used in many popular Linux distributions, for example, CentOS. For example, I looked at which initialization system is on my virtual machine (Linux, Fedora distribution), and it's SystemD.

The initialization system is the first process launched in the user space. Its PID (Process ID) is 1.

# How did SystemD appear?

SystemD was developed by Red Hat software engineers Lennart Poetering and Kay Sievers. Initially, it was a project to replace the standard well-known Linux System V init in 2010.

An experimental version of SystemD was already presented in April 2010 in the Poettering blog called "Rethinking PID 1". 

In May 2011, Fedora included SystemD by default for the first time, replacing the standard SysVinit at that time. 

Further, the developers argued a lot about the functionality and advantages of SystemD and SysVinit. Some even believed that the dislike and carping about SystemD were based not so much on real shortcomings as personal dislike of developers and undesirable attitudes towards change processes.

Let's go back to the SystemD initialization system, its work. After starting, the initialization system should start the daemons. But this is not just a list of programs that should be run. Some of them need to be launched before others, some programs may conflict with each other, and so on. Therefore, it is necessary to determine which programs and when to run, to enable the user to decide which programs to run and which not to run. These are the tasks that SystemD faces. 

In general, it should be understood that the role of the initialization system, in short, is to launch the OS. That is, the purpose of the initialization system is to make sure that all the daemons necessary for the correct operation of certain processes are started. However, SystemD is not just an initialization system. SystemD positions itself as a system and service manager, it binds and replaces many OS components, that is, it is responsible for much more.

# Conclusion:

SystemD is a service initialization and management system in Linux, which in the 2010s practically replaced the Init initialization system, which was traditional, which was not accepted unambiguously, but is still used in many distributions today. The main goal is to have full control over all processes during their startup and before their completion. 

Thus, SystemD is a relatively young Linux initialization system, for the first time the SystemD initialization system appeared by default in Fedora 15, and then began to be used in many popular Linux OS distributions. SystemD is not only an initialization process that supports a large number of features, but also a set of tools that allow you to manage the services and capabilities of the system.

