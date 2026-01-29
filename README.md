# ASH — AI-Driven Cinematic Visual Intelligence

ASH is an AI-driven cinematic visual intelligence demo that orchestrates AI-generated video and imagery into immersive, high-end visual experiences with a futuristic corporate aesthetic.

## Live Demo

[View ASH Demo](https://ash-demo.vercel.app)

## Concept

Four 10-second cinematic clips form a 40-second visual arc:

| # | Clip | Camera Motion | Narrative |
|---|------|---------------|-----------|
| 1 | IGNITION | Dolly forward | Entry — anticipation, precision |
| 2 | STRUCTURE | Slow orbit | Observation — contemplation |
| 3 | EXPANSION | Push-in | Scale — quiet power |
| 4 | SILENCE | Dolly backward | Closure — serenity |

Arc: **enter → observe → expand → retreat** (a breathing cycle)

## Visual Identity

- **Palette:** Deep blacks, metallic grays, cold blue, amber accents
- - **Surfaces:** Polished floors, dark glass, brushed metal, volumetric light
  - - **Camera:** Slow, controlled — dolly, orbit, push-in
    - - **Lighting:** Low-key, backlit, volumetric
      - - **Constraints:** No people, no text, no logos, no UI
       
        - ## Tech Stack
       
        - | Component | Tool |
        - |-----------|------|
        - | Video Generation | Runway Gen-3 |
        - | Image Generation | Craiyon / Midjourney |
        - | Frontend | HTML, CSS, JavaScript |
        - | Hosting | Vercel |
        - | Video Assembly | FFmpeg |
       
        - ## Project Structure
       
        - ```
          ash-demo/
          ├── index.html
          ├── assets/
          │   ├── video/
          │   │   └── ash-final.mp4
          │   ├── clips/
          │   │   ├── 01-ignition.mp4
          │   │   ├── 02-structure.mp4
          │   │   ├── 03-expansion.mp4
          │   │   └── 04-silence.mp4
          │   └── images/
          │       └── cover.png
          ├── pitch/
          │   ├── ash-pitch.mp4
          │   └── ash-deck.pdf
          └── README.md
          ```

          ## Video Assembly

          ```bash
          echo "file 'assets/clips/01-ignition.mp4'" > filelist.txt
          echo "file 'assets/clips/02-structure.mp4'" >> filelist.txt
          echo "file 'assets/clips/03-expansion.mp4'" >> filelist.txt
          echo "file 'assets/clips/04-silence.mp4'" >> filelist.txt
          ffmpeg -f concat -safe 0 -i filelist.txt -c copy assets/video/ash-final.mp4
          ```

          ## Use Cases

          - Corporate brand videos and visual identities
          - - Immersive event presentations
            - - Product launch cinematics
              - - AI-powered creative pipeline demonstrations
                - - Visual prototyping for agencies and studios
                 
                  - ## Hackathon
                 
                  - Built for [lablab.ai Hackathon 2026](https://lablab.ai).
                 
                  - ## License
                 
                  - MIT
