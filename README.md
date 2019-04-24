Audio Manager
-----------------

Audio Manager is, as the name implies, an audio manager with support for 3D spatialised audio for the Unity Engine.
This is based on a Tutorial created by Brackeys, available here:
https://www.youtube.com/watch?v=6OT43pvUyfY


How to use:
-----------

1: Create an empty Gameobject and attach the AudioManager Component to it.

2: Insert any audio files you wish to play into the AudioManager Component.

3: Modify the array entries to your liking.

4: Play the sounds via Play("Soundname", gameObject), or PlayOneShot("Soundname", gameObject).



Sound Parameters:
--------------

Name (String): An identifier for the audio clip.

Clip (AudioClip): The Audio Clip to play.

Volume (Float): Linear Volume of the clip, from 0-1. 1 is Full Volume.

Volume Variance (Float): Allows for variance in the volume when the clip is played, from 0-1.

Pitch (Float): The Pitch of the Audio clip, from 0.1 - 3. 1 is normal Pitch.

Pitch Variance (Float): Allows for variance in the pitch of the clip when played, from 0-1.

Mixer Group (AudioMixerGroup): The Mixer group to use for the clip (music, sound effects, etc)

Loop (Bool): Wether or not to loop the Audio Clip.

Spatialize (Bool): Wether or not to spatialize the audio. If you are using an emitter, 
make sure this is checked.

Min Distance (Float): The Minimum distance from the emitter the audo clip can be heard at full volume.

Max Distance (Float): The Maximum Distance from the emitter that the audio clip can be heard.
This uses a Linear Falloff.


Script Functions:
-----------------


Play(string soundname, GameObject emitter);

PlayOneShot(string soundname, GameObject emitter);

These both create an audiosource at the specified emitter object (if there isn't one already),
sets the parameters of the audiosource form the parameters in the Array, then plays the audio clip.

As these are simply extensions of the standard Unity Audiosource.Play() and Audiosource.PlayOneShot() functions,
the same pros and cons for each function apply. In general, use Play() for Music and looping sound effects, and PlayOneShot() 
for Short sound effects that do not loop.

For More information on the Play() and PlayOneShot() functions, please refer to the Unity Documentation pages on these functions:

https://docs.unity3d.com/ScriptReference/AudioSource.Play.html

https://docs.unity3d.com/ScriptReference/AudioSource.PlayOneShot.html


Special Thanks
---------------
Brackeys, for the original code

SAE Institute, For getting me to start coding in the first place




