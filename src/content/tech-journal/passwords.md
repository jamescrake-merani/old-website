---
title: "How I Manage my Passswords Across my Devices"
date: 2021-09-04T16:10:21+01:00
draft: false
---

Previously, I used Lastpass for this purpose, but as I grew more accustomed to using free software, Lastpass became more, and more of a strange choice. Then, the people at Lastpass decided to restrict usage to one device without their premium service. I put off moving from Lastpass until a few months ago where I switched to storing the passwords encrypted with GPG. At time of writing, there are 3 devices that I need my passwords on: my main PC, my Surface Pro laptop (both of which are running Arch Linux), and my Android phone.

# Disclaimer

I am not providing you a tutorial for the software I will mention. While I will offer some pointers, you should consult the documentation of each software to get an understanding of how to use it. I should also point out that I am merely sharing how I store passwords in this article. This may not be the best way to store passwords, and if you copy my method then I cannot take responsibility for anything that goes wrong.

# Passwords on Arch

On Arch, I use pass to manage my passwords. It actually doesn't do too much on its own: running `pass init` will create a directory named `.password-store` on your home directory. Then, each password will be stored in a file encrypted with GPG.

In order to retrive a password, I use pass-menu which uses dmenu. Selecting a password will decrypt it, and copy it to your clipboard. On DWM, I have pass-menu bound to `Shift + Super + p`, and I have also applied a patch to Dmenu to make it case-insensitive so I don't have to worry about that. You can find my Dwm, and Dmenu forks on my [Github page](https://github.com/jamescrake-merani). I also use Dmenu for pinentry (the program which prompts for my key password).

# Passwords on Android

There are two apps that I use: [Password Store](https://f-droid.org/en/packages/dev.msfjarvis.aps/), and [OpenKeychain](https://f-droid.org/en/packages/org.sufficientlysecure.keychain/). Both of these apps are available on Fdroid. 

# Syncing with Syncthing

I use Syncthing not just for passwords, but for all the files I want to keep synchronised across my 3 devices. I do NOT use this for syncing my private keys - I have transfered them over manually, and I encourage you to do the same. This is because the keys will of course never change, and also it simply feels wrong to transfer them over the network in this way.

# Conclusions

I kept putting off moving to a system like this but after doing so I think it is much better than Lastpass. Restricting the Lastpass free version was probably a good business decision - I don't think many people needed the premium features until then. But even without that, I think this approach is better because you are not uploading your passwords to a server you don't own, but you are simply transferring passwords between devices you **do** own. I wasn't too concerned about the security of my passwords on Lastpass since I knew they were encrypted but actually being able to **see** my encrypted passwords does give me a bit more peace of mind. At least now if my passwords get leaked it is less likely to be the fault of some company, but the consequence of my own incompetency. 
