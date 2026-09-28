---
layout: post
title: "Video files are useful inputs and outputs, with ffmpeg and vision-aware models"
date: 2026-09-28
---

Today I was working on a plan for a home improvement project. I walked around my home filming with my iPhone on the 0.5x wide-angle lens, in 4K, narrating what I was seeing and what I wanted to change. With two added capabilities, Claude Code is able to make good use of this as input context to better understand me, and as output for me to share with others.

The first added capability is the command-line tool [ffmpeg](https://github.com/FFmpeg/FFmpeg). This gives Claude Code lots of generally useful capabilities for working with video files – resizing, converting between file formats, extracting audio, trimming, etc. I think of this basically like a video editor application that Claude can use.

The second capability is an API key with billing set up on OpenRouter. Anthropic models can't accept video as an input, but other models available on OpenRouter can. I like having just one API key that gives me access to every model I'd care to try at the moment. Claude can discover models suitable for the task at hand by hitting an endpoint that OpenRouter provides for listing currently available models.

Here's how Claude used these capabilities together for me today.

First, it downsized the 4K video files in order to send them to [Gemini 3.8 Flash](https://openrouter.ai/google/gemini-3.8-flash). Because Claude and I had already been working on this home improvement plan in our session, it was able to write its own prompt for Gemini, aimed at extracting the nature of my physical space as well as my own impressions of what I don't like about it today, and what I aim to improve.

It also separately transcribed my speech as a raw, unprocessed input.

Finally, using ffmpeg, it extracted stills – this time from the 4K original footage – illustrating various points I had made about the space, and embedded them in the document that represents the output of this particular plan.

Recording the videos only took a few minutes, but because of the context that Claude had from an already running conversation, ffmpeg's ability to work generally with the files, and OpenRouter's video-aware model access, lots of useful information could be extracted from the videos without wasting any of my Claude session's context window.
