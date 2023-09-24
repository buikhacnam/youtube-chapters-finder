<div align="center">
  <div>
    <h1 align="center">youtube-chapters-finder</h1>
  </div>
	<p>A tiny npm library that helps get chapters from any Youtube video.

<a href="https://www.npmjs.com/package/youtube-chapters-finder"><img src="https://img.shields.io/npm/v/youtube-chapters-finder" alt="Current version"></a>

</div>

---

## Problem
I wanted to get the chapters from a youtube video, but I couldn't find such functionality in the [Youtube API](https://developers.google.com/youtube/v3). So I made one.

## Installation

`npm i youtube-chapters-finder`

## Example

Get all chapters from this youtube video: https://youtube.com/watch?v=Gi8LUnhP5yU

```js
import YoutubeChaptersGetter from 'youtube-chapters-finder'

async function getChapters() {
  return await YoutubeChaptersGetter.getChapter('Gi8LUnhP5yU') // video id
}

// expected output:
[
  {
    title: 'Introduction',
    time: '0:00',
    url: 'https://youtube.com/watch?v=Gi8LUnhP5yU&t=0s'
  },
  {
    title: 'Are there intelligent life out there',
    time: '2:27',
    url: 'https://youtube.com/watch?v=Gi8LUnhP5yU&t=147s'
  },
  {
    title: 'We dont mean all of space',
    time: '3:02',
    url: 'https://youtube.com/watch?v=Gi8LUnhP5yU&t=182s'
  },
  {
    title: 'Intelligent life',
    time: '5:42',
    url: 'https://youtube.com/watch?v=Gi8LUnhP5yU&t=342s'
  },
  ...
]

```

[![Edit bold-ellis-6rg1t](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/hardcore-bush-nq2t26?file=/src/index.mjs)

## Usage

This package is intended to be used in server-side applications (Next.js included). I may add support for client-side applications in the future.


## License

MIT License
