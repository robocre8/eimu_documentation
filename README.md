## Easy IMU (EIMU) User Documentation
Anyone using an Inertial Measurement Unit (IMU) generally wants it to spit out filtered orientation readings and integrate them into their preferred project(s) without the unnecessary stress and headaches of the mathematics and computational algorithms behind it. This is what the **`Easy IMU`** does.
The **`Easy IMU`** is an easy-to-use Advanced Inertial Measurement Unit (IMU) built on and based on the popular **MPU9250** IMU. It consists of the `MPU9250 IMU`, an `ATmega328 microcontroller computational system`, and a `GUI Application` to ease the calibration, reference frame setup (e.g. NED, ENU, or NWU), and filter setup process for the **MPU9250** IMU (it uses the Madgwick filter). It also provides a `USB serial and I2C communication interface` with `ROS2`, `Arduino`, `Python`, and `Cpp` libraries for easy interfacing with one's preferred project. 

> Short test video

> [!NOTE]
> The name of the Easy IMU circuit board which consists of the MPU9250 and an ATmega328 microcontroller computational system is **`MPU9250 EIMU Module`** or the **`Easy IMU Module`**  
> It can easily be used by hobbyists, students, learners, researchers, etc.

> Picture explaining the module
#

#### COMMON MPU9250 PROBLEM
The **MPU9250** IMU is a widely used Inertial Measurement Unit (IMU) among hobbyists, researchers, engineers, and developers in robotics, drones, virtual reality, augmented reality, and wearable technology. It is renowned for its accuracy, reliability, and affordability, making it a popular choice for projects requiring motion tracking and orientation sensing.
</br></br>
While there are libraries available to assist in using the **MPU9250** IMU, common issues encountered with it typically revolve around calibration (especially of the magnetometer), setup, noise filtering, choosing reference frame (e.g. `NED`, `ENU`, or `NWU` reference frame), and seamless integration into preferred projects.
</br></br>
Calibrating its sensors, especially the magnetometer, is usually an issue and can be frustrating as wrong calibration will result in faulty orientation readings. Also, implementing filtering algorithms like the popular Kalman or Madgwick filter to get less noisy filtered orientation readings can be another problem, not to mention choosing a reference frame (e.g. `NED`, `ENU`, or `NWU` reference frame) and trying to add the whole code into your preferred project (which is usually bulky).
</br></br>
Ultimately, anyone using an IMU desires filtered orientation readings, in a preferred reference frame (e.g. NED, ENU, or NWU) without the unnecessary stress and headaches of calibration and noise filtering as well as frame transformation when integrating it into their projects.
</br></br>
The **`Easy IMU`** easily solves and abstracts all these problems so you can focus on using the filtered readings in your projects.
> [!IMPORTANT]
> In summary, the **`Easy IMU`** provides the following:
> * Easy quick reference frame setup (`NED`, `ENU`, `NWU`) via its GUI application - [eimu_setup_application]().
> * Easy `calibration` via its GUI application.
> * Easy `Madgwick filter` gain setup (and visualization) via its GUI application.
> * Easy integration with `ROS2` (microcomputer or PC) projects with its ROS2 package - [eimu_ros2]().
> * Easy integration with `Arduino` projects with its I2C library - [eimu_arduino]().
> * Easy integration with a microcomputer-based (`Python` or `Cpp`) project with its [eimu_python]() and [eimu_cpp]() library.
