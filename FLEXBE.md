# FlexBE - the flexible behavior engine

[FlexBE](http://philserver.bplaced.net/fbe/) is a powerful and user-friendly high-level behavior engine for use in robots running the Robot Operating System (ROS). FlexBE helps you to create complex robot behaviors without the need for manually coding them.

Behaviors are specified using hierarchical state machines. They can easily be composed via the provided drag&drop editor.

States can be used for e.g. checking a condition, doing a calculation, interacting with an operator, sending a message or executing an action.

A state(machine) has one or more outcomes. Based on the outcome the next state(machine) is entered.

A number of basic states are provided. Additional, custom states can be created manually in Python.

Behaviors can be run autonomously on a robot. They can also be monitored, started, paused and stopped by a human operator via an operator console.

## Installation

Install FlexBE Behavior Engine:
```
roscd && cd ../src
git clone https://github.com/team-vigir/flexbe_behavior_engine.git
roscd && cd ..
catkin_make
```

Install FlexBE App (replaces deprecated Chrome app):
```
roscd && cd ../src
git clone https://github.com/FlexBE/flexbe_app.git
cd flexbe_behavior_engine
git fetch
git checkout feature/flexbe_app
roscd && cd ..
catkin_make
```

Create your own FlexBE repo
```
roscd && cd ../src
rosrun flexbe_widget create_repo <YOUR_PROJECT_NAME>
roscd && cd ..
catkin_make
```

## Usage

To run the FlexBE App alone for developing behaviors, but not executing them:
```
rosrun flexbe_app run_app --offline
```

To run both on_board behavior engine and FlexBE's operator control station app:
```
roslaunch flexbe_app flexbe_full.launch
```
See the [FlexBE tutorials](http://wiki.ros.org/flexbe/Tutorials) to learn how to use the operator control station.

You can also [run a behavior standalone on the robot](http://wiki.ros.org/flexbe/Tutorials/Running%20Behaviors%20Without%20Operator).

To start only the on_board behavior engine (on your robot)
```
roslaunch flexbe_onboard behavior_onboard.launch

```
On any computer connected to the ROS master, run the following command to start execution of the behavior named "Example Behavior":
```
rosrun flexbe_widget be_launcher -b 'Example Behavior'
```

## References

FlexBE homepage
http://philserver.bplaced.net/fbe/

FlexBE page on ROS wiki
http://wiki.ros.org/flexbe

FlexBE App
https://github.com/FlexBE/flexbe_app#flexbe-app

FlexBE Tutorials
http://wiki.ros.org/flexbe/Tutorials

Running Behaviors Without Operator
http://wiki.ros.org/flexbe/Tutorials/Running%20Behaviors%20Without%20Operator
