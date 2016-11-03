---
layout: post
title: "Singularity Drive"
image: images/singularity-drive-1.jpg
tags:
  - Robots
  - 3D Printing
  - Remote Control
---
This post is copied from my old website.
{: .notice}

## Project Goal
The goal of this project was to create a drive mechanism capable of forward, reverse, and rotation without changing the speed or direction of the drive motor. This is accomplished by driving a hemisphere of rubber and controlling the angle at which the rubber contacts the ground. This essentially changes the size  and direction of the 'wheel' contacting the ground. I was inspired by [this article](http://spectrum.ieee.org/automaton/robotics/diy/youve-never-seen-a-drive-system-like-this-before), but I wanted to try and make a larger and more stable version. The drive mechanism in the video suffers from having coupled steering mechanisms, as well as a platform which shifts in orientation. Working in conjunction with Ian Daniher, I wanted to see if we could do better.

## Components

| Category | Model/Type |
| -------- | ---- |
| Chassis| ABS plastic|
| Motor | Eflite Park 400 Brushless Outrunner |
| Servos | HiTech HS-5685MH |
| Receiver | Spektrum AR8000 |
| Battery | 1800 mAh LiPo |

## Result

The platform I have created is functional, but far from perfect. It is as stable laterally as I had hoped and it is extremely maneuverable. However, that maneuverability comes at a price; it is very difficult of control this platform at very slow speeds or to hold stationary without slowing the motor.

![image-center](/images/singularity-drive-2.jpg){: .align-center}

![image-center](/images/singularity-drive-3.jpg){: .align-center}

![image-center](/images/singularity-drive-4.jpg){: .align-center}

![image-center](/images/singularity-drive-5.jpg){: .align-center}

![image-center](/images/singularity-drive-6.jpg){: .align-center}

![image-center](/images/singularity-drive-7.jpg){: .align-center}

<iframe width="560" height="315" src="https://www.youtube.com/embed/nIEBChw5x8Q" frameborder="0" allowfullscreen></iframe>

There are two main issues in this current design: the rubber wheel is not perfectly centered about it's axis and steering is not completely symmetrical. The first issue does not cause major issues at low speeds, but after half throttle the entire assembly begins shaking destructively. It could be fixed by printing the half sphere wheel as part of the assembly. This would also allow for the manipulation of the shape of the wheel for different driving characteristics.

The second problem is caused by geometry of the steering servo linkage. Due to the position of the steering servo, the polygon formed between the four pivot points in the steering system is not a parallelogram. If the steering servo's connection to the chassis can be redesigned such that a parallelogram is formed, the steering behavior will be theoretically symmetrical.

## Responses to questions posted on Hackaday.com

[My Post on Hackaday](#http://hackaday.com/2011/07/28/3d-printed-singularity-drive-platform/){: .btn .btn_info}

* Gyroscopic balancing would be amazing and if I work out a few kinks in this design, I would love to see what I can do in that direction

* As far as adding two more drives, I am fairly sure that I would be able to have full range of motion with only two drive wheels, and my control system would be a lot simpler than if I had three. With traditional omniwheels, at least three are needed because they can only drive in one direction on their own. This drive mechanism can actively drive in all directions on a 2d plane.

* I am starting to feel that the ball may be centered and it is just deforming under high speeds. I am not sure. Either way, I will be looking into new methods of making the drive hemisphere.

* This platform does have the complete potential to drive in a perfectly straight line and be completely maneuverable in small spaces. However, this would be greatly aided by a control loop of some form. Right now it is fairly drivable because I have tuned the servo limits and added exponential to my control. However, I need to know how it will react under different condition and drive it accordingly; ideally, a smart control loop would fill in that gap between what I want it to do and making it do it smoothly.

* I designed this to be driven with the regular wheels in front, but for some reason it was easier to control driving in the other direction.

* This platform has plenty of power to handle a 1.2kg load, if not much more. I feel like it would actually handle better. The biggest issue is that the rubber hemisphere will be pushed deeper into the surface it is riding on. On a hard floor, I think it would drive better, but on a rug I think it would put a tremendous load on the motor.

* The original inspiration for this project was to take the IEEE drive mechanism and see how it would work scaled up. I scaled up the drive mechanism, but the chassis itself is still very small. Judging by how it drives now, I think it would drive better if the body were significantly larger.

* The platform is ABS plastic and was printed using an extrusion method.

* I completely plan on sharing my CAD files for this project and all my other projects. However, I need to find a reasonably robust (and hopefully free) method of hosting those files. I know there are tons of services out there; I just need to pick one.
