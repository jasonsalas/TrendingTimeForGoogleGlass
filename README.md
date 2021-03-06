# Trending Time - gives you a view in Google Glass of what everyone's buzzing about
## A Glassware application using Twitter's trending topics

![Trending Time surfaces the latest trending topics on Twitter](https://dl.dropboxusercontent.com/u/12019700/glass-dev/trendingtime/github-REAME-cover.png)

### Project description
This project is a port to Glass of an app [originally built for Android Wear](https://play.google.com/store/apps/details?id=wearables.jasonsalas.com.trendingtime) and made available as [an open source tutorial](https://github.com/jasonsalas/TrendingTime) that conveniently surfaces the latest trending topics from Twitter in the wearer's periphery. The aim is not only to let the user see what's trending at the moment - but also to let the user drill-down into the actual tweets constituting that trend. Users will be able to send a selected trending topic to their phone or to Chrome on the desktop to get tweets about a popular topic - at the pulse it's happening. They can also view Twitter's mobile site directly on Glass. 

The wearable ethos isn't ruined by trying to keep up with trends at that pace on Glass...but people are empowered with the ability to see why something's captured the public's attention and let them participate in a normal way.

### Tech talk presentation
You can review the slide deck that details this project [here](http://www.slideshare.net/jasonsalas/trending-time-on-google-glass).

### Sideloading instructions
This app is currently under review by Google, so until it goes live in [MyGlass](http://google.com/myglass), you can [download the APK here](https://github.com/jasonsalas/TrendingTimeForGlass/releases) and then sideload it by connecting Glass to your computer via USB and then executing the following at a command prompt:
**adb install -r TrendingTimeForGlass-v0.1.apk**

### Target audience
The Glassware is geared towards people heavily involved in social media and popular culture, with an interest in what's going on around them. The roadmap is to have the data eventually be increasingly dynamic (faster updates) and contextual (relevant to their location, surroundings, proximity to friends, etc.). 

At it's core, Trending Time serves as a fun utility that's entertaining, informative, and helpful - keeping users in the know about what the buzz online is.


### Usage flow
Have a look at [Trending Time's usage flow](https://drive.google.com/file/d/0B4vMEmrUkj0qOVJCT2k5TjZBSG8/view?usp=sharing) in [Glassware Flow Designer](https://developers.google.com/glass/tools-downloads/glassware-flow-designer).

To launch Trending Time, say, _"OK, Glass...see what's trending"_. The card launches to the left of the home screen. Tapping on this card at any time brings up a series of commands, as follows:

**Send to Phone**

![Send to Phone](https://dl.dropboxusercontent.com/u/12019700/glass-dev/trendingtime/2.png)

Tapping on this menu items uses [Pushbullet](http://pushbullet.com) (requires an account and authorization) to send a selected trending topic as a notification to your designated Android or iOS phone. (It also works for tablets.)

A new pushed trending topic arrives on your phone's notification drawer.
![Push example Step 1](https://dl.dropboxusercontent.com/u/12019700/glass-dev/trendingtime/push1.png)


Tapping on the notification brings up the pushed trending topic link in Pushbullet.
![Push example Step 2](https://dl.dropboxusercontent.com/u/12019700/glass-dev/trendingtime/push2.png)


Tapping the link gives you the ability to view tweets in Twitter's mobile app (if installed) or your mobile browser.
![Push example Step 3](https://dl.dropboxusercontent.com/u/12019700/glass-dev/trendingtime/push3.png)


**Send to Chrome**

![Send to Chrome](https://dl.dropboxusercontent.com/u/12019700/glass-dev/trendingtime/3.png)

Tapping on this menu items uses [Pushbullet](http://pushbullet.com) (requires an account and authorization) to send a selected trending topic to Chrome on your desktop PC or laptop.

![Send to Chrome](https://dl.dropboxusercontent.com/u/12019700/glass-dev/trendingtime/view-desktopbrowser.png)


**View in Browser**

![View in Browser](https://dl.dropboxusercontent.com/u/12019700/glass-dev/trendingtime/4.png)

Tapping on this menu items allows you to view Twitter's mobile web UI to review tweets making up the trending topic directly on Glass.

![View in Browser](https://dl.dropboxusercontent.com/u/12019700/glass-dev/trendingtime/view-glassbrowser.png)


### Architecture
Trending Time is intended to be a fun utility to use, and also a learning tutorial for Glassware development. Just like [it's Android Wear cousin](http://www.slideshare.net/jasonsalas/trending-time-datadriven-watch-face-development-for-android-wear), it's open source and free to examine. This Glass version is based on [live cards](https://developers.google.com/glass/develop/gdk/live-cards), and uses a [shared proxy handler on Google App Engine](https://github.com/jasonsalas/TrendingTime/wiki/Custom-proxy-on-App-Engine) to access [Twitter's API](https://dev.twitter.com/rest/reference/get/trends/place) to access the latest trending topics for the **"USA"** region.

It also uses the [GDK authentication scheme](https://developers.google.com/glass/develop/gdk/authentication) to access the [Pushbullet API](https://docs.pushbullet.com/http/) in order to send selected trending topics to your phone or desktop version of Chrome so you can see how the topic got so popular, and what people are saying about it in real time.

Feel free to submit bug reports, pull requests, and fork the code and make it your own. There's lots that can be done with the core idea. I'd love to see what you do with it!

---

You can find out more Glassware tips in my book, [Designing and Developing for Google Glass](http://www.amazon.com/Designing-Developing-Google-Glass-Differently/dp/1491946458), by O'Reilly & Associates. **Thanks for your support! :)**
