So... this is basically Reveal.js, but with the Grunt/Node stuff stripped out.

I just take a release snapshot of Reveal, stripped out what I did not want.

To install:

    wget https://github.com/aaronr/revealz/archive/master.zip
    unzip master.zip
    mv revealz-master myNewPresentation
    cd myNewPresentation/

If you are already on a server in a web accessible directory... just got to the URL and you are rolling.

To run a local (port 8000) webserver (to get the markdown includes to work) I just use:

    python -m SimpleHTTPServer

Every server has python... and I like Python.

The main idea is that the index.html file has been stripped down, the js config moved to a config.js file, and the FULL presentation content comes from slides.md.

You heard me... ALL the slide content is in one file... slides.md

You use `--SLIDE--` on a line by itself to indicate the next horizontal slide.  You use `--SUBSLIDE--` on a line by itslef to indicate the next vertical sub-slide.

You can just use html comments inline to write notes etc:

    <!------------------------------------------------------------>
    --SLIDE--
    <!-- Topic: xxx -->
    
    <h1>Slide 15</h1>
    
    --SUBSLIDE--
    
    <h2>Sub Slide 15--1</h2>

There is an images directory and you can either use markdown or raw html to embed images etc.

Thats it... pretty basic, but a template for a single markdown page presentation in Reveal.js
