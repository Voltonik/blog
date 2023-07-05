<h1><span className="text-primary-dark">.</span>Blog<span className="text-primary-dark">/</span>Making CS2-like Smoke Grenades in Unity<span className="text-primary-dark">/</span></h1>

# Introduction
CS2 beta access recently got released, and they [showcased](https://youtu.be/_y9MpNcAitQ) their new fancy responsive smoke grenades which are actual 3D volumes that grow and react to the environment and bullets, unlike the traditional smoke billboard textures used in other games.

Developers on twitter were clearly fascinated by that mechanic and started implementing it in their favorite game engines, some made it in Unreal, some in Godot and others in Unity.

However, I haven't seen anyone who got very far, except for [acerola](https://youtu.be/ryB8hT5TMSg), who had access to hook an analyzer between the GPU and the game to see how it was made.

This is my documentation of making it from scratch without knowing a thing about the techniques used by Valve and minimal shader knowledge.

# Voxels

<blockquote class="twitter-tweet" data-theme="dark"><p lang="en" dir="ltr">My take (so far) on CS2 smoke bombs <a href="https://t.co/4soGmOCVa3">pic.twitter.com/4soGmOCVa3</a></p>&mdash; Mark Asaad (@_markasaad) <a href="https://twitter.com/_markasaad/status/1649570285815775232?ref_src=twsrc%5Etfw">April 22, 2023</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>