# Streaming of SQT features

The JavaScript client is in stream_client/index.html. It is a web user interface that captures, downsamples to 16kHz, and POSTs speech chunks to Python. Simultaneously, the interface also streams, upsamples, and reconstructs back the speech signal. The SQT features in the 16kHz are 32 harmonic energies along with the vividest fundamental frequency in the range 55-880Hz. See the following figure for the flowchart, which does not exactly describe the implementation. The LibFlac, a JavaScript library, is being used to compress the audio chunks in streaming mode. The Flac is lossless and reduces about 30% from the PCM chunk size. Another library also used is AudioContext, for the browsers' compatibilities, which also include mobile versions. This implementation simplifies the compatibility of the devices in future work. 

Figure: Flowchart of the User Interface. \
![stream_client_flowchart](stream_client_flowchart.png)

## [Live Demo](https://app.recite.live/t1) 
 Privacy Notice: your voice may be recorded when you test the demo URL. 
 

## Copying Notes

* Copy the files to the new server and check the files' permissions.  
* Modify the URLs in the index.html file to map to the new directories. 
* Also modify the "libflac.min.js.mem" URL in the  libflac.min.js file.


## Libraries & acknowledgments

### [LibFlac.js](https://github.com/mmig/libflac.js)
* libflac.min.js
* libflac.min.js.mem

### [jQuery](https://jquery.com/)
* jquery-3.5.1.min.js

### Google voice [icons](https://icon-library.com) 
* mic_off.png
* mic_on.png

