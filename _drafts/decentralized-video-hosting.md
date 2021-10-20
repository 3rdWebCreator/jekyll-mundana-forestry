---
layout: post
categories:
- Web3
tags:
- Fleek
- Video
- Hosting
- Video JS
title: Decentralized Video Hosting
author: tim
image: ''

---
## Your YouTube channel isn't yours.

YouTube is great. It's fast. It's easy. And of course, it's free. But if you want to be in complete control of your content, you will want to build your own platform, on your own web site.

Generally that means using a content distribution network (CDN). A web site host will not always provide enough space for large files like videos. A CDN is designed to store large files, and serve them up quickly.

For a completely decentralized Web3 option, videos for _Creator_ will be hosted on [IPFS](https://ipfs.io/) via [Fleek Storage](https://fleek.co/storage/). A recent post titled _The Squeeze on Content Creators_ was the first on the site to featured an embedded video. Read on for a complete breakdown of the process to use for hosting your own videos.

First, the open source [Video JS ](https://videojs.com/)video player was added to the _Creator_ web site, which is built with Jekyll. Following the path of least resistance, the default player was imported from the [Video JS CDN storage](https://en.wikipedia.org/wiki/Content_delivery_network) by simply copying and pasting two lines of code into the site's HTML. The link to the video player CSS was inserted in the header. Then, the player's JavaScript is placed right before the closing body tag.

The video was embedded using the example HTML from that same [Video JS](https://en.wikipedia.org/wiki/Content_delivery_network) page. For _Creator_ two optional CSS classes were included. Adding vjs-big-play-centered centers the play button in the player thumbnail image. And \[CSS\] made the player size responsive instead of a fixed dimension.

The poster image is located in the site's assets folder in Jekyll. The video location comes from Fleek Storage.

To upload the video file to Fleek, look for the Storage link in the account. Click the upload button and select your video file. It may take a bit, but eventually you should see a confirmation that your video has been uploaded. Click the "Verify on IPFS" link, and copy the URL. Paste that in as the source for your video on your site, and you are good to go. Congrats, video creator, you have successfully decentralized your content. Now pop some popcorn, and mash that play button.