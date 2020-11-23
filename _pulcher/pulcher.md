---
title: "core of pulcher"
excerpt: "core of pulcher"
---

This is the current public page for Core of Pulcher.

Core of Pulcher is a game coded by myself in C++, with art/assets/sounds being
done by Smilecythe. I use my own plugin-based engine, though I pull in a lot of
libraries such as EnTT. It is a quake-inspired 2D shooter. As far as graphics
goes, there is nothing very fancy here, this type of project calls for
performant graphics that targets a multitude of hardware, along with many other
general game-development focus.

The physics are signed-distance field based. This means that general collisions
physics with the environment are pixel-perfect, and that collisions can be
handled from even extreme velocities. Because the entire environment is laid
out on a 2D grid, I can further accelerate the SDF intersections.

I implement my own robust 2D animation system that is inspired by the typical
3D skeletal-mesh system, except, as the art is pixel-perfect, instead the
animations have to be handled using varying sprites, varying animation times,
varying joint connection spots based off the current sprite, and so forth. It
is designed to be robust enough to allow complex 2D animations to be described
in a JSON format by an artist, rather than put into the code itself.

The engine is calculated in fixed-step frames, at 90 frames per second. Fixed
timesteps are an important aspect for the game. That being said, I am planning,
to capture entire frames of data, which, combined with just a single frame of
latency, will allow interpolation between frames to desync rendering from
logical frames.

Along with the animation system, I possibly plan on writing a
"video-editor"-esque cutscene creator, which could also be used to script
various AI/gameplay actions. I really like the idea of this but something that
has to be put on the backburner as other parts of the game are fleshed out.

I plan on doing writeups in the future of the work involved once it is in a more polished state.

![](https://aodq.net/files/pulcher-madness.png)
Several (unsophisticated) AI used to benchmark/test the weapons and physics
collision in the game

<a href=https://aodq.net/files/pulcher.tar.gz>Linux Download here</a>
