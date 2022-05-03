- [1. Getting Started With Linux 🐧](#1-getting-started-with-linux-)
  - [1.1 Structure 🦊](#11-structure-)
  - [1.2 Objectives 🐢](#12-objectives-)
  - [1.3 What is Linux? 🐉](#13-what-is-linux-)
    - [1.3.1 Distributions 🐼](#131-distributions-)
    - [1.3.2 Servers 🐳](#132-servers-)
    - [1.3.3 Conclusion 🪲](#133-conclusion-)
  - [1.4 Setting up your environment 🐞](#14-setting-up-your-environment-)
    - [1.4.1 Installing the VirtualBox 🕷️](#141-installing-the-virtualbox-️)
    - [1.4 Installing the Linux System ⚡](#14-installing-the-linux-system-)
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
`Servers` are nothing more than `computers`. They are usually more `powerful` than
`PCs`, which are created and installed to attend to a purpose. For example, we can
install a Linux server for acting, like `web server`. In other words, to run a `website`
on it, like `Facebook`, `Amazon`, or `Google`. It can also act like a `database` `server`
where we can install a `PostgreSQL`, `SQL` Server, `MySQL`, `Oracle`, or another
that can be `file server` where the company stores all the `data` inside it, and in
many cases, all of it together. One example of it is what we call the `LAMP`,
`Linux` `Apache` `MySQL` `PHP`. Usually, we call a server `LAMP` when we have a
`Linux system` (a webserver, in that case), `Apache`, a `database` server (`MySQL`),
and a `programming` `language` interpreter, in this case, `PHP`. We can also call this
a `stack`. Stack means a set of tools that you can use to solve a problem. One of
my favorite stacks is `NPM`, `Nginx`, `Python`, and `MongoDB`. I have been using it
to solve many issues in the company that I work. This stack can be installed in a
server, which can be `virtual` or `physical`, and we will do that in the next chapters.


`On-premise` is a term often used for server installed within the infrastructure of
our companies, many-a-times, in a `datacenter`, and sometimes, under the system
admin desk. The `VMs` can also run in an `on-premise` infrastructure when we use
tools like `OpenStack` or `oVirt` to create them `on` the `top` of `physical` `servers`. It is a
`strategy` adopted by the companies towards having more `resilience`, `flexibility`,
and `better` use of our `resources`. One example is if you have to `switch` one or
more `servers` in your `datacenter`, for the fact that it is very `old` and is not able to
have the same `performance` as the `other` `servers`, you can `migrate` the `VMs` from
`one` `server` to `another`. `Switch` the `physical` machine and after `installing` a `new`
`one`, `migrate` all the `VMs` `back`.


`Cloud` is the name used to describe when the virtual servers are installed inside
the infrastructure of something else. In most cases, the companies like `AWS`,
`Azure`, and `GCP` have their own `on-premise` `infrastructure` and `rent` it for us. So,
we do not need to take care of the `maintenance`, like `switching` `disks` when they
`fail`, switching the server when they are `deprecated`, or even the `electricity` and
the `internet`. Furthermore, you can save costs by turning them `off` after the
`business` day and starting them again the `next` day. All these providers only
`charge` you for the time `that` the machine is `turned` `on`. Otherwise, you are going to `pay` only for the `storage`.
#### 1.3.3 Conclusion 🪲
Now that we already have a brief explanation regarding the `servers`, `virtual`
`machines`, `Linux`, and `distributions`, we are ready to start the hands-on. Let's
begin by setting up our first `Linux` `environment` and get to know the basics, and
so much more.
### 1.4 Setting up your environment 🐞
install preferred `distribution`.in virtual box or vmware
#### 1.4.1 Installing the VirtualBox 🕷️
follow the instructions on the [`VirtualBox` website](https://www.virtualbox.org/wiki/Downloads)
#### 1.4 Installing the Linux System ⚡

#### 1.4.1 Installing Your Linux System 🔥
install ubuntu server
after the installation
logged in into your machine, run the following command:
```shell
🔥➜  ~ ip a
```
The preceding command will show all the `network` `interfaces` you have and their
`IP address`, like the following:

**output**

```shell
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
2: ens33: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 00:0c:29:f4:99:82 brd ff:ff:ff:ff:ff:ff
    altname enp2s1
    inet 192.168.163.131/24 metric 100 brd 192.168.163.255 scope global dynamic ens33
       valid_lft 1761sec preferred_lft 1761sec
    inet6 fe80::20c:29ff:fef4:9982/64 scope link 
       valid_lft forever preferred_lft forever
```
#### 1.4.1 Accessing via SSH 🦁


### 1.5 Conclusion 🦄
