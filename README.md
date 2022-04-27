# Archery-Unity
Archery Game built in Unity
Itch.io(link to play game):
https://db488.itch.io/archer-training
Controls for gameplay: Use the WASD/Arrow keys to move in any direction, Space to jump, and holding 
Shift will allow you to sprint. To fire an arrow, simply left click. 
Gameplay: You will be trying to find targets throughout the map. Once they are hit the target changes 
to a green color for a visual conformation that the target has been counted, but each target can only be 
hit once. There are a few Points of Interest including two blacksmith hubs, a campfire, and an archery 
range. These can be hints as to where you might find a few targets. 
World Mods:
1. Skybox: Added a nice morning sky skybox for a calming scene. 
2. First Person Controller: From an asset on the Asset Store, this is the “main player”. I changed 
different variables for speed, sounds, and jump force. 
3. Player Model: From the Asset Store, I used this as the player model as well as the three models 
on the archery range. This also came with the animations that I used. 
4. Sounds: Added sounds for the player walking, I’m not happy with the sounds but they do suffice.
5. Bow: This is from Open Game Art, and I mainly wanted this linked to the player to feel like you 
are holding something that would shoot arrows rather than arrows just appearing. 
6. Arrows: This is the main Prefab that you shoot (Using mechanics from Sprint 3 – Painting)
7. Stone Walls: This is used for the walls around the castle to keep the player from falling into a 
never-ending void. 
8. Wooden Fences: From the Asset Store, I used these around the archer range, and the doors on 
each side of the castle gates is just a fence that I turned on its side. 
9. Blacksmith Stations/Campfire: I used a few models to build these two sections from the Asset 
Store
10. Targets: I found the Models on Open Game Art, and used them as the main item that you shoot 
to keep the game “Family Friendly”
Code Mods:
1. Shoot Arrows with Right click: This is the main mechanic for the game. The arrow shoots out in 
the direction that you are facing with a pre-determined velocity. I did not directly use the script 
I created for Sprint 3, But I managed to pull pieces out, and instead of just creating an object, It 
creates the Arrow object and sends it in the correct direction with a velocity of 30;
2. Arrow Movement: This was by far the most difficult for me. I found a few tutorials online to 
walk me through the process, but the arrow has a different rotation based on how far it is from 
its original spawn location. Included a picture for an example: 
The arrow’s velocity vector changes as it rotates, using red arrows as a velocity vector, and black 
arrows as the projectile. 
3. Target Collision: The ArrowMovement Script checks that the arrow hits a target by checking the 
tag of the object it collides with. It then removes the tag from the target so it can not be used to 
count again. 
4. Color Changing: Each target just waits to be collided with an arrow. Once a Collison is detected, 
the target changes it material color to green, and this gives a nice hint of green while still being 
able to see the target details. (See ColorChanger Script)
5. Player Animations: Changes the Player animations depending on the key you are hitting; W, A,
D/ Up, Left, Right are a walking animation, S/Down are a Running backward animation, and 
Space is a jumping animation. 
6. Timer: Created a timer to count down from 2 minutes. Also found a way to format the time to 
fit the format: MM:SS.
7. Win/Loss: Win if all targets are hit before time runs out, and lost if time runs out before hitting 
the targets in time. Text is just displayed to say player lost/won.
8. Win/Loss Text: Text Changes for win or loss, and I figured out how to change the color of the 
text. I set it to Green for a win, and Red for a loss.
9. Arrow Orientation/Scale: Since my projectile is a prefab, there was no way to keep any rotation
or scale value, so I added a Vector3 to scale the arrow, and I added a rotation in the form of a 
Quaternion. 
10. Arrow Sound Effect: Plays a sound effect when an arrow is shot
