* VIDEO ELEMENT EXTENDED

This goal of this project is to
create a simple wrapper for video web components.

This module Uses HTMLElementExtended to create a number of video webComponents that
know how to display videos from a variety of sources (based on the URL)
allowing a single <ContentVideo> component to handle
YouTube, Vimeo, Internet Archive, WebTorrent etc.

This component can take a variety of forms to display different sources of video. Currently supported are...

// To include a You tube video
// Note that you-tube regularly breaks APIs.
<content-video src="https://youtube.com/watch?v=xxxxx"></content-video>

// To include a web torrent video. 
// Note that typically this will fall back to HTTP and then share to others viewing at the same time
<content-video torrent="A1B2C3" file="aa/bb.mp4"></content-video>

// To include a file from the Internet Archive
<content-video archiveitem="Banana" file="doco.mp4"></content-video>

// To include a regular video
<content-video src="https://foo.com/bar.mp4"></content-video>

**Usage**

In particular there is no compile-time step for this module.

To use this,
To a caller add to `package.json/dependencies`
```
"video-element-extended": "^0.0.1",
```
Then in your webcomponents.js file for example include it with
```
import { ContentVideo } from './node_modules/video-element-extended/videoelementextended.js';
```
In brief.

Note - This is under development - but is in active use on my website mitra.biz 
If you use it please introduce yourself in a git issue, 
and I'll bear this in mind when making any breaking revisions. 

** Upgrading packages
There is a fair bit of instability at the moment (July 2023) in npm 
with modules and commonJS coexisting. 
The following document some of the issues with upgrading
*** webtorrent
At some point webtorrent.min.js was moved into dist/ certainly there in 2.1.13
