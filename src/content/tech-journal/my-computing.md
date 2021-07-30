---
title: "How I do my Computing"
date: 2021-07-30T10:05:25+01:00
draft: false
---

This is a list of software that I use on my main computer. I won't mention my phone, or other devices that I use today as I think that is a subject worhty of its own article, and I still unfortunately use a lot of non-free software on my other devices which I am going to start to rectify.

I try to use as much free (as in freedom) software as I can. However, I do not absolutely refuse to touch non-free software. This is a compromise I have to make to live a normal life, since I need to use non-free software for school, and connecting with friends.

I am constantly switching out the software I use so this list will probably need rewriting in a month, or so. You'll notice that I often switch software not because I am dissatisfied with the software I used before, but because I like trying out other solutions which might be better.

# Operation System

## Arch Linux

I use Arch just so I can install my own desktop environment, and other stuff that other distros have setup for you. Of course, there are other distros that I could use but Arch does the job perfectly fine. I have thought about switching to Gentoo but I decided that I probably wouldn't get much benefit from it, and having to compile all my software would just get annoying. I might be trying out Artix Linux soon to see what it's like to use a non-systemd system, although I don't really have much problem with systemd.

I hate Windows with a passion, and I hate everytime I have to go near that dreadful piece of software. Fortunately, there isn't really any software that I need Windows for anymore, and I no longer have a Window partition. The only problem is that getting video games to work on Linux is a pain in the arse because many don't run natively. I've also heard that developers really don't like supporting Linux because of the amount of issues people report. However, I don't really play video games as much as I used to, and there's still a decent set of games that'll run on Linux. There's a good amount of libre games for a lot of the board games you might play, but beyond that it's a bit lacking.

# Editor

## Emacs

A month or two ago, I switched from Vim to Emacs. I did this more to try out Emacs, and see what it's like. No one had been able to convince me that Emacs is better, I just decided that I wanted to see for myself. My verdict so far is that it doesn't really seem much better than Vim for editing. I've done a little bit of scripting in Elisp, and it seems to be a better language than Vimscript, but I'll need to use it more to say that for certain. Of course, Emacs isn't just an editor, and I'll mention a few other programs within Emacs that I use later. One of the problems though is that startup time is quite bad at least on my configuration as Emacs will take a few seconds to startup compared to Vim which starts up almost instantly. I might be able to optimise my configuration to reduce startup times, but I don't think you can eliminate them. Another problem I have is that Emacs has some bizzare defaults but I can of course change that in my configuration.

When code editing, I use flycheck, and company to get a decent editing environment. I don't currently use lsp-mode although I intend to look into doing so.

I do also use Emacs for writing, including the article you're currently reading. I normally use either Org mode, or Markdown depending on what seems best for the situation. All the articles that are on my website use Markdown. Org mode does have it's other uses - I have my todo list in Org mode, and I sometimes use it for note taking.

I should note that I don't use a certain distribution of Emacs like Doom Emacs, or Spacemacs. If you're a beginner you might prefer that because as previously mentioned, you might not like the defaults Emacs comes with. However, I've just built up a config from scratch, stealing bits, and pieces from other configs. I am using the Evil bindings which bring vim keybindings into Emacs. 

# Browser 

## Librewolf

I think that the browser is probably the worst piece of software you'll run, so when picking a browser there are no good options - just plenty of terrible options. I've gone with Librewolf because it is Firefox but it strips some of the Mozilla features e.g. pocket, and has some privacy protections. It comes pre-installed with an adblocker (uBlock Origin). The most noticable feature is that LibreWolf will by default clear all your cookies when you exit the program. You can of course add exemptions for websites if you so wish. The downside of this is that you'll be logged out of all your accounts when you quit the browser, but I don't really mind because with stuff like YouTube, I don't need to be logged in as I have RSS feeds for all the channels I want to keep up to date with (see the section on RSS).

Librewolf is based on Firefox, but I don't really have a preference between Firefox, and Chromium based browsers. They both seem to be just as good as each other from my experience. If I were using Chromium though I would probably use Ungoogled Chromium to strip out the Google services.

I should also mention that I used to use the Brave browser before, and I still think its a decent choice. However, I stopped using it because: I've heard a few dodgy things about it (although a lot of it could just be misinformation), the adblocking doesn't seem to be very good since it misses some adverts, and I never used their cryptocurrency features. They have this thing called BAT which is their own cryptocurrency you can earn by turning on adverts provided by Brave. You are then encouraged to donate to creators on the internet although I don't think there's anything stopping you from just cashing them in for yourself. I despise adverts so I never turned this feature on. The browser also provides wallets for cryptocurrency but I think it's better to have a separate program for this rather than having it integrated into the browser.

## Emacs Web Wowser (eww)

I ocassionally use the browser built into Emacs if I'm accessing sites that render well in it, which is mostly text based sites with simple layouts like mine. It can also be good for news websites, although I've started just using Librewolf for these now.

# Video + Audio

## MPV

MPV is a great video player. You can control it entirely through the keyboard if you want to, and it's really fast, and responsive. You can put YouTube links, and it's much better than the YouTube web player, although I tend not to do this because it's more convenient to click on a video rather than copy pasting the link into a terminal if I'm on the YouTube website.

I do also use this as a music player. If you pass in a directory, it'll just create a playlist with all the files in it. I could use a player designed for music like mpd but I don't really have much of a problem with this approach.

## Youtube-dl

As the title of this software suggests, you can download videos off of youtube without having to go through some dodgy ad ridden site online. I'll often download longer videos to my hard drive to watch later. I also use this to download music off of YouTube as you can pass the `--extract-audio` option to just get an audio file rather than the whole video.

This software also works on other websites although you can't use it on anything with DRM on it e.g. Netflix. I tend to use it on the BBC websites - I download programmes on BBC iPlayer, and also podcasts from BBC sounds.

# PDFs, Ebooks, and other similar formats

## Zathura

I love zathura. It makes it incredibly easy to navigate PDFs, and is 10x better than the PDF viewers they build into browsers. I also sometimes use it for Ebooks but not so much these days as I tend to just read physical books.

# Pictures

## Feh

The only problem with Feh is that it doesn't work with gifs - it'll just show the first frame. This doesn't really bother me since I don't tend to have gifs on my PC but if it does bother you I'm sure there's others out there.

# Display manager

## Dwm

Dwm is a tiling manager that follows the [suckless philosophy](https://suckless.org/philosophy/). I actually reckon its easier to configure than i3, which I used before. I haven't configured it a lot though. I've got a patch for vanity gaps, and I've added a few shortcuts for Emacs, and Librewolf as I use these programs frequently. I also use the swallow patch, which is great. It allows me to launch a program from the terminal which will then use that terminal window until the program closes. This avoids the problem of having a terminal window which you can't do anything with. It's hard to get this functionality from i3. When I used i3, I had a devour script which would hide the terminal until the program I launched closed, but this would often mess up the posistioning of the other progams I had open. The Dwm swallow patch is just much better.

Tiling managers are simply just better for producitivity in my experience. I don't have to worry about posistioning windows as the tiling manager will do that for me. I also like having multiple desktops that I can quickly switch to. For example, I might have Emacs, a browser, and a terminal with MPV playing my music all in separate desktops which I can quickly switch between. I tried to do this in Gnome but it just wasn't as quick to switch between them as it is in Dwm, or i3.

## Terminal

## Simple Terminal (ST)

ST also follows the [suckless philosophy](https://suckless.org/philosophy/). I've patched it to implement scrolling, but other than that I have it pretty close to vanilla. I used Alacritty before, but I switched to ST as does everything I need.

## Zsh

I have zsh set as my $SHELL. It has good completion, and colouring on it. I'm not sure if you can get that functionality from bash, I might have to look into that one day.

# RSS

## Elfeed

Elfeed is an Emacs package. I use it for reading blog posts, and watching videos from the feeds I'm subscribed to. I don't currently use it for news reading - I'll just go to news websites for that.

There's probably some small programs I'm forgetting about, but I've covered all the programs I use often. I do a lot my file management in the terminal so I don't really have the need for a file manager. I have a setup that works for me, and the beauty of GNU/Linux is it's modularity. I could easily replace any of these programs if I became dissastisfied with any of them, and I'm not locked into any configuration. If you have any questions, please feel free to email them to me.
