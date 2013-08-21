# Getting started

Following [this example](http://delog.wordpress.com/2011/04/26/stream-live-webm-video-to-browser-using-node-js-and-gstreamer/)

Start installing Gstreamer, download from [here](http://docs.gstreamer.com/display/GstSDK/Installing+on+Mac+OS+X). Package files will
be in `/Library/Frameworks/GStreamer.framework/Commands`. You can test
it by doing

    # Sets up your path, assuming standard Gstreamer path
    $ source env.sh 
    $ gst-launch-0.10 autovideosrc ! video/x-raw-yuv,framerate=\(fraction\)30/1,width=640,height=480 ! ffmpegcolorspace ! autovideosink

Try the node.js server:

    $ source env.sh
    $ npm install
    $ node streamer.js
    
And then go to http://localhost:9001/
