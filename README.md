# RustyPhysics
A simple rigid body physics solver with collisions. Primarily meant to be an entertaining project to learn the Rust language with. 
![BouncingCubes](https://github.com/user-attachments/assets/d494d97b-0058-4b89-96e3-dd5e93aecf0a)

## Features
* Custom gravity
* Easy to use RigidBody component, with convience methods for common operations such as adding torque, impulse, applying force at a specific position, etc.
* Kinematic and non kinematic bodies.
* Extendible Collider component for different collider types, using rust's powerful enums.
* Custom collision surfaces with tunable friction and bounce values.
* Colliders work alongside scaling, rotations, and translations done via bevy's transform component
* Contact resolution featuring contact pairs, normals, relative velocity, impulses, etc.
* Support for angular forces, calculating the inertia tensor for colliders, and angular velocity and drag.
* Included basic camera movement for scene navigation.


## How To Use 
Camera rotation, moving, and zooming is handled through the WASD keys, right clicking and dragging the mouse, and using the scroll wheel. Left click fires cubes from the screen with a given velocity. 

Unfortunately, the current UI functionality of Bevy and the rust community as a whole is very much in it's infancy and a custom UI solution would be quite a bit out of scope for this project. So currently, changing the settings for things needs to be changed in the actual code. Most things should be accessible from main.rs if you'd like to change them. There are ui options within bevy and bindings for immediate mode ui frameworks available if you'd like to extend it for whatever reason. 

## Known Issues
Torque and angular velocity is quite extreme and unstable so by default it's not enabled. If you want to enable it, change the function to either add the impulse at a specific position on contact, or explicitely add torque. Alternatively, the starting angular velocity and angular drag can be adjusted in the main.rs file. 

## How To Install 
I'm likely not putting this on crates.io, but the number of files is relatively small, so you should be able to just drag the files into a project, copy and paste the cargo.toml file, and then once it builds you should be good to go.

## Future Plans 
I likely won't be adding anything else to this project specifically as I typically enjoy larger projects more. I may dig deeper into a more serious physics solver/engine in the future once I'm more comfortable with rust, but if I do it will most likely not be an extension of this project. 
