

## Installation

You can install the package using npm:

```bash
npm install youtube_scraper
```

## Usage

```Javascript
const { search, ytmp3, ytmp4, ytdlv2, channel } = require('@vreden/youtube_scraper');
```

## Quality Available

```Javascript
const audio = [ 64, 96, 128, 192, 256, 320 ]
const video = [ 360, 480, 720, 1080 ]
```
## Download Audio (MP3) 🎧

```Javascript
// url YouTube kamu
const url = 'https://www.youtube.com/watch?v=YOUR_VIDEO_ID';

// quality download, pilih di Quality Available
const quality = "128"

/* 
 * atau kamu bisa langsung url
 * saja untuk default quality (128)
 * example: ytmp3(url)
*/

ytmp3(url, quality)
    .then(result => {
        if (result.status) {
            console.log('Download Link:', result.download);
            console.log('Metadata:', result.metadata);
        } else {
            console.error('Error:', result.result);
        }
    });
```

## Download Video (MP4) 🗃️

```Javascript
// url YouTube kamu
const url = 'https://www.youtube.com/watch?v=YOUR_VIDEO_ID';

// quality download, pilih di Quality Available
const quality = "360"

/* 
 * atau kamu bisa langsung url
 * saja untuk default quality (360)
 * example: ytmp4(url)
*/

ytmp4(url, quality)
    .then(result => {
        if (result.status) {
            console.log('Download Link:', result.download);
            console.log('Metadata:', result.metadata);
        } else {
            console.error('Error:', result.result);
        }
    });
```

## Download YTDLV2 (MP3 & MP4) 🤖

```Javascript
// url YouTube kamu
const url = 'https://www.youtube.com/watch?v=YOUR_VIDEO_ID';

/*
 * quality download
 * pilih di Quality Available
 * bisa dalam format audio
 * maupun video
 */
const quality = 360
const quality = 128

/* 
 * atau kamu bisa langsung url
 * saja untuk default quality (128 & 360)
 * example: ytdlv2(url)
*/

ytdlv2(url, quality)
    .then(result => {
        if (result.status) {
            console.log('Download Link:', result.download);
            console.log('Metadata:', result.metadata);
        } else {
            console.error('Error:', result.result);
        }
    });
```

## Search Video 🍟

```Javascript
const query = 'your search term';

search(query)
    .then(result => {
        if (result.status) {
            console.log('Search Results:', result.results);
        } else {
            console.error('Error:', result.result);
        }
    });
```

## Stalker Channel 😈

```Javascript
const query = 'your username channel';

channel(query)
    .then(result => {
        if (result.status) {
            console.log('Channel Results:', result.results);
        } else {
            console.error('Error:', result.result);
        }
    });
```
