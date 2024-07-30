# cobot_arm_examples

This package provides basic ROS 2 examples to demonstrate fundamental concepts such as publishing/subscribing and parameter handling. Despite its name, it does not specifically deal with robot arms but serves as a general introduction to ROS 2 programming.

## Overview

The `cobot_arm_examples` package includes simple implementations of ROS 2 nodes in both Python and C++. It covers:

- Publishers and Subscribers
- Parameter declaration and handling

## Contents

### Python Examples

- `minimal_py_publisher.py`: A simple publisher node that sends "Hello World" messages.
- `minimal_py_subscriber.py`: A subscriber node that listens for messages on a topic.
- `minimal_py_parameters.py`: Demonstrates parameter declaration and handling in ROS 2.

Topics used in Python examples:
- `/topic`: Used by both the publisher and subscriber for string messages.

### C++ Examples

- `minimal_cpp_publisher.cpp`: A C++ implementation of a simple publisher node.
- `minimal_cpp_subscriber.cpp`: A C++ implementation of a subscriber node.
- `minimal_cpp_parameters.cpp`: Demonstrates parameter handling in C++.

Topics used in C++ examples:
- `/topic_cpp`: Used by both the publisher and subscriber for string messages.

## Prerequisites

- ROS 2 Iron

## Building the package

To build this package, clone this repository into your ROS 2 workspace and build it using colcon:

```bash
cd ~/ros2_ws/src
git clone https://github.com/automaticaddison/cobot_arm_examples.git
cd ..
colcon build --packages-select cobot_arm_examples
source ~/ros2_ws/install/setup.bash
```

## Running the examples

After building and sourcing the package, you can run the examples using the `ros2 run` command.

### Python Examples

Run the publisher:
```bash
ros2 run cobot_arm_examples minimal_py_publisher.py
```

In another terminal, run the subscriber:
```bash
ros2 run cobot_arm_examples minimal_py_subscriber.py
```

To run the parameters example:
```bash
ros2 run cobot_arm_examples minimal_py_parameters.py
```

### C++ Examples

Run the publisher:
```bash
ros2 run cobot_arm_examples minimal_cpp_publisher
```

In another terminal, run the subscriber:
```bash
ros2 run cobot_arm_examples minimal_cpp_subscriber
```

To run the parameters example:
```bash
ros2 run cobot_arm_examples minimal_cpp_parameters
```

## Modifying Parameters

You can modify parameters at runtime using the `ros2 param set` command. For example:

```bash
ros2 param set /minimal_parameter_cpp_node velocity_limit 3.14
```

## Dependencies

This package depends on the following ROS 2 packages:
- rclcpp
- rclpy
- rcl_interfaces
- std_msgs

These dependencies are listed in the `package.xml` file and will be automatically resolved when building with colcon.

## License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.

## Author

Addison Sears-Collins

