---
layout: post
title: "Google's Lighthouse is a quality signal that Claude Code can optimise for"
date: 2026-09-25
---

AI models are great at achieving a very clearly defined measure of success. However, sometimes the challenge is defining it, and allowing the model to check how well it is performing against that measure. But if we can give the model direct access to this measurement, it can incorporate the results into its own loop. It can then implement something, check the result against the measure of success, make some more changes, and check again – repeating this loop until it has achieved "success" as defined.

When getting Claude Code to build the frontend of my photography portfolio recently, I installed the Lighthouse CLI. Lighthouse is Google's suite of tests that can be run against any website, and gives a score for performance (i.e., speed), accessibility, SEO and "best practices". This proved to be a perfect yardstick that Claude Code could use to measure the results of its changes, and Claude easily achieved a perfect score.

As a non-developer, I find it helpful to have a second opinion in my collaborations with Claude Code. Claude will happily humour me endlessly with tweaks and changes that may not really be necessary or productive to implement. With Lighthouse, I can confidently say that the site is good enough technically, and if I want to change something in the future, I'll be able to check that Claude and I don't inadvertently introduce problems elsewhere in the site.

In September, the Claude team published a [blog post describing how they improved the loading time of claude.ai and the desktop app](https://claude.dev/blog/how-we-made-claude-ai-faster/) by giving Claude granular visibility into those loading times. This allowed Claude to not just find different optimisations, but verify that the changes helped. I see clear parallels with this approach and my use of Lighthouse.

Lots of our work (most?) doesn't have this kind of clear, unambiguous and real-time success metric. But when it does, it's a very helpful addition to a coding agent's setup.