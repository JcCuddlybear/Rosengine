Rosengine
Create. Publish. Own it.
Self-hosted multilingual 3D cinematic publishing suite. Off grid. Off dependencies. Community open source.

What it is
Rosengine makes multilingual 3D cinematic publishing trivial — three files per language, no re-export, no game engine, no cloud.
A browser-native player for interactive 3D scenes — GLB characters with ARKit lipsync, Gaussian Splat environments, audio, video, and subtitles — with a localisation architecture that makes adding a new language as simple as dropping in three files.
No Unity. No Unreal. No Pixel Streaming server. No platform account. No ongoing fees.
Your scene lives at a URL you own, on a server you control.

The localisation breakthrough
The character mesh and body animation never change between languages. Only three assets change per locale:

The VO audio file
The lipsync GLB (generated in ~30 seconds from audio via NVIDIA Audio2Face, locally on an RTX GPU)
The subtitle text file

Adding Hindi to an English scene: drop in three files. No code changes. No re-export. No production day.
Three languages confirmed working: English, Hindi, Cantonese.

Scene types

GLB Static — 3D character, no animation
GLB Lipsync — 3D character with ARKit-driven lipsync
Gaussian Splat — photorealistic environment capture
Slide Animation — image sequence with audio
Video — standard video with subtitles
Audio — audio-only with subtitles

All scene types support runtime language switching via URL parameter (?lang=en, ?lang=hi, ?lang=yue).

Jc Cuddlybear
Jc Cuddlybear is the first open ARKit-compatible browser-ready 3D character.

52 ARKit morph targets
Full lipsync compatibility
Production-ready GLB
Released under CC BY-NC licence
No MetaHuman EULA — entirely original mesh

Coming with the v1.0 release.

Architecture
scene/
  manifest.json          ← scene description
  en/
    audio.mp3            ← English VO
    lipsync.glb          ← English lipsync animation
    subtitles.vtt        ← English subtitles
  hi/
    audio.mp3            ← Hindi VO
    lipsync.glb          ← Hindi lipsync animation  
    subtitles.vtt        ← Hindi subtitles
  character.glb          ← mesh (shared across all languages)
  body.glb               ← body animation (shared)
  environment.splat      ← Gaussian Splat (shared)
Adding a language = adding one folder with three files. No code changes ever.

Philosophy
Create. Publish. Own it.

No platform dependency — your content lives at your URL
No proprietary runtime — vanilla Three.js, any browser, forever
No cloud pipeline — lipsync generation runs locally on your GPU
No localisation vendor — three files, 30 seconds, any language
No ongoing fees — self-host on €6/month shared hosting


Roadmap

v0.5 — Rosengine Player, localisation system, Jc Cuddlybear character kit
v0.6 — Studio editor, Audio2Face pipeline documentation
v0.7 — Gaussian Splat support, subtitle renderer (RTL + CJK)
v1.0 — Full release, community characters, open manifest standard


Related
Alaya — self-hosted AI session persistence. github.com/JcCuddlybear/alaya
Rosengine and Alaya share the same PHP infrastructure. Installing one gives you everything the other needs to run.

Licence
AGPL-3.0 — see LICENSE
Jc Cuddlybear character kit: CC BY-NC for non-commercial use. Commercial licence available separately.

Built by Christian Jelen — VFX Supervisor, Cinematic Artist. BAFTA Best Visual Effects. 30 years production pipeline experience.
