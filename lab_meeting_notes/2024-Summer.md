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

# 2024-07-30
## Trents meeting with Bill Warren

dora angelaki - chasing dots through optic flow -- optic flow and extra-retinal signals, dot chasing

Jim Todd & Ecological Optics - Bill: What Neurons are doing is like template matching - Bill has always liked pulling out the differential motion in the same depth, but there aren't a lot of examples of this in natural scenes. Heger and Jepson 1992 paper the subspace algorithm. Bill worked through this paper, Lappe and Raschuk paper, Bill finally understood this; what the subspace algorithm does - it doesn't detect the radial flow pattern, it detects the error in the radial flow pattern. If I have a template that doesn't match the perceived flow, it calculates the error of these flow patterns.
- Markus Lappe went on to fit this Heeger & Jepson 1992 model
- this is the best computational solution
- find the perpendicular error, measure the motion opponency 

the dot chaser experiment is the exact kind of thing that these models are trying to handle
- models are trying to handle fixating stationary points in the environment
- including Olivers model
- the case of the flat plane is surprisingly hard
- some of the models fail because of that -- they're trying to get out the rotational and translational components of the eye's motion
- they'll take the flow field and break it into two parts
- by doing this continuously, we're getting a whole series of these instantaneous velocity fields
- there is some controversy if neurons can extract more than *A* velocity field - acceleration of a dot, jerk of a dot, etc.
- Bill: there is almost no evidence that neurons are selective for anything other than velocity
- Bill just reviewed a paper from a student of Heeger that claimed they found more evidence of neurons 

Questions that people are concerned with:
- when you add noise into the flow field, most models fall apart
- the visual system itself has a lot of noise in it
- noise is a big issue
- in this kind of case it is interesting to look at: "what are people doing over time?"
-- do they cancel out all the rotation in the flow field
-- do they turn and go straight toward it, and eliminate the rotation
-- some models from the late 80's and 90's Wang and Swap: if you're fixating the target but you're not heading to the target, there will be flow across the line of sight towards the target, if you're going the other way, there is flow in the other direction towards the target
- there still isn't evidence that the visual system is sensitive to local divergence and curl 
- Warren et al Nature Neuroscience 2001 
- rotations in the groundplane around the fixation point are a good idea but you've got to be careful about what you're manipulating
- Li Li did a lot of work in this space
- Oliver Layton, too. Built recurrent NN's of MST

- Ken Britton

There hasn't been a very detailed analysis of 

Old results from the cat - more cells responsive to expansion to 


Horse Vision: 
- Eli Pelli; they did weird optics. Take someone who only has foveal vision and see if you take spherical vision and put it in their fovea
- prism goggle; the phenomenology doesn't flip upside-down but people learn to adapt to it. but the phenomenology wasn't carefully analyzed 

- literature on adapting to new glasses -- if you get lenses that magnify the world it takes you a while to adapt. In a week, you've adapted to that and the world doesn't look distorted any more. Two calibrations (you calibrate to your glasses and without your glasses) 


Bill & Mario realized the limits of TDDC, Kei is now looking at causation entropy (a development of transfer entropy, which is a development of mutual information)

# 2024-08-06 -- Oliver Layton

- challenges involved
	- scenarios we're interested in
	- Brett & Bill: "Information input space"
	- combinations of pieces of information that are used for control
	- it takes a lot of time to build even that stuff up
	- challenges with the neuroscience itself - there's a lot we don't know
	- the problem is so under-constrained
		- we know a lot about the retina
		- we know about V1
		- but as the information goes up, we don't know what's going on
		- we don't know enough about it to know what exactly is doing
		- a lot of Oliver's work is positing how the brain might behave 
		- fundamental problems that we don't know much about
		- example bottleneck: rotation problem 
			- "is the brain doing this visually or with extra-retinal signals?"
- a whole other "leg of the stool" is the modeling approach
	- e.g., deep learning. Set up architecture, click go, analyze the properties
	- what kind of deep learning is best for task
	- deep learning model might solve the problem, but you don't know how it's doing it
	- you can do neuroscience on deep neural nets, but is it worth your time and attention to do it on *that* network. 
		- you might find x y and z
- problem with Jon and Kate dataset is that it's unlabeled - you don't know what the heading is, about the ground truth - it's basically "unsupervised"
> heading vs. foot placement

- basic dataset -> "that would be perfect"
	- very specific task, label the data accurately
	- collect a lot of it
	- that would be useful - probably more useful than the Jon dataset 
- the Jon and Kate story about retinal optic flow is too extreme to be true
	- their argument is kind of a strawman, it's not supported by the data that exists out there
	- you can get really similar patterns for different motion
	- you can also get very different flow patterns for similar motion
- another hot topic in optic flow right now is "flow parsing" - estimate the motion of a moving object with flow coordinates
	- there is evidence that the brain is transforming the motion of the object from retinal to world-coordinates
	- what are the invariants?
		- "invariant detection"

Plan: experiment is great - send Oliver details in September when the project starts to solidify so we can talk about labeling/organizing the data in a way that is meaningful to him
