## Changelog for package rmf_battery

0.1.2 (2021-10-27)
------------------
* Using eigen3_cmake_module to fix RHEL build [#16](https://github.com/open-rmf/rmf_battery/commit/7e1a4e73135963df2542e40913aa50ae79266fb3)

0.1.1 (2021-09-08)
------------------
* Making package ament agnostic

0.1.0 (2021-06-02)
------------------
* Provides core `rmf_battery::agv` utilities
    * `BatterySystem` - Describe battery properties of the vehicle
    * `MechanicalSystem` - Describe mechanical properties of the vehicle
    * `PowerSystem` - Describe a power system on-board the vehicle
* Provides `rmf_battery::agv::SimpleMotionPowerSink`
    * Sample implementation of `rmf_battery::MotionPowerSink`
    * Compute change in battery charge due to locomotion over a specified `rmf_traffic::Trajectory`
* Provides `rmf_traffic::agv::SimpleDevicePowerSink`
    * Sample implementation of `rmf_battery::DevicePowerSink`
    * Compute change in battery charge due to power systems over a specified duration
* Contributors: Yadunund
