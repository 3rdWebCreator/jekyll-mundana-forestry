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

YouTube is great. It's fast. It's easy. And of course, it's free. But if you want to be in complete control of your content, you will need to build your own platform, on your own web site. Generally that means using a content distribution network (CDN), which is designed to store large files, and serve them up quickly.

### A Web3 Solution

For a completely decentralized option, videos for _Creator_ will be hosted on [IPFS](https://ipfs.io/) via [Fleek Storage](https://fleek.co/storage/). A recent post titled [_The Squeeze on Content Creators_](/evidence-a/) was the first on the site to feature an embedded video. Read on for a complete breakdown of the process to use for hosting your own videos.

### Video JS

First, the open source [Video JS ](https://videojs.com/)video player was added to the _Creator_ web site. Following the path of least resistance, the default player was imported from the [Video JS CDN storage](https://en.wikipedia.org/wiki/Content_delivery_network) by simply copying and pasting two lines of code into the site's HTML. The link to the video player CSS was inserted in the header. 

    <link href="https://vjs.zencdn.net/7.15.4/video-js.css" rel="stylesheet" />

Then, the player's JavaScript is placed right before the closing body tag.

    <script src="https://vjs.zencdn.net/7.15.4/video.min.js"></script>

The video was embedded using the example HTML from that same [Video JS](https://en.wikipedia.org/wiki/Content_delivery_network) page. For _Creator,_ two optional CSS classes were included. Adding `vjs-big-play-centered` centers the play button in the player thumbnail image. And `vjs-fluid` made the player size responsive instead of a fixed dimension.

Here's an example of what the complete video element HTML looks like.

    <video id="wired" 
    class="video-js vjs-fluid vjs-big-play-centered" 
    controls preload="auto" 
    width="640" 
    height="264" 
    poster="/assets/images/thumbnail.jpg" 
    data-setup="{}"> 
    <source src="https://ipfs.fleek.co/ipfs/bafybeiatdr6dbsm7q4wo3iwawq6iqgfcznpx6prkudh23hrzdzm6fy4rhi" 
    type="video/mp4" /> 
    <p class="vjs-no-js"> To view this video please enable JavaScript, and consider upgrading to a web browser that <a href="https://videojs.com/html5-video-support/" target="_blank" >supports HTML5 video</a > 
    </p> 
    </video>

The thumbnail or poster image is located in the site's assets folder in Jekyll. The video location comes from Fleek Storage.

### Fleek Storage

To upload the video file to Fleek, look for the Storage link in the account. Click the upload button and select your video file. It may take a bit, but eventually you should see a confirmation that your video has been uploaded. Click the "Verify on IPFS" link, and copy the URL. Paste that in as the source for the video on your site, and you are good to go. Congrats, video creator, you have successfully decentralized your content. Now pop some popcorn, and mash that play button.