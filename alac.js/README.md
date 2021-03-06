alac.js: An Apple Lossless decoder in the browser
================================================================================

The Apple Lossless Audio Codec (ALAC) is an audio codec developed by Apple and included in the original iPod.
ALAC is a data compression method which reduces the size of audio files with no loss of information.
A decoded ALAC stream is bit-for-bit identical to the original uncompressed audio file.

The original encoder and decoder were [open sourced](http://alac.macosforge.org/) by Apple, 
and this is a port of the decoder to CoffeeScript so that ALAC files can be played in the browser.

## Demo

You can check out a [demo](http://audiocogs.org/codecs/alac/) alongside our other decoders [flac.js](http://github.com/audiocogs/flac.js), [MP3.js](http://github.com/devongovett/mp3.js), and [AAC.js](http://github.com/audiocogs/aac.js).  Currently, alac.js works properly in the latest versions of Firefox, Chrome, and Safari.

## Authors

alac.js was written by [@jensnockert](http://github.com/jensnockert) and [@devongovett](http://github.com/devongovett) 
of [Audiocogs](http://audiocogs.org/).

## Building
    
Currently, the [importer](https://github.com/devongovett/importer) module is used to build alac.js.  You can run
the development server on port `3030` by first installing `importer` with npm, and then running it like this:

    npm install importer -g
    importer alac.js -p 3030
    
You can also build a static version like this:

    importer alac.js build.js

alac.js depends on [Aurora.js](https://github.com/audiocogs/aurora.js), our audio codec framework.  You will need
to include either a prebuilt version of Aurora.js, or start another `importer` development server for Aurora before
alac.js will work.  You can use the [test.html](https://github.com/audiocogs/aurora.js/blob/master/src/test.html) file
in the Aurora.js repo as an example of how to use the APIs to play back audio files.  Just include alac.js on that 
page as well in order to add support for ALAC files.

    
## License

alac.js is released under the same terms as the original ALAC decoder from Apple, which is the 
[Apache 2](http://www.apache.org/licenses/LICENSE-2.0) license.