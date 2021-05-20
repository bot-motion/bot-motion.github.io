---
title: "Learning to Seek: Tiny Robot Learning (tinyRL) for Source Seeking on a Nano Quadcopter"
collection: publications
permalink: /publication/2019-09-learning-to-seek
excerpt: ''
date: 2020-09-01
venue: 'arXiv'
paperurl: 'https://arxiv.org/abs/1909.11236v5'
---
This is an amazing paper showing the power of simple solutions. I'm a fan of [bio-inspired stuff](https://www.epfl.ch/labs/lis/); and while this is not 'officially' inspired 
by insect life, the Crazyflie here shows a 'seeking' behavior for something that could be food (a landing pad, the [Qi charging deck](https://store.bitcraze.io/collections/decks/products/qi-1-2-wireless-charging-deck)) or, as in the paper, a light source. 

I had already aquired a chemical sensor to play around with, and implement a seeking behavior. This paper really drives home that it should be possible to build a system that a) takes off
with a full battery, b) seeks a light or odour source, exploring as long as possible, and then c) returning 'home' driven by the need to re-charge. 
Reminds me of a bee! I read a paper recently that [described the difficulties of landing on a pad guided by camera only](https://www.mdpi.com/1424-8220/19/21/4703/htm) 
-- but perhaps this could be made simpler by putting a long stick with (passive) height markers up next to the Qi deck, allowing the flie to 'watch' the stick while kind of 
going down like in an elevator.

While it's impressive and a strong message that they used a simple system instead of a 'complicated' vision based system, I still think that it would
be interesting and possible to use the AI deck to recognize 'the source' that the flie is supposed to seek, substituting the role of the light sensor for the camera.

The sad truth is that I recently spent hours trying to debug UART communications between two decks on the Crazyflie, so this project will most likely
never come true. But I enjoy imagining this stuff, it's at the right intersection between doable in principle and challenging.

[Download paper here](https://arxiv.org/abs/1909.11236v5); [the code is available on github](https://github.com/harvard-edge/source-seeking).

There's a [video on Youtube](https://www.youtube.com/watch?v=wmVKbX7MOnU).

