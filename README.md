# rmf\_battery

![](https://github.com/open-rmf/rmf_battery/workflows/build/badge.svg)
![](https://github.com/open-rmf/rmf_battery/workflows/asan/badge.svg)
![](https://github.com/open-rmf/rmf_battery/workflows/tsan/badge.svg)
![](https://github.com/open-rmf/rmf_battery/workflows/style/badge.svg)
[![codecov](https://codecov.io/gh/open-rmf/rmf_battery/branch/main/graph/badge.svg)](https://codecov.io/gh/open-rmf/rmf_battery)

The `rmf_battery` package provides the following APIs to model a robot's battery life.
* [rmf_battery::agv::BatterySystem](https://docs.ros.org/en/rolling/p/rmf_battery/generated/classrmf__battery_1_1agv_1_1BatterySystem.html) which bundles parameters related to the battery onboard a robot.
* [rmf_battery::agv::MechanicalSystem](https://docs.ros.org/en/rolling/p/rmf_battery/generated/classrmf__battery_1_1agv_1_1MechanicalSystem.html) which bundles physical parameters of a robot.
* [rmf_battery::agv::PowerSystem](https://docs.ros.org/en/rolling/p/rmf_battery/generated/classrmf__battery_1_1agv_1_1PowerSystem.html) to model a component onboard a robot with a specified power rating.
* [rmf_battery::DevicePowerSink](https://docs.ros.org/en/rolling/p/rmf_battery/generated/classrmf__battery_1_1DevicePowerSink.html) is a pure abstract class to model the change in state-of-charge of the robot's battery from a power consuming device onboard the robot.
  * [rmf_battery::agv::SimpleDevicePowerSink](https://docs.ros.org/en/rolling/p/rmf_battery/generated/classrmf__battery_1_1agv_1_1SimpleDevicePowerSink.html) is a simple out-of-the-box implementation of `rmf_battery::DevicePowerSink`. This class wraps a `BatterySystem` and `PowerSystem` of a robot, and can estimate the change in state-of-charge of the battery from the `PowerSystem's` energy consumption over a duration.
* [rmf_battery::MotionPowerSink](https://docs.ros.org/en/rolling/p/rmf_battery/generated/classrmf__battery_1_1MotionPowerSink.html) to model the change in state-of-charge of the robot's battery resulting from the motion of the robot.
  * [rmf_battery::agv::SimpleMotionPowerSink](https://docs.ros.org/en/rolling/p/rmf_battery/generated/classrmf__battery_1_1agv_1_1SimpleMotionPowerSink.html) is a simple out-of-the-box implementation of `rmf_battery::MotionPowerSink`. This class wraps a `BatterySystem` and `MechanicalSystem` of a robot, and can estimate the change in state-of-charge of the battery from the energy consumed to accelerate/decelerate a robot as it moves along a trajectory.

Full API documentation is available [here](https://docs.ros.org/en/rolling/p/rmf_battery/)
