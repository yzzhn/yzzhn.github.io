---
layout: post
title: Wireshark permission issue
date: 2024-10-29
description: tips on how to resolve Wireshark permission issue on mac
tags: wireshark
categories: tips
featured: false
---
### Tips: How to resolve Wireshark permission issue on mac

When freshly installed wireshark on mac, one may encoutered permission issue such as:

 ```
 Can not create profile directory at $directory
 ```

 Here's something to try:

1. On your macbook, go to System Settings -> Privacy & Security -> Full Disk Access -> click "+" button and add Wireshark
   
2. Locate the $directory in the error message, check its owner and permission `ls -la $directory`. Identify current user `whoami`. Change the `$directory` owner to the correct user using `sudo chown -R $user:$group $directory`
