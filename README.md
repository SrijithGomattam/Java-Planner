# Java Weekly Planner


## Program Pitch
Stay organized and maximize productivity with WeekPlan. This app offers a streamlined interface to create, edit, 
and manage events and tasks for the week. Customize categories, save and load pre-existing weeks, and enjoy keyboard 
shortcuts for seamless navigation. Get a detailed view of each task, a weekly overview, and choose your preferred week
start day. Take control of your schedule with WeekPlan—download now!

## GUI Screenshots
![img.png](pngs/WelcomeScreen.png)
![img.png](PrePasswordWeekView.png)
![img_1.png](PasswordView.png)
![img.png](pngs/WeekView.png)
![img.png](pngs/CreateNewEvent.png)
![img_1.png](pngs/CreateNewTask.png)
![img_2.png](pngs/CreateNewWeek.png)
![img_1.png](pngs/MiniViewerEvent.png)
![img.png](pngs/MiniViewerTask.png)

## SOLID Principles
- S: we applied the Single Responsibility principle by having each window use its own controller, for example, 
the mini viewer controllers for events and tasks have their own classes. Each class controls its own mini viewer and stage,
so that they do not interrupt each other. For the new event and new task controllers, each class handles making only
its appropriate type of bullet, but are abstracted through an interface since they have similar functionality.

- O: Applied the Open/Closed principle through the use of abstraction. Abstracted events and tasks
to be classified as EventBullets and TaskBullets, respectively, which extend AbstractBullet. These then implement the
interface, Bullet. This means that we would not have to modify event or task in order to add more features. Because there are
multiple levels of abstraction, it is possible to implement other types of bullets in the future if we choose to do so.

- L: Applied the Liskov Substitution principle in many cases. Used different data structures involving Bullets 
which meant they could be an EventBullet or TaskBullet. In most cases, it is possible to replace a generic Bullet with an EventBullet
or TaskBullet without changing the way the code works.

- I: Applied the Interface Segregation principle when creating our controller interfaces. Each controller interface
has a specific level of functionality that only gets used when it needs to. There are many interfaces so that no classes
that implement an interface do not use its methods. This ensures differentiation between our controller classes and reduces
ambiguity.

- D: Applied the Dependency Inversion principle by abstracting code with interfaces in multiple places. In the model, the Bullet,
EventBullet and TaskBullet interfaces can be seen. In the controller, several interfaces were used to abstract
the different purposes for each controller. Both of these ensure that the high-level modules are not dependent on the low-level
modules

## Extending Program for Additional Features
It is possible to extend the program in the future to have the additional feature of themes, as per the use CSS files to color,
organize, and format our week view. Right now, there is a limited use of CSS files to set background images and since
these files are readily available, they can be expanded upon to include other properties like colors for the different elements
in our scenes.

## Image Credits
https://wallpaperaccess.com/minimalist-space
https://giphy.com/stickers/kurzgesagt-loop-kurzgesagt-in-a-nutshell-inanutshell-y8tLxq4uGuIWFFIOQW
