# Session 2 - Virtual Filmmaking 

# <a name="Animations"></a>Animations 
![](images/animations.jpeg)

## Animations window 

To animate an object, open the "Animation" window (Window -> Animation -> Anmation). 
The select the GameObject you want to animate in the hierarchy window, now you should see this in the Animation Window: 
![](images/beginanimating.jpeg)
Click on "Create" this creates an *Animation Clip*.

Now you can start to animate your object either by hitting the record button:
![](images/record.gif)
or by manually adding the properties and keyframes: 
![](images/keyframe.gif)

See also:
- [Tutorial Animation in Unity](https://learn.unity.com/tutorial/working-with-animations-and-animation-curves#)

By default the Animation will loop, if you only want it to play once select the Animation Clip in the Project window and untick "Loop Time" in the Inspector. 
![](images/loop.jpeg)


> This method works best when you want to animate a single objects, like a spinning light. If you want to animate multiple objects together and the timing is importing, like for example a cinematic scene, or a transition scene then the "Timeline"-feature works better. 

## Animator window
![](images/Animator.jpeg)

*Note: we don't need the animator window for our course, but it's easier to understand the Unity Animation system if you know about it* 
The Animator selects when your animation clips will be played, for example when you want to create a Character that has different states (like walking, standing, running) and one animation clip for each state you would animate this in the Animator window. In this case you would need a little bit of coding, you can find a easy tutorial here: 
https://www.youtube.com/watch?v=tveRasxUabo

## Timeline
![](images/Timeline.jpeg)

The Timeline works best if you want to create a sequence of animations, like a transition scene or in our case a little movie sequence. 

To work with the Timeline open the Timeline window (Window -> Sequencing -> Timeline). 
Then create an empty GameObject (GameObject -> Create Empty) and name it "Director", this GameObject will control our movie sequence (and also our Cameras later). 

You can click on the settings wheel on the upper right side and choose whether you wanna work in seconds or in frames. 
![](images/timing.jpeg)

### Activating Objects in the Timeline
With the timeline you can easily activate and deactivate objects. Right-click on the left side of the Timeline window and select "Activation Track" then drag and drop the GameObject you want to activate and deactive in the selector field. 
![](images/activation.gif)
You can also change the time when and for how long your object should be active
![](images/changeactivation.gif)

### Animate Objects
You can also animate object in the same way as in the Animation window, but in the Timeline window you can directly see the timing for the whole scene, in case the animation should happen at a specific point in time. 
Right click on the left side again and select "Animation Track" (always make sure that the "Director" GameObject is selected in the hierarchy) then drag and drop the object you want to animate in the selector field and click on record. 
![](images/animationtimeline.gif)


# <a name="cinemachine"></a>Cinemachine 
With Cinemachine you can create complex camera behaviours without coding, like following a target, switching between different cameras, blending camera positions etc. 

## Virtual Cameras
Cinemachine works with so called *Virtual Cameras*. GameObjects that tell the MainCamera how to behave, so its always important, that you still have a normal camera (GameObject -> Camera) in your Scene. You can create Virtual Cameras by clicking on GameObject -> Cinemachine -> Virtual Camera this will add a GameObject called "CM vcam1" in your scene, this GameObject now controls the position of the Main Camera. 
![](images/virtualcamera.jpeg)

## Blending/ Switching between two virtual cameras
Lets create two virtual Cameras and switch between them in the Timeline: 
Create another Virtual Camera and position both cameras in different spots, so move the CM vcam1 & CM vcam2 GameObject in the Scene View.

> To get a preview of what the cameras see switch to Game view, i would suggest to split the window that you can see the scene view and the game view at the same time: ![](images/split.gif)

To Switch between the cameras in the preview you can just click on "Solo" in the inspector, when you select the virtual camera you want to preview. 
![](images/solo.gif)

The next step is to switch between the cameras in the Timeline, so select the *Director*-GameObject again and and drag and drop the Main Camera in the left field of the Timeline window and select "Add Cinemachine Track". Now you can drag and drop you virtual cameras in the Cinemachine Track and arrange them: 
![](images/timelinecinemachine.gif)

If you overlap the two virtual cameras Unity with blend between the two positions: 
![](images/blending.gif)

## Looking at a target 
Cinemachine cameras can also automatically look at a moving target: Select the Virtual Camera and drag and drop the moving GameObject in the "Look At" field. 
![](images/lookat.gif)

## Following a target
The same also works for following a target: Select the Virtual Camera and just drag and drop the target in the "Follow" field. 
![](images/following.gif)

## Dollytrack 

# <a name="cinemachine"></a>Post Processing 


# <a name="sounds"></a>Sound 

To add sound to a scene create a new Audio Source: GameObject -> Audio -> Audio Source. 

Then drag and drop your soundfile. 

- [Tutorial: Sound Component in Unity](https://learn.unity.com/tutorial/working-with-audio-components-2019-3)

Supported file formats: 
- AIFF 
- WAV 
- MP3
- Ogg 

Places to get free sounds: 
- [freesounds.org](https://freesound.org/people/Nox_Sound/): Different licenses
- [OpenGameArt](https://opengameart.org/art-search-advanced?field_art_type_tid%5B%5D=13)
- [Soundcloud](https://soundcloud.com/)





