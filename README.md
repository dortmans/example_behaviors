# example_behaviors
This repo contains [FlexBE](FLEXBE.md) example states and behaviors.

Installation:
```
roscd && cd ../src
git clone https://github.com/team-vigir/flexbe_behavior_engine.git
git clone https://github.com/FlexBE/flexbe_app.git
cd flexbe_behavior_engine
git fetch
git checkout feature/flexbe_app
cd ..
git clone https://github.com/dortmans/example_behaviors.git
roscd && cd ..
catkin_make
```
Use the operator console to edit, run and monitor a behavior:
```
roslaunch flexbe_app flexbe_full.launch
```

Or run a behavior standalone:
```
roslaunch example_flexbe_behaviors behavior.launch behavior:="Example Behavior"
```
