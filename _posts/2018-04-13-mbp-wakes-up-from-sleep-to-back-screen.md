---
id: 1772
title: MBP wakes up from sleep to back screen
date: 2018-04-13T17:37:52+00:00
author: Luis Puerto
layout: post
guid: http://luisspuerto.net/?p=1772
permalink: /2018/04/mbp-wakes-up-from-sleep-to-back-screen/
wtr-disable-reading-progress:
  - ""
wtr-disable-time-commitment:
  - ""
image: /wp-content/uploads/2018/04/apple-wake-up.jpg
categories:
  - Personal
  - Technology
tags:
  - dGPU
  - high sierra
  - macOS
---
As you know, I have had problems with my old MacBook Pro Late 2011 and its [dGPU](http://luisspuerto.net/tag/dgpu/) which I&#8217;ve been able to _patch_ to make the computer work again. In the beginning, the side effect of the fix was not to be able to wake up properly the Mac from sleep mode. The computer woke up to a black or grey screen and the fans started to work at full speed to finally turn off itself. This was cause because on the wake up process the computer decided to stuck to the faulty dGPU instead to the iGPU. Luckily, this problem was solve as you can see in the [final fix](http://luisspuerto.net/2017/12/disconnecting-the-dgpu-in-a-late-2011-macbook-pro-third-way/).

However, my Mac still wakes up to a black screen from time to time. This isn&#8217;t a new behavior at all, just happen to come up more often. Perhaps, in the past, this problem happened once per month or two months or even once every six months.

Basically, the computer wakes up from sleep mode to a black screen that remains black no matter you do or what key you punch, while the computer seems to perfectly work in the dark. In this case, the fans don&#8217;t run at full speed and seems that the computer can stay like that for long. I haven&#8217;t tried, but I guess you can even log in remotely. If your Mac happen to have the iconic glowing apple in the lid you can put there a source of light –the flashlight of your smartphone for example– and you&#8217;ll probably be able to see the login screen –just the part around the Apple logo. Basically, what is going on in most of the cases, is the computer wakes up but it doesn&#8217;t turn on the blacklight of the screen for some reason.

This is a quite a [common problem](https://www.google.com/search?newwindow=1&client=safari&rls=en&ei=t63QWq7hDcb_swHCg6mIBg&q=macbook+black+screen+wake+up&oq=macbook+black+screen+wa&gs_l=psy-ab.3.1.0j0i22i30k1l6.20990.25239.0.27396.7.6.1.0.0.0.168.909.0j6.6.0....0...1c.1.64.psy-ab..0.7.949...35i39k1j0i67k1.0.t79Q76vUQP0) on MacBooks and if you search on internet about it you are going to find multiple solutions. Till now, none of them has really worked for me, but if you have this problem perhaps some of them are going to work for your, so why not to give it a try.

# Reset SMC and **PRAM/NVRAM**

This is the most common solution you are going to find our there since perhaps the problem is related to those basic configurations. Yet, in my case I can&#8217;t do that –or I rather not– because the solution for disable the dGPU of my MPB is partly a setting on the NVRAM, so if I reset it I need to reapply the whole thing again, or at least that.

If you want to give it a try to can reset those settings with this directions:

  * [**SMC**](https://support.apple.com/en-us/HT201295): shutdown, unplug everything except power, now hold <span class="lang:sh highlight:0 decode:true crayon-inline">leftShift + Ctrl + Opt/Alt + Power</span> for about 10&#8243; and release at the same time.
  * [**PRAM/NVRAM**](https://support.apple.com/en-us/HT204063): with the power cord on, power on and immediately later and before the chime hold <span class="lang:sh highlight:0 decode:true crayon-inline">cmd + Opt/Alt + P + R</span> at the same time until you hear the chime for the second time.

# Making it sleep again

Some people argue that the problem is related to the the lid itself that becomes a little bit faulty, either in the hinge or in the magnet, so it doesn&#8217;t send the proper signal to the computer to wake up when you open the lid. In in this camp I&#8217;ve seen like a couple of solutions.

## Try to log in and make it sleep again

Since you computer seems to work properly but the screen if not receiving backlight, so it remains black, you can log in and command your computer to sleep again to reattempt to wake up properly this time. You can check if this is your case, if your lid&#8217;s Apple logo is not glowing chances are that the problem is just the backlight. You can put a source of light there –the flashlight of your smartphone, as suggested before– and see in you can spot the login screen. That means your computer is up and running perfectly.

Then, you can type your password, log in and after that push the power button for just a couple of seconds –no more or you are going to turn off the computer and we are trying to avoid that. That we&#8217;re trying to accomplish here is to make to show up the power / shut down menu in macOS. If we&#8217;ve succeeded we can hit the S key next and your computer should sleep again.

<div id="attachment_1777" style="width: 578px" class="wp-caption aligncenter">
  <a href="http://luisspuerto.net/wp-content/uploads/2018/04/Screen-Shot-2018-04-13-at-13.16.22.png"><img class="size-full wp-image-1777" src="http://luisspuerto.net/wp-content/uploads/2018/04/Screen-Shot-2018-04-13-at-13.16.22.png" alt="" width="568" height="279" srcset="http://luisspuerto.net/wp-content/uploads/2018/04/Screen-Shot-2018-04-13-at-13.16.22.png 568w, http://luisspuerto.net/wp-content/uploads/2018/04/Screen-Shot-2018-04-13-at-13.16.22-300x147.png 300w, http://luisspuerto.net/wp-content/uploads/2018/04/Screen-Shot-2018-04-13-at-13.16.22-509x250.png 509w" sizes="(max-width: 568px) 100vw, 568px" /></a>
  
  <p class="wp-caption-text">
    macOS power / shut down menu
  </p>
</div>

If your computer doesn&#8217;t go to sleep, don&#8217;t worry, mine either. I haven&#8217;t been able to make this solution yet a single time.

## Push the power button and close the lid

When you see that your Mac doesn&#8217;t wake up in the correct way, one of the most obvious behaviors is close the lid again –like trying to make this a bad dream– and open again, to give another try. Also pushing buttons here and there, scape key –let me get out of this nightmare, I don&#8217;t want to lose my 150 pages document that I didn&#8217;t save before and I&#8217;ve been working the whole week when I sent the Mac to sleep– and the power button and go on and so for. That has worked for me in the past sometimes, not always. Sometimes the computer turned the screen on again and some others it just reboots.

Some people say that the correct way to do this just push the power button and close the lid, to open it again after a couple of seconds. But I haven&#8217;t try this yet. I don&#8217;t remember if the times I&#8217;ve succeeded to be back to life the computer I&#8217;ve followed that sequence by any chance. Who knows!!

# Changing energy parameters

Other solution I&#8217;ve read about is just change the way your Mac sleeps. You Mac can be sent to sleep in two ways, simple sleep or Safe Sleep –the last one is/was called hibernation in windows– so macOS has three different setups for sleeping –only simple sleep, only safe sleep or both. You can see your config using the command:

<pre class="lang:sh decode:true">$ sudo pmset -g custom</pre>

In my case are the following right now:

<pre class="lang:sh decode:true">Battery Power:
 lidwake              0
 standbydelay         4200
 standby              0
 ttyskeepawake        1
 hibernatemode        0
 gpuswitch            1
 hibernatefile        /var/vm/sleepimage
 displaysleep         2
 sleep                10
 acwake               0
 halfdim              1
 sms                  1
 lessbright           1
 disksleep            10
AC Power:
 lidwake              0
 standbydelay         4200
 standby              0
 ttyskeepawake        1
 hibernatemode        0
 gpuswitch            1
 hibernatefile        /var/vm/sleepimage
 womp                 0
 displaysleep         10
 networkoversleep     0
 sleep                0
 acwake               0
 halfdim              1
 sms                  1
 disksleep            10</pre>

The variable that holds this setting is `hibernatemode` and `` is simple sleep, `3` is both and `25` is just safe sleep. In essence what is going on here is:

  * Simple Sleep &#8211; \`hibernatemode 0\` : Your computer keeps all the info in the RAM and stops all the rest of the computer. The RAM still has power and if you happen to run our of battery –after quite long time– you lose everything –not really, but let&#8217;s be catastrophical and think in the worse picture. However, you usually you don&#8217;t let your Mac sleeping and unplugged for more than a week, do you? I think the battery in this state can last more than a week, let be conservative here. This mode is the quickest, and usually your Mac is sleeping just after a couple of seconds you close the lid.
  * Both &#8211; `hibenatemode 3` : This is the standard mode and how most of the MacBooks behave. When you close the lid the Mac just normally sleep, but before it&#8217;s going to save its state in the `sleepimage`. If it doesn&#8217;t run out of battery, it usually wakes up normally, from the info in the RAM and you continue working as usually. If it runs out of battery it&#8217;s going to switch to safe sleep before it loses power. In this case when you open the lid you have to push the power button and your Mac is going to recover from the `sleepimage`. This is the safest&#8230; since it&#8217;s redundant, but it&#8217;s is slower than just sleep. This in modern MacBooks with SSD is call Standby Mode, and instead of waiting till the total lost of power between 1 h or 3h –depending on the year model– it goes to safe sleep.
  * Safe Sleep &#8211; `hibernatemode 25` : This is the hibernation mode in windows, in other words, the computer saves everything to the `sleepimage` and them disconnect power from everything. This mode is also really safe, perhaps safer than the previous one for some people and cases, but it&#8217;s the slowest. Usually the sleep process is the same than in the previous one, but it&#8217;s always going to wake up from the sleepimage, regardless of it has run out of battery or not. So it&#8217;s going to take more or less time depending of the capacity of your machine to read the `sleepimage`.

There is more info about the sleep modes [here](https://support.apple.com/en-us/HT202824).

<div id="attachment_1782" style="width: 1570px" class="wp-caption alignleft">
  <a href="http://luisspuerto.net/wp-content/uploads/2018/04/macos-sierra-mbp-progress-bar-after-deep-sleep.png"><img class="size-full wp-image-1782" src="http://luisspuerto.net/wp-content/uploads/2018/04/macos-sierra-mbp-progress-bar-after-deep-sleep.png" alt="" width="1560" height="1004" srcset="http://luisspuerto.net/wp-content/uploads/2018/04/macos-sierra-mbp-progress-bar-after-deep-sleep.png 1560w, http://luisspuerto.net/wp-content/uploads/2018/04/macos-sierra-mbp-progress-bar-after-deep-sleep-300x193.png 300w, http://luisspuerto.net/wp-content/uploads/2018/04/macos-sierra-mbp-progress-bar-after-deep-sleep-768x494.png 768w, http://luisspuerto.net/wp-content/uploads/2018/04/macos-sierra-mbp-progress-bar-after-deep-sleep-1024x659.png 1024w, http://luisspuerto.net/wp-content/uploads/2018/04/macos-sierra-mbp-progress-bar-after-deep-sleep-1216x783.png 1216w, http://luisspuerto.net/wp-content/uploads/2018/04/macos-sierra-mbp-progress-bar-after-deep-sleep-388x250.png 388w" sizes="(max-width: 1560px) 100vw, 1560px" /></a>
  
  <p class="wp-caption-text">
    Waking up from safe sleep
  </p>
</div>

Some people argue that the back screen problem is related to the sleep image or the `hibernatemode 3` , so you have two options, change to `hibernatemode 0` –the one I have right now– or to `hibernatemode 25`. If the problem is in the `sleepimage` the obvious candidate is the zero mode, but I&#8217;ve tried it and I&#8217;ve just woken up to a back screen. On the other hand,  while I was trying to fix the dGPU problem I had set the 25 mode for long, but sometimes it also woke up to the back screen. So this isn&#8217;t working for me.

To change the sleep behavior you can run the following commands

<pre class="lang:sh decode:true"># Just sleep mode
$ sudo pmset -a hibernationmode 0
# Sleep mode + safe sleep 
$ sudo pmset -a hibernationmode 3
# Just safe sleep
$ sudo pmset -a hibernationmode 25</pre>

`-a` is for all –when you are on power ac and battery– but you can specify different settings. `-b` for battery and `-c` wall power.

If you decide to go for `hibernatemode 0` you can also delete de `sleepimage` and sabe some space in your hard drive.

<pre class="lang:sh decode:true ">$ sudo rm -f /var/vm/sleepimage</pre>

&nbsp;

# The lidwake (on test)

Since some people say that the problem is related to the lid I&#8217;ve decided to change the way the computer wakes up. Instead of waking it up when I open the lid I going to wake up it pushing a key after opening the lid.

You can achieve this changing the `lidwake` parameter to ``:

<pre class="lang:default decode:true ">$ sudo pmset -a lidwake 0</pre>

The normal value is `1`.

Let&#8217;s see how this pan out and I&#8217;m able to stop the back screen wake up.

# Final thoughts

The issue isn&#8217;t incredible problematic, even more right now that in modern system is really difficult to lose data because a force reboot. However, isn&#8217;t a normal behavior and is something that Apple should take a look to it. Seems that the problem extents across several generation of Macs and for some people has become more acute with High Sierra. Perhaps this is my case, but I don&#8217;t really know. I&#8217;ve [installed High Sierra](http://luisspuerto.net/wp-admin/post.php?post=735&action=edit) around beginning of November and in the beginning of December my dGPU crashed. So it&#8217;s difficult for me if this behavior has increased due to the crash, due to High Sierra or just because my Mac is old.