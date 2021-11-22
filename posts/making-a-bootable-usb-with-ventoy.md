---
title: 'Making a bootable USB with Ventoy'
date: '2021-11-22'
---

## Making a bootable USB with Ventoy

Welcome to this blog post about making a bootable USB with Ventoy! In this post, Today I am going to cover how you can make a bootable USB with Ventoy, which you can use to boot multiple operating systems, all from one USB, instead of having alot of seperate ones. I will also show how to change the Ventoy theme.

## What is Ventoy?

So let's start by figuring out what Ventoy is, and what it does. Let's start with what Wikipedia has to say:

*Ventoy is a free and open-source utility used for writing image files such as .iso, .wim, .img, .vhd(x), and .efi files onto storage media to create bootable USB flash drives. Once Ventoy is installed onto a USB drive, there is no need to reformat the disk to update it with new installation files; it is enough to copy the .iso, .wim, .img, .img(x), or .efi file(s) to the USB drive and boot from them directly.Ventoy will present the user with a boot menu to select one of these files.*

So uh...yeah. But now let me break this down a little bit for you. Basically, Ventoy lets you make a bootable USB, which you can store mutliple operating systems on. When you start your computer and boot into the ventoy USB, it will ask you to select a file to boot from. You can select multiple files, and Ventoy will boot them all from the same USB.

## Setting it up

Now that we know what it does, lets look at using it. 

### Some Prerequisites

- A USB drive that's at least 2 GB in size
- A computer
- One or more ISO files you want to use

First of all, you need to install the ventoy program. You can download it from the [Ventoy website](https://ventoy.org/). Install the zip file, open it, and run the Ventoy2Disk.exe file. Now, we need to enable [Secure Boot](https://en.wikipedia.org/wiki/Secure_Boot) on Ventoy, by clicking on the Option button at the top, and then clicking on the "Secure Boot Support" button. Now, in the "Device" dropdown, make sure you have the USB drive you want to install Ventoy on selected. Now, click on the "Install" button, and wait for the installation to finish. 

Now, you can grab your .iso files, and drag them all into the Ventoy USB. 

## Enabling Secure Boot

We're almost done! Just a few more steps and then we'll have a fully working, bootable USB. 

Now to enable Secure Boot, you need to first boot the Ventoy USB. To do this, restart your computer, and then open your computer's boot menu, and boot from the USB. Now, how you access the Boot Menu varies depending on your computer. On my laptop, it's F12, but you can just Google "How to open Boot Menu in <your computer model>" and you'll find out how to do it. Now, first time you boot Ventoy, you should be seeing a blue screen, which says "Press any key to perform MOK Management". Just press Enter a few times, and you'll be brought to a few options. Select "Enroll key from disk" and press Enter (you can navigate the menu with the arrow keys). Now, select the option that says either EFI or VTOYEFI. Then choose ENROLL_THIS_KEY_IN_MOKMANAGER.cer. Hit Continue, hit Yes, Reboot. Aaand now, you have officially installed Ventoy! On your screen, you should be seeing all the .iso files you put in the USB. Now to run any of the iso files, its as simple as navigating to the file, and pressing Enter, and it will boot like normal!

## Adding a theme

Now, technically, we are done with Ventoy. But, we still need to change the theme, because currently the Ventoy screen doesn't look the best. To do this, we first need to download the theme. You can get the theme from [here](https://www.gnome-look.org/p/1443844/). I am going to be using a MacOS-based theme because I think it looks clean, but you can look through the website and find a theme you like. You can search for themes in the "GRUB Themes" section. But anyways, back to setting up the MacOS theme. Install the bigsur-ventoy-theme.zip file, extract it, and copy the "ventoy" folder into the root of your Ventoy USB. Next time you boot it, it will automatically load the theme. Looks much better now, doesn't it?

Now, if you want some other options, you can explore gnome-looks.org yourself to find one you like, but here are a few I found and like:

- [MacOS Theme](https://www.gnome-look.org/p/1443844/)
- [Distro Grub Themes](https://www.gnome-look.org/p/1482847)
- [Ventoy Dark Theme](https://www.gnome-look.org/p/1519894)

## Conclusion

In this post, we covered how to make a bootable USB with Ventoy, and how to change the Ventoy theme. I hope you enjoy this post, and you all learnt something new!