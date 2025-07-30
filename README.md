# Interbotix ALOHA

Project Websites:

* [ALOHA](https://tonyzhaozh.github.io/aloha/)
* [Mobile ALOHA](https://mobile-aloha.github.io/)

Trossen Robotics Documentation: https://docs.trossenrobotics.com/aloha_docs/

This codebase is forked from the [Mobile ALOHA repo](https://github.com/MarkFzp/mobile-aloha), and contains teleoperation and dataset collection and evaluation tools for the Stationary and Mobile ALOHA kits available from Trossen Robotics.

To get started with your ALOHA kit, follow the [ALOHA Getting Started Documentation](https://docs.trossenrobotics.com/aloha_docs/getting_started.html).

To train imitation learning algorithms, you would also need to install:

* [ACT for Stationary ALOHA](https://github.com/Interbotix/act).
* [ACT++ for Mobile ALOHA](https://github.com/Interbotix/act-plus-plus)

# Structure
- [``aloha``](./aloha/): Python package providing useful classes and constants for teleoperation and dataset collection.
- [``config``](./config/): a config for each robot, designating the port they should bind to, more details in quick start guide.
- [``launch``](./launch): a ROS 2 launch file for all cameras and manipulators.
- [``scripts``](./scripts/): Python scripts for teleop and data collection


# Modifications

`real_env.py` now has some added functionality like `make_real_env_and_spin` and `step_no_reqs` in `RealEnv`. Generally fixes some bugs where the interbotix node wouldn't spin sometimes. Also added `spinup` and `shutdown` methods to `RealEnv` to manage the interbotix node.