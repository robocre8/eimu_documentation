## Easy IMU (EIMU) User Documentation
Anyone using an Inertial Measurement Unit (IMU) generally wants it to spit out filtered orientation readings and integrate them into their preferred project(s) without the unnecessary stress and headaches of the mathematics and computational algorithms behind it. This is what the **`Easy IMU`** does.
</br></br>
The **`Easy IMU`** is an easy-to-use Advanced Inertial Measurement Unit (IMU) built on and based on the popular **MPU9250** IMU. It consists of the `MPU9250 IMU`, an `ATmega328 microcontroller computational system`, and a `GUI Application` to ease the calibration, reference frame setup (e.g. NED, ENU, or NWU), and filter setup process for the **MPU9250** IMU (it uses the Madgwick filter).
</br></br>
It also provides a `USB serial and I2C communication interface` with `ROS2`, `Arduino`, `Python`, and `Cpp` libraries for easy interfacing with one's preferred project.
> Short test video

![sic_ros2_test_new](https://github.com/user-attachments/assets/b4c69494-5065-4943-b6ae-208dee447f3c)

> [!NOTE]
> The name of the Easy IMU circuit board which consists of the MPU9250 and an ATmega328 microcontroller computational system is **`MPU9250 EIMU Module`** or the **`Easy IMU Module`**
> 
> It can easily be used by hobbyists, students, learners, researchers, engineers, etc.

> **Picture explaining the module (MPU9250 + COMPUTATIONAL SYSTEM)**

![eimu_summary_pic](https://github.com/user-attachments/assets/c9cb1634-0215-4ad5-a767-07b007e178bd)

![Screenshot from 2024-10-02 17-27-00](https://github.com/user-attachments/assets/8b9f2b7a-23b3-491e-bc0d-f49c7eda4336)

#

#### COMMON MPU9250 PROBLEM
The **MPU9250** IMU is a widely used Inertial Measurement Unit (IMU) among hobbyists, researchers, engineers, and developers in robotics, drones, virtual reality, augmented reality, and wearable technology. It is renowned for its accuracy, reliability, and affordability, making it a popular choice for projects requiring motion tracking and orientation sensing.
</br></br>
While there are libraries available to assist in using the **MPU9250** IMU, common issues encountered with it typically revolve around calibration (especially of the magnetometer), setup, noise filtering, choosing reference frame (e.g. `NED`, `ENU`, or `NWU` reference frame), and seamless integration into preferred projects.
</br></br>
Calibrating its sensors, especially the magnetometer, is usually an issue and can be frustrating as wrong calibration will result in faulty orientation readings. Also, implementing filtering algorithms like the popular Kalman or Madgwick filter to get less noisy filtered orientation readings can be another problem, not to mention choosing a reference frame (e.g. `NED`, `ENU`, or `NWU` reference frame) and trying to add the whole code into your preferred project (which is usually bulky).
</br></br>
Ultimately, anyone using an IMU desires filtered orientation readings, in a preferred reference frame (e.g. NED, ENU, or NWU) without the unnecessary stress and headaches of calibration and noise filtering as well as frame transformation when integrating it into their projects.

#

The **`Easy IMU`** easily solves and abstracts all these problems so you can focus on using the filtered readings in your projects.
> [!IMPORTANT]
> In summary, the **`Easy IMU`** provides the following:
> * Easy `calibration` via its GUI application - [eimu_setup_application](https://github.com/samuko-things-company/eimu_setup_application).
> * Easy `Madgwick filter` gain setup (and visualization) via its GUI application.
> * Easy quick reference frame setup (`NED`, `ENU`, `NWU`) via its GUI application.
> * Easy integration with `ROS2` (microcomputer or PC) projects with its ROS2 package - [eimu_ros2](https://github.com/samuko-things-company/eimu_ros2).
> * Easy integration with `Arduino` projects with its I2C library - [eimu_arduino](https://github.com/samuko-things-company/eimu_arduino).
> * Easy integration with a microcomputer-based (`Python` or `Cpp`) project with its [eimu_python](https://github.com/samuko-things-company/eimu_python) and [eimu_cpp](https://github.com/samuko-things-company/eimu_cpp) library.

#

#### THE Easy IMU Module (i.e MPU9250 EIMU MODULE) SPECIFICATION
> **Picture showing part labels**

![eimu_conn_overview](https://github.com/user-attachments/assets/858339da-8f88-4be8-8c8d-1c3288cb5022)

* Supply Voltage - 5V (typical)
* Low Power Consumption.
* Communication Interface - `USB Serial` and `I2C`
* It can be configured to use any of the `NED`, `ENU`, or `NWU` Reference Frame.
* Easily integrates with `ROS2` and `Arduino` (as well as `Python` and `Cpp`) projects.
* `Orientation` readings (Roll, Pitch, and Yaw) are in **radians**. It also outputs quaternion orientation readings.
* `Angular rate` readings are in **rad/sec**.
* `Acceleration` readings are in **m/s2**.
> [!NOTE]
> Only orientation readings are filtered, not the rate or acceleration readings but it also provides the orientation, angular rates, and acceleration variances which can be used in more advanced filter algorithms as covariance matrices.

> **Picture showing different reference frame configurations of the Easy IMU**

![eimu_ref_frame](https://github.com/user-attachments/assets/748ba1a4-6347-455c-98b7-58569c317fef)

#

#### Easy IMU APPLICATIONS
* Robotics (Arduino, ROS2, Python, and C++)
* Precise Motion tracking
* Drones
* GPS Guided systems
* Heading reference system

#

#### Easy IMU USAGE GUIDE SUMMARY
* Get/Purchase the **Easy IMU Module** (i.e. **MPU9250 EIMU Module**)
> [!NOTE]
> The **Easy IMU Module** (i.e. **MPU9250 EIMU Module**) is available on **`Pre-order`**.
> Please reach out to me via [LinkedIn](www.linkedin.com/in/samuel-obiagba-a61316196) or through my [Contact](https://samukothings.com/contact/) page.
* Download and run the **Setup Application** to calibrate the **`Easy IMU Module`** and set up the Madgwick filter parameter and gain. You will be able to visualize the final result - [tutorial]()
* Use it in your **ROS2** project - [tutorial]()
* Use it in your **Arduino** project - [tutorial]()
* Use it in your **Python** project - [tutorial]()
* Use it in your **Cpp** project - [tutorial]()

#

#### LIBRARIES THAT MADE THE Easy IMU PROJECT POSSIBLE
Check out these Github repos of libraries that went a long way in developing the `Easy IMU ATmega328 microcontroller computational system`. You can use them in your projects also (Ensure to star them).
* [imu_madgwick_filter]() - Madgwick filter Arduino library based on (and adapted from) the [imu_tool]() ROS2 Madgwick code by CCNYRoboticsLab, adapted by samuko-things.
* [arduino_matrix_vector_lab]() - Arduino library that helps you perform vector and matrix operations and transformation with arrays, developed by samuko-things.
* [invensense_imu]() - Arduino and CMake library for communicating with the InvenSense MPU-6500, MPU-9250, and MPU-9255 nine-axis IMUs, by Bolder Flight.
* [Serial_comm_pyserial_and_arduino]() - a backend-API-style serial communication code between Pyserial and Arduino that can be adapted to any project, developed by samuko-things.
