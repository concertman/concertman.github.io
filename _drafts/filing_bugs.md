---
layout: post
title: filing good bugs
---

Every developer has to deal with them. Whether they are incoming from your users or you are on the filing end for a bug in an OSS project or filing something against the tools you are using, bug reports are a part of developer life.

I was at Apple when this meme went viral. While it is firmly tongue in cheek it does high 

![Radar or GTFO]({{ site.url }}/assets/2012_02_29_photo.png "Photo by George Dick https://twitter.com/georgedick, 'Radar or GTFO' addition by Steve Streza https://twitter.com/stevestreza/status/177190924386975744")

\<rant\> I'm not going to talk about the quality of Apple's bug reporting tools. Saying that the quality of radar is why you don't file bugs is just an excuse for not helping the community. And a poor one at that. \</rant\>

One of the many things I learned in my tenure at Apple was the importance of good and frequent bug reporting. Here are a few things that help improve the quality of your bugs.

###Clear steps to reproduce

Which is better:

> Dont know what little black bin? Icon means?

or

> Steps to Reproduce: <br />
> 1) add item to basket <br />
> 2) to to checkout <br />
> 3) enter valid registration and shipping/billing address <br />
> 4) go to order summary <br />
> 5) check gift message box <br />
> 6) enter text into message field <br />
> 7) dismiss keyboard and go to another part of the view <br />
> 8) come back to the gift message box and tap in it again. see that all text you had previously entered is cleared <br />

Obviously these are a bit contrived (though they are actual bug reports I've received on a recent project). It's obvious which is preferable, but it does illustrate the issue. Be explicit as to how you were able to replicate the issue. Even if you have screenshots or videos of the actual issue happening provide the steps you used to replicate the issue. Often when trying to replicate the bug so that you can get the steps, you'll find other information that could be potentially valuable.

###Screenshots / videos

> A picture is worth a thousand words

![]({{ site.url }}/assets/iphone5-4-1.1.png "Photo from http://www.marco.org/bugshot")

And showing me what you saw when you filed the bug is far more valuable than trying to explain it in text. And if you're an iOS developer and you don't know how to do screen videos of your device with [Quicktime in Yosemite](http://apple.stackexchange.com/a/151306) then you are massively missing out. (It was a life changing feature for iOS testers!).

On Android the process for screen recording is not as clean but still doable and still very valuable. If you have Android Studio screen recording is [built in](https://developer.android.com/tools/debugging/debugging-studio.html#screenCap). If you don't then you're going to have to jump into the [command line to make your videos](http://www.cnet.com/uk/how-to/how-to-record-your-screen-on-android-4-4-kitkat/).

[Skitch by Evernote](https://evernote.com/skitch/) (available for [Android](https://play.google.com/store/apps/details?id=com.evernote.skitch&hl=en_GB) and [iOS](https://itunes.apple.com/gb/app/skitch-snap.-mark-up.-send./id490505997?mt=8)) is a great tool for annotating screenshots.

###Logs / crash reports

These are the bread and butter of reporting a crash. In my early days I had filed many bug reports detailing crashes and one of the first things the bug screener would come back and ask me for were the crash logs. These are invaluable to developers. Even if your crash is easy to replicate, the crash log can let the dev know exactly where to start looking. It can also help group seemingly unrelated bugs together. A stack trace from two different crashes in two different areas can lead back to a single point of failure and save the screener or the dev time in trying to replicate the issue and trace it back.

###One issue per report

> After payment has been verified - app crashes (using a iphone 4s, not sure if its the phone or the app?). Also when entering card details it says mm/yy - please specify if you need expiry or valid from date. Also CVC - perhaps entering a phrase or a question mark and hover over saying three digit security code at signature strip on back may be helpful. When going through categories, movement is a little bouncy and will not scroll through properly.

<iframe src="//giphy.com/embed/5DpF7t1WzLnCU?html5=true" width="240" height="180" frameBorder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

Where do you even start?! This one really seems obvious to some but to many it's not. Be concise. Be focused. Have a point.

###Never assign blame

Bugs were not introduced into the app just to frustrate you. The developer who introduced or missed the bug is going to be more frustrated and upset that it shipped than you are. Be professional. Be empatheic. Be helpful. Don't make it personal.

Bug reports are not the place for you to air your personal grievences about the state of the software or the world in general. That's what Twitter is for \</sarcasm\>. Seriously, have some empathy when filing bugs. Odds are you have been on the receiving end and know what it feels like. So remember that and file the types of bugs you would like to see yourself.

###Conclusion

The real purpose of bug reports are to be helpful. They are to solve a problem and to make things better.

And always remember the first bug report and the woman responsible for giving us the term. Thank you Admiral Grace Murray Hopper!

![]({{ site.url }}/assets/Commodore_Grace_M._Hopper,_USN_(covered).jpg "Admiral Grace Murray Hopper: Photo Courtesy of United States Navy, taken from Wikipedia")
![]({{ site.url }}/assets/H96566k.jpg "First Computer Bug: Photo Courtesy of the Naval Surface Warfare Center, Dahlgren, VA., 1988. - U.S. Naval Historical Center Online Library Photograph NH 96566-KN")
