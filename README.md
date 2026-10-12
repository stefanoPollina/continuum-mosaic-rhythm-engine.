# Continuum Mosaic · Rhythm Engine

A standalone, browser-based 40-track rhythm workstation built with HTML, JavaScript and the Web Audio API. It is being developed as a future component of Continuum Mosaic, while remaining independently usable.

## Getting started

Open `index.html` in a modern browser and select **ACTIVATE AUDIO**. Choose a drum-machine-inspired kit, select **GENERATE DEMO SAMPLES**, upload your own audio, or assemble a custom kit using the Kit Voice Loader. Press **START** to play the pattern, or tap the instrument pads to audition sounds directly.

## Sound Sources and kit building

There are 40 independent instrument tracks. Each can use a sample, a synthesised voice or a hybrid of the two. Upload an audio file alongside a track, or choose from the built-in drum-machine-inspired voice banks. These banks are original synthesis interpretations, not recordings of the original hardware.

The **Kit Voice Loader** lets you select a source bank and instrument, then add that voice to the next empty track, replace a chosen track, or append a bank to available tracks. **LOAD SELECTED KIT** deliberately replaces the current kit arrangement. The Sound Sources list scrolls internally, keeping the rest of the workspace in place.

Uploaded audio can be used as a **ONE SHOT** (triggered by sequencer steps), a **SYNC LOOP** (aligned to the transport and tempo-matched by changing playback speed, which also changes pitch), or **FREE PLAY** (independent audition). For synchronised loops, set the source length in bars.

## Selected Track Voice Designer

Select a track to shape its sound without affecting other tracks. The designer provides voice templates, an audition button and controls grouped into **Strike / Transient**, **Resonant Body**, **Timbre / Tail**, and **Sample Layer**. Changes influence audition and sequenced playback. The designer remains stationary beside the internally scrolling Sound Sources panel.

## Rhythm Sequencer

The Pattern Grid contains **40 lanes** and supports **16, 32 or 64 steps** per pattern. Click a cell to turn a hit on or off; amber cells are active. The window shows approximately 16 tracks at once, with vertical scrolling for the other lanes and horizontal scrolling for longer patterns. The step header remains visible while navigating.

Use **BPM** to set tempo, **Swing** to adjust timing feel, and **RANDOMISE PATTERN** or **CLEAR PATTERN** to generate or reset step arrangements. **START** and **STOP** control transport playback.

## Live pads, mixer and effects

Forty rounded-square **Live Instrument Trigger Pads** let you play tracks directly. Keyboard shortcuts are available when you are not typing: **1–0** trigger tracks 1–10, and **Q–P** trigger tracks 11–20.

The **Track Mixer** provides independent level, pitch, pan and low-pass-filter controls, plus audition, for each of the 40 channels. The **Shared Effects Rack** offers 16 effects with individual enable switches and wet-level controls. Effects start bypassed; **BYPASS ALL EFFECTS** turns them off together.

## Saving projects

**SAVE PROJECT** stores the current pattern, voice assignments, sound-design parameters, mixer settings and effects settings in the browser's local storage. **LOAD PROJECT** restores the saved settings in that browser. Uploaded audio files are **not** embedded in the save: you must load those files again after reopening the project. Browser storage is not a portable project file or cloud backup.

## Technical notes

The audio path combines sample and/or synthesised voice generation with per-track gain, pan and filtering, optional shared effects and master output. Sequencing is separate from audio routing to support later integration with Continuum Mosaic.

This is a developing prototype, not a finished commercial drum-machine emulation. The original Continuum Mosaic application remains separate and unchanged.
