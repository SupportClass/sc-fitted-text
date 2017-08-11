# \<sc-fitted-text\> [![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/SupportClass/sc-fitted-text) [![Build Status](https://travis-ci.org/SupportClass/sc-fitted-text.svg?branch=master)](https://travis-ci.org/SupportClass/sc-fitted-text) [![Coverage Status](https://coveralls.io/repos/github/SupportClass/sc-fitted-text/badge.svg?branch=master)](https://coveralls.io/github/SupportClass/sc-fitted-text?branch=master) ![Polymer 2 only](https://img.shields.io/badge/Polymer%202-only-blue.svg)

A Polymer 2.x element for playing video assets with discrete enter, exit, and loop parts.

## Motivation
Sometimes we have assets that just doesn't make sense to implement purely in code. The asset might be too complex, too performance-intensive, or maybe we just don't have the time. In these cases, we often will pre-render the asset and slice it into discrete `enter`, `loop`, and `exit` parts.

## Installation
```bash
bower install --save SupportClass/sc-fitted-text
```

## Example
<!--
```
<custom-element-demo height="225">
  <template>
    <link rel="import" href="sc-fitted-text.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<sc-fitted-text
	id="demo"
	enter-src="demo/enter.webm"
	loop-src="demo/loop.webm"
	exit-src="demo/exit.webm">
</sc-fitted-text>

<button onclick="demo.enterAndLoop()">Enter and Loop</button>
<button onclick="demo.exit()">Exit</button>
<button onclick="demo.exit(true)">Fast Exit</button>
```

## How do I make transparent videos like the demo?
Some browsers (only Chrome and Firefox at the time of this writing) support an alpha channel in `.webm` videos. However, most tools don't actually have support for rendering or encoding a `.webm` with this alpha channel, so you will probably have to first render out in a format that _does_ support alpha (such as `.avi` or `.mov`) and _then_ encode the `.webm` using FFmpeg:

```bash
# This is just an example. There's tons of parameters that you can play with, but this will get you going.
ffmpeg.exe -i enter.avi -c:v libvpx -b:v 3000k -c:a libvorbis -b:a 128k enter.webm
```
