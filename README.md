# Practical Part
<img width="1383" height="835" alt="image" src="https://github.com/user-attachments/assets/2d95405f-f270-4897-afb5-6809eb62713e" />

For my practical component for Bubble Bobble, I tried to make a recreation of the game by making two 
seperate levels that had enemies and the player being able to shoot projectiles from a certain point. Since I made this within unreal
engine I seperated the blueprints up into different sections. I made logic for the actual AI movement, a bubble projectile blueprint,
and a score tracker. 

<img width="1919" height="640" alt="image" src="https://github.com/user-attachments/assets/90bc1cfd-b1b0-41a5-ad78-25aac2834f6e" />
<img width="1919" height="495" alt="image" src="https://github.com/user-attachments/assets/b0bd8abb-9f7f-49cb-a50f-7c0cd09aff20" />
<img width="1919" height="757" alt="image" src="https://github.com/user-attachments/assets/2b27668e-30bf-4d70-926d-076e0c700986" />

# Custom AI 
I was able to make the custom AI controller move with 2 different states. The AI controller was able to move toward the player location at all 
times and once it reached the player it went into a roaming state. This meant the enemy could track the player location and try to defeat the player.
The intention was to have the enemy AI not only move to the player but also have it shoot projectiles however I did not have enough time to implement this.
I also have a base enemy class that has a roam radius range as a variable and has the custom AI controller inside so that when I made the child class
enemy it would inherit all of these.
<img width="228" height="214" alt="image" src="https://github.com/user-attachments/assets/9fd595f9-a6ae-4c94-975a-3212068cd6ed" />

# Bubble Projectile 
Next I tried making the projectile for the player and added a projectile movement that would move the bullet at a certain speed. 
The bullet mesh would check to see if the player overlapped with the enemy and if so, it would destroy the enemy and the bullet actor itself. 
The third person character then now tries to shoot this projectile by pressing the IA_Shoot which is binded to the E key in input actions. When the player shoots
it should spawn the actor from a certain point in front of the follow camera. What I had intended to do was to make the player shoot the bullet out as it uses a homing 
feature that would move toward the enemy and destroy them, which is why I had set up logic for it to shoot out first before making the homing AI feature.
<img width="1919" height="848" alt="image" src="https://github.com/user-attachments/assets/f2d7697f-24e8-4fea-a4be-c74e73745995" />
<img width="1919" height="853" alt="image" src="https://github.com/user-attachments/assets/cd84cced-e45c-42f4-b426-ed0a5dc94f2d" />
<img width="1919" height="653" alt="image" src="https://github.com/user-attachments/assets/dc663e46-62ca-49c8-b564-2047e4c48423" />

# Custom Game Instance
Next, I tried to make a custom game instance that would not only change the player post process settings to show that the score is updated
but also update the text that would increase the score. I did not have time to implement a score system using the game instance but I was able to get the logic working
inside the widget blueprint. I had most of the logic set up but didn't have time to get the functionality from the game instance I was working on.
<img width="1919" height="967" alt="image" src="https://github.com/user-attachments/assets/2b880d46-4d5d-482f-9ad5-9432625f9358" />
<img width="1919" height="888" alt="image" src="https://github.com/user-attachments/assets/73850ec6-f44e-44fd-9cf9-4469b218ce26" />
<img width="1919" height="963" alt="image" src="https://github.com/user-attachments/assets/db29d16e-316c-48cb-b9c0-27b958b57f0b" />


# Interfaces & Level Switching
I used interfaces to attempt making the score increment. The interface also includes a wave increment which would have been based on the score
of the player. As a smaller part of the project, I wanted to add a portal that teleports the player into the next world on overlap. This was intended to spawn in
only when the score reaches a certain set value to introduce the player to the next level however, I did not have time to fully implement this feature.
<img width="1919" height="939" alt="image" src="https://github.com/user-attachments/assets/58ce85f0-8fca-4106-9f43-abe5c863c1cf" />
<img width="1919" height="923" alt="image" src="https://github.com/user-attachments/assets/9efcfd77-a2ab-4c46-a35d-0ce99443ef69" />



# Intended Project Design
My intended project was to have a player that can move around on platforms and shoot out the bubble projectile using the 
input action defined earlier within the project that uses a homing feature onto the enemies close to the player. The bubble would use 
the projectile movement component for easy movement rather than complex functionality. If the bubble hits the enemy, it would change 
the score of the player from 0 to a higher score using the game instance. The interface functions would be called using the game instance and run them 
inside the widget blueprints. Once all enemies are beaten it would spawn the portal actor which would teleport the player to the next level and the core loop
would repeat itself.
<img width="1919" height="1029" alt="image" src="https://github.com/user-attachments/assets/bd6ed7f5-4160-4771-a635-fa7e0dccb34c" />

