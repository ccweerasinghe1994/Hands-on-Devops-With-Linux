- [1. Getting Started With Linux 🐧](#1-getting-started-with-linux-)
  - [1.1 Structure 🦊](#11-structure-)
  - [1.2 Objectives 🐢](#12-objectives-)
  - [1.3 What is Linux? 🐉](#13-what-is-linux-)
    - [1.3.1 Distributions 🐼](#131-distributions-)
    - [1.3.2 Servers 🐳](#132-servers-)
    - [1.3.3 Conclusion 🪲](#133-conclusion-)
  - [1.4 Setting up your environment 🐞](#14-setting-up-your-environment-)
    - [1.4.1 Installing the VirtualBox 🕷️](#141-installing-the-virtualbox-️)
    - [1.4.1 Installing the Linux System ⚡](#141-installing-the-linux-system-)
    - [1.4.1 Installing Your Linux System 🔥](#141-installing-your-linux-system-)
    - [1.4.1 Accessing via SSH 🦁](#141-accessing-via-ssh-)
  - [1.5 Conclusion 🦄](#15-conclusion-)

## 1. Getting Started With Linux 🐧

This chapter will introduce you to the `Linux` world with a focus on `servers`. Therefore, I will not explain about it on `desktops`. You will see explanations about Linux, why you `should` know `it`, its basic concepts, and a lot of `commands`. I am a technical guy, so brace yourself because you are about to see how to set up your `lab` hands-on!

### 1.1 Structure 🦊

- In this chapter, we will discuss the following topics:
- What is Linux
  - Distributions
  - Servers
- Setting up your environment
  - Installing the VirtualBox
  - Installing a Linux system
- Accessing via SSH
- Introduction to Bash
  - Useful commands
  - Basic files and how to edit them
  - Customizing your shell
  - Installing packages

### 1.2 Objectives 🐢

After studying this unit, you should be able to:

- Understand the basics of Linux
- Choose your favorite distribution
- Install your virtual machine
- Access any remote Linux server

### 1.3 What is Linux? 🐉

In my view, if you bought this book, you probably have a basic idea of what is
`Linux` and you already know why you want to learn it. Thus summarizing, Linux
is an operating system with an `open-source code`, and works similar to the
famous `Windows`, but it does not belong to any company. So, how is the code
open? Everyone can download the `core Linux` using this site:
https://www.kernel.org/, and if you are interested to give a look around the
`source code`, it can be found on this link https://git.kernel.org/.

Linux has this name because of its creator, `Linus Torvalds`. The first 3 letters are
the initials of Linus, and the last 2 come from another OS, called Minix, created
by a man, named Andrew Tanenbaum.

It is common for you to see Linux bound to other initials, like `GNU`. This
happens because when Linus Torvalds was creating Linux, he used many tools
that were created by the `GNU project`, https://www.gnu.org/home.en.html. The
GNU project began with Richard Stallman, the creator of the `Free Software Foundation`, https://www.fsf.org. What does it mean to license an `open-source`?
It means that every software written by the GNU project has its code open for
everyone who wants to work on it. Then, how Linus Torvalds used the tools
from the GNU project? He decided to use the same philosophy of the open source and he released the Linux system with the tools from the GNU project.
This explains the term `GNU/Linux`.

#### 1.3.1 Distributions 🐼

Since Linux is open-source, a lot of people and companies created their own
versions of Linux, which are called `distributions`. Everyone who has the
knowledge in computer programming can make their own Linux distribution.
One example is  Kurumin Linux , created by a Brazilian programmer, Carlos
`Morimoto`, and can be found on the link, https://distrowatch.com/table.php?distribution=kurumin. Unfortunately, it is discontinued, because maintaining
your `own distribution` is not an `easy task`. You have to be concerned about
`updates`, `new releases`, `new software`, `bug correction`, and `infinite` things that are
basically `impossible` for just one person to take all that effort and without being paid for it. So, it is one important topic for you to decide what distribution you
are planning to install in your `infrastructure`. Imagine the situation where you
began with one `distribution`. A year later, it is `discontinued` and you have to
`reinstall` your whole infrastructure with more than 300 servers. We, as
professionals, cannot let this happen.
Regarding the `distribution` we want to choose for our infrastructure, there exists
several of them, but some are the mostly used, because of the reasons I am going
to explain further:

- **RedHat Enterprise Linux** 🎩: This is the `most famous` and `corporative`
distribution because of the `RedHat Company`. It is one of the most `famous`
companies in the `Linux world`. It has amazing support, frequent updates,
and 100% compatibility with the `RedHat software`, like `JBoss`, `OpenStack`,
`RedHat Enterprise Virtualization Manager`, and a lot of more options. But,
for using `RHEL`, it is required to take a `subscription` with the company and
pay for it. Otherwise, you will `neither receive any updates`, nor will you be
able to `access to the repository`.

- **Community Enterprise Operating System**🧨: `CentOS` is the community
version of `RHEL`. It is the most common distribution among the companies
that have chosen to not use the paid version and want to use the `community`
version of the `RedHat software`.
- **SUSE**🎈: It is the Novell (`Microsoft`) distribution and is a good option,
because, Microsoft is one of the biggest companies around the world.
Therefore, the probability of it being `discontinued` is `zero`, and you will
always have the `updates` and `new software` published by the company. It
also has a community version called the `OpenSUSE` which follows the
same features of the `CentOS`.
- **Debian**🕹️: This is the option for those who are more involved in the
community and do not want to be bound to any company, like the `distros`
mentioned previously. Debian is `100%` maintained by the `community` and
is one of the `oldest` distros we have. Also running over a lot of servers, it is
very `stable` and `reliable`, and is frequently used by the companies and
common users.
- **Ubuntu**🧸: This distro was made in `Africa` by Canonical that used to
distribute CDs over the whole world for people to get to know more about
Linux and run it on their desktops. The final users were the target by
Canonical in the beginning. So, I believe that for desktops, Ubuntu is the
`most` `used` `distro`, and for `servers`, it is `CentOS`. Ubuntu has a version for server which is my favorite distribution. That's why I am writing this book
using Ubuntu. But the knowledge you will acquire here can be used for all
the distributions.


#### 1.3.2 Servers 🐳

#### 1.3.3 Conclusion 🪲

### 1.4 Setting up your environment 🐞

#### 1.4.1 Installing the VirtualBox 🕷️

#### 1.4.1 Installing the Linux System ⚡

#### 1.4.1 Installing Your Linux System 🔥

#### 1.4.1 Accessing via SSH 🦁

### 1.5 Conclusion 🦄
