# Session 2 - Virtual Filmmaking 


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


# <a name="cinemachine"></a>Animations - Cinemachine 



