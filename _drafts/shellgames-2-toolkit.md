---
published: false
layout: post
name: Shell Games - Getting Started
title: Shell Games - Getting Started
tags: 
---

Recently, I've been using [Mint Linux](http://linuxmint.com) for my base
system. It's an Ubuntu based system which in turn is based on
Debian. All are similar with slightly different nuances. I prefer
Mint's look which is more like "traditional Windows" than Ubuntu's
current interface which is more Mac like.

In either case, I use the GUI to open up terminals, an editor, and a
browser so I mostly want the GUI to keep out of my way.

You could install instal Linux on a spare machie or set up a dual boot, but if you just want to play with a shell, there's an easier way.

I'm a big fan of [Digital Ocean](http://digitalocean.com). They're a
cloud hosting service. Really affordable, really reliable, and run by
great guys (full disclosure: they're part of the StuyCS
family).

 Basically, you can set up a Linux server in the cloud in just
a couple of minutes for $5 a month (and there's usually a coupon
floating around on line for a free month).

On top of that, the Digital Ocean team is putting together a great series of [tutorials](https://digitalocean.com/community) on all manner of Linux Dev/Ops stuff.

So, if you want an easy way to play with some of this stuff, head on over there and make an account.

Now that you have an account, you can follow this
[tutorial](https://digitalocean.com/community/articles/how-to-create-your-first-digitalocean-droplet-virtual-server)
on creating a droplet or virtual server. If you are familiar with ssh
you should [set up your
keys](https://digitalocean.com/community/articles/how-to-use-ssh-keys-with-digitalocean-droplets)
first but if not, don't worry about it.

Just a couple more steps for today.

If you follow the above tutorial, you should be able to use **ssh** (or **putty** on Windows) to log onto your server as root. You'll want a non-root account. Let's say I'm creating account for myself, the dialog will look something like this:

<pre>
root@server1:~# adduser <b>zamansky</b>

  adding user `zamansky' ...
  adding new group `zamansky' (1002) ...
  Adding new user `zamansky' (1002) with group `zamansky' ...
  Creating home directory `/home/zamansky' ...
  Copying files from `/etc/skel' ...
  Enter new UNIX password: <b>ENTER YOUR PASSWORD - NOTHING WILL SHOW</b>
  Retype new UNIX password: <b>ENTER YOUR PASSWORD - NOTHING WILL SHOW</b>
  passwd: password updated successfully
  Changing the user information for zamansky
  Enter the new value, or press ENTER for the default
	Full Name []: <b>Mike Zamansky</b>
	Room Number []:
	Work Phone []: 
	Home Phone []: 
	Other []: 
	Is the information correct? [Y/n] <b>y</b>
root@server1:~# 
</pre>

The stuff you type is in bold.

<pre>
root@server1:~# <b>addgroup zamansky sudo</b>
  Adding user `zamansky' to group `sudo' ...
  Adding user zamansky to group sudo
  Done.
root@server1:~# 
</pre>
