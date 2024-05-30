# Summer
# ViLoN Lab Meeting Notes
# 2024-05-30 Technical Meeting

## Experiments to Build:
### Dot Chaser Experiment
> The goal of this experiment is to establish a simple research paradigm for examining the natural optic geometry associated with gaze-ground fixations during locomotion. 

"Ground-Dot Paradigm"

#### Core Features
- eye tracking from quest pro
- Ground Plane
    - should contain (or be defined by) the walkable space in the experiment
    - **gaze ground intersection** (GGI)
        - invisibly collect data on this
        - use the GGI to give fixation feedback
- Dot 
    - Dot Logic:
        - jump position when participant gets too close (hitbox)
        - jumps a certain distance within walkable space
        - jump a certain number of times (*our trial number*)
        - provide feedback to the participant based on GGI (is the dot being looked at? If so change color and/or shape)

- Data We'll Collect
    - Gaze data
    - Headset position
    - GGI 
    - Dot Position


### Horse Vision Experiment
> Purpose of this experiment is to explore if/how humans can adapt to having "hemispherical vision" (aka, horse vision - `HV`), where their eyes are on the sides of their head. This is easy and safe to play with in VR!
#### Core Features
- `HV` capabilities
    - customizing the VR Rig in Unity; moving the camera positions, changing the FOV of the cameras as best we can. 
- Projectiles
    - little dodge balls that will hit you if you don't move
    - give participant feedback if they've been hit
    - gamify the task a bit; end of every trial they have a "score"
- "trial" system
    - example: 10 10 second intervals, each interval has a different angular difference between eye positions 

## Replay App - not building this yet, but in the future
What does this do?
- Unity Game/App that takes a folder of `Ground-Dot Paradigm` data and play back the experiment
- retinotopic (camera) view -- what the subject sees in retinotopic space 
    - it could just be a replay of what the participant sees to start with
- spatial view -- a 3D view of the headset moving through 3D space, with colored gaze vectors to demonstrate where the participant is looking. This will include all the other assets in the scene as well.



# 2024-05-14 Technical Meeting

## Tools We'll Likely Use:
### General Tools
- GitHub (Code & Writing Repository)
- Discord (Team Comms)
- [VSCode (Code Editor)](https://code.visualstudio.com/)

### Collecting Data
- VR/AR Headset
    - Meta Quest Pro
    - Vive Eye Pro <- older, tethered, but higher refresh rate
- Motion Analysis Motion Capture System
- FreeMoCap
- Software
    - Unity Game Engine `C#`
    
    `OR`

    - JavaScript
        - [ThreeJS](https://threejs.org/)
        - [BabylonJS](https://www.babylonjs.com/) -> `Babylon Native`

### Analyzing Data
- Python

`AND/OR`

- R

### Writing-Up Data
- [LaTeX](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)
- [Markdown](https://www.markdownguide.org/)
    
# 2024-05-14

## Summer Plans
- Reading
    - `who?` Anyone who wants to
    - `when` whenever -BUT we'll also meet to discuss some readings
- Paradigms (Experiments) Built (everything - `Braden`, `Reid`, `Lily`)
    1. General Optic Flow stuff (Mocap [marker based] + VR/AR)
        - `Kit`, `Reid`
    2. Horse-Vision Experiment [VR] `Lily`
    3. Muller Lyer Aperture Experiment [VR]
    - Other random Research Questions
        - vanishing mill
        - 3rd person motor control (walking)
        - 3d from 2d machine learning


## Fall 
- Collect some data (early fall)
- Submit to conferences (late fall - more specifically early december.)
- Research Papers (Write it up)

### Undergraduate Research Travel
- ~$500-700
- Trent gets a Grant [trent-job]

## Homework
- Trent invites Reid to Discord, shares reading links
- Set June Meeting Time

