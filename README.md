# C++ samples

This repository contains  **C++** code samples for **Zivid**.

[![Build Status][ci-badge]][ci-url]

## Samples list

There are two main categories of samples: **Camera** and **Applications**. The samples in the **Camera** category focus only on how to use the camera. The samples in the **Applications** category use the output generated by the camera, such as the 3D point cloud, a 2D image or other data from the camera. These samples shows how the data from the camera can be used.

- **Camera**
  - **Basic** ([quick tutorial][QuickCaptureTutorial-url] / [complete tutorial][CompleteCaptureTutorial-url])
    - [**Capture**][Capture-url] - Capture point clouds, with color, from the Zivid camera.
    - [**Capture2D**][Capture2D-url] - Capture 2D images from the Zivid camera.
    - [**CaptureAssistant**][CaptureAssistant-url] - Use Capture Assistant to capture point clouds, with color, from the Zivid camera.
    - [**CaptureFromFileCamera**][CaptureFromFileCamera-url] - Capture point clouds, with color, from the Zivid file camera.
    - [**CaptureWithSettingsFromYML**][CaptureWithSettingsFromYML-url] - Capture point clouds, with color, from the Zivid camera, with settings from YML file.
    - [**CaptureHDR**][CaptureHDR-url] - Capture HDR point clouds, with color, from the Zivid camera.
    - [**CaptureHDRCompleteSettings**][CaptureHDRCompleteSettings-url] - Capture point clouds, with color, from the Zivid camera with fully configured settings.
  - **Advanced**
    - [**CaptureHDRLoop**][CaptureHDRLoop-url] - Cover the same dynamic range in a scene with different acquisition settings to optimize for quality, speed, or to find a compromise.
  - **InfoUtilOther**
    - [**CameraUserData**][CameraUserData-url] - Store user data on the Zivid camera.
    - [**GetCameraIntrinsics**][GetCameraIntrinsics-url] - Read intrinsic parameters from the Zivid camera.
    - [**FirmwareUpdater**][FirmwareUpdater-url] - Update firmware on the Zivid camera.
    - [**ZividBenchmark**][ZividBenchmark-url] - Benchmark the Zivid camera.

- **Applications**
  - **Basic**
    - **Visualization**
      - [**CaptureFromFileCameraVis3D**][CaptureFromFileCameraVis3D-url] - Capture point clouds, with color, from the virtual Zivid camera, and visualize it.
      - [**CaptureVis3D**][CaptureVis3D-url] - Capture point clouds, with color, from the Zivid camera, and visualize it.
      - [**CaptureWritePCLVis3D**][CaptureWritePCLVis3D-url] - Capture point clouds, with color, from the Zivid camera, save it to PCD file format, and visualize it.
        - **Dependencies:**
          - [Point Cloud Library](https://pointcloudlibrary.github.io) version 1.2 or newer
      - [**ReadPCLVis3D**][ReadPCLVis3D-url] - Read point cloud from PCL file and visualize it.
        - **Dependencies:**
          - [Point Cloud Library](https://pointcloudlibrary.github.io) version 1.2 or newer
    - **FileFormats**
      - [**ReadIterateZDF**][ReadIterateZDF-url] - Read point cloud data from a ZDF file, iterate through it, and extract individual points.
  - **Advanced**
    - [**HandEyeCalibration**][HandEyeCalibration-url]
      - [**HandEyeCalibration**][HandEyeCalibrationSample-url] - Perform Hand-Eye calibration
      - [**UtilizeEyeInHandCalibration**][UtilizeEyeInHandCalibration-url] - Transform single data point or entire point cloud from camera frame to robot base frame using Eye-in-Hand calibration matrix.
        - **Dependencies:**
          - [Eigen](http://eigen.tuxfamily.org/) version 3.3.7 or newer
          - [OpenCV](https://opencv.org/) version 4.1.0 or newer
      - [**PoseConversions**][PoseConversions-url] - Convert to/from Transformation Matrix (Rotation Matrix + Translation Vector)
        - **Dependencies:**
          - [Eigen](http://eigen.tuxfamily.org/) version 3.3.7 or newer
          - [OpenCV](https://opencv.org/) version 4.1.0 or newer
    - [**MultiCamera**][MultiCamera-url] ([tutorial][MultiCameraTutorial-url])
      - [**MultiCameraCalibration**][MultiCameraCalibration-url] and [**MultiCameraCalibrationFromFile**][MultiCameraCalibrationFromZDF-url] - Use captures of a calibration object to generate transformation matrices to a single coordinate frame. First sample captures from connected cameras, the second loads existing captures from .ZDF files.
      - [**StitchByTransformation**][StitchByTransformation-url] and [**StitchByTransformationFromFile**][StitchByTransformationFromZDF-url] - Use transformation matrices from Multi-Camera calibration to transform point clouds into single coordinate frame. First sample uses connected cameras, the second loads existing captures from .ZDF files.
    - [**Downsample**][Downsample-url] - Downsample point cloud from ZDF file.
    - [**CaptureUndistortRGB**][CaptureUndistortRGB-url] - Use camera intrinsics to undistort RGB image.
      - **Dependencies:**
        - [OpenCV](https://opencv.org/) version 4.1.0 or newer
    - [**CreateDepthMap**][CreateDepthMap-url] - Convert point cloud from ZDF file to OpenCV format, extract depth map and visualize it.
      - **Dependencies:**
        - [OpenCV](https://opencv.org/) version 4.1.0 or newer
    - [**MaskPointCloud**][MaskPointCloud-url] - Mask point cloud from ZDF file and convert to PCL format, extract depth map and visualize it.
      - **Dependencies:**
        - [OpenCV](https://opencv.org/) version 4.1.0 or newer
        - [Point Cloud Library](https://pointcloudlibrary.github.io/) version 1.2 or newer

## Instructions

1. [**Install Zivid Software**](https://zivid.atlassian.net/wiki/spaces/ZividKB/pages/59080712/Zivid+Software+Installation).
Note: The samples require Zivid SDK v2 (minor version 2.1 or newer).

2. [**Download Zivid Sample Data**](https://zivid.atlassian.net/wiki/spaces/ZividKB/pages/450363393/Sample+Data).

### Windows

Launch the Command Prompt by pressing *Win + R* keys on the keyboard, then type cmd and press Enter.

Navigate to a location where you want to clone the repository, then run to following command:

```bash
git clone https://github.com/zivid/zivid-cpp-samples
```

[comment]: <> (Choose a sample solution and configure it with CMake.)
[comment]: <> (Launch Visual Studio, open, build, and run the sample solution.)

Configure the sample solution with CMake, open it in Visual Studio, build it, run it. If you are uncertain about doing this, check out our [**tutorials for configuring and building C++ Samples**](https://zivid.atlassian.net/wiki/spaces/ZividKB/pages/427987).

#### Ubuntu

Open the Terminal by pressing *Ctrl + Alt + T* keys on the keyboard.

Navigate to a location where you want to clone the repository, then run to following commands:

```bash
git clone https://github.com/zivid/zivid-cpp-samples
cd zivid-cpp-samples
```

Build the project:

```bash
mkdir build
cd build
cmake <options, see below> ../source
make -j
```

Some of the samples depend on external libraries, in particular Eigen 3, OpenCV or PCL. If you don't want to install those, you can disable the samples depending on them by passing the following options, respectively, to `cmake`: `-DUSE_EIGEN3=OFF`, `-DUSE_OPENCV=OFF`, `-DUSE_PCL=OFF`.

If you do want to use them:

- **Eigen 3**: Set `-DEIGEN3_INCLUDE_DIR=<path>` where `<path>` is the root directory of your Eigen3 installation (the folder containing Eigen/Core, Eigen/Dense etc.)
- **PCL** and **OpenCV**: If a recent enough version is installed on your system, these should just work. If not, set `-DPCL_DIR=<path>` / `-DOpenCV_DIR=<path>` where `<path>` is the directory containing `PCLConfig.cmake` and `OpenCVConfig.cmake`, respectively.

The samples can now be run from the `build` directory, for instance like this:

```bash
./CaptureFromFileCameraVis3D
```

## Support

If you need assistance with using Zivid cameras, visit our [**Knowledge Base**](https://help.zivid.com/) or contact us at [customersuccess@zivid.com](mailto:customersuccess@zivid.com).

## Licence

Zivid Samples are distributed under the [BSD license](LICENSE).

## Development

To run continuous integration locally, use [Docker](https://www.docker.com). With Docker installed, run this command:

```bash
docker run -it -v <unixy-repo-path>:/host -w /host/continuous-integration/linux ubuntu:20.04
```

Where `<unixy-repo-path>` is the unixy path to the repo on your computer. On Linux, use `$PWD` for this. On Windows you need to translate the windowsy path to a unixy one (e.g. `/c/Users/alice/Documents/zivid-cpp-samples`).

Now run `./setup.sh` to install dependencies. Once setup has completed, you can run `./lint.sh && ./build.sh` repeatedly to check your code.

Tip: If your build hangs, try to increase the memory available to Docker.

[ci-badge]: https://img.shields.io/azure-devops/build/zivid-devops/79b793a0-a49a-463b-9c76-39b1e4947800/8
[ci-url]: https://dev.azure.com/zivid-devops/zivid-cpp-samples/_build/latest?definitionId=8&branchName=master
[QuickCaptureTutorial-url]: source/Camera/Basic/QuickCaptureTutorial.md
[CompleteCaptureTutorial-url]: source/Camera/Basic/CaptureTutorial.md
[Capture-url]: source/Camera/Basic/Capture/Capture.cpp
[Capture2D-url]: source/Camera/Basic/Capture2D/Capture2D.cpp
[CaptureAssistant-url]: source/Camera/Basic/CaptureAssistant/CaptureAssistant.cpp
[CaptureFromFileCamera-url]: source/Camera/Basic/CaptureFromFileCamera/CaptureFromFileCamera.cpp
[CaptureWithSettingsFromYML-url]: source/Camera/Basic/CaptureWithSettingsFromYML/CaptureWithSettingsFromYML.cpp
[CaptureHDR-url]: source/Camera/Basic/CaptureHDR/CaptureHDR.cpp
[CaptureHDRLoop-url]: source/Camera/Advanced/CaptureHDRLoop/CaptureHDRLoop.cpp
[CaptureHDRCompleteSettings-url]: source/Camera/Basic/CaptureHDRCompleteSettings/CaptureHDRCompleteSettings.cpp
[CameraUserData-url]: source/Camera/InfoUtilOther/CameraUserData/CameraUserData.cpp
[GetCameraIntrinsics-url]: source/Camera/InfoUtilOther/GetCameraIntrinsics/GetCameraIntrinsics.cpp
[FirmwareUpdater-url]: source/Camera/InfoUtilOther/FirmwareUpdater/FirmwareUpdater.cpp
[ZividBenchmark-url]: source/Camera/InfoUtilOther/ZividBenchmark/ZividBenchmark.cpp
[CaptureFromFileCameraVis3D-url]: source/Applications/Basic/Visualization/CaptureFromFileCameraVis3D/CaptureFromFileCameraVis3D.cpp
[CaptureVis3D-url]: source/Applications/Basic/Visualization/CaptureVis3D/CaptureVis3D.cpp
[CaptureWritePCLVis3D-url]: source/Applications/Basic/Visualization/CaptureWritePCLVis3D/CaptureWritePCLVis3D.cpp
[ReadPCLVis3D-url]: source/Applications/Basic/Visualization/ReadPCLVis3D/ReadPCLVis3D.cpp
[ReadIterateZDF-url]: source/Applications/Basic/FileFormats/ReadIterateZDF/ReadIterateZDF.cpp
[HandEyeCalibration-url]: source/Applications/Advanced/HandEyeCalibration
[HandEyeCalibrationSample-url]: source/Applications/Advanced/HandEyeCalibration/HandEyeCalibration/HandEyeCalibration.cpp
[UtilizeEyeInHandCalibration-url]: source/Applications/Advanced/HandEyeCalibration/UtilizeEyeInHandCalibration/UtilizeEyeInHandCalibration.cpp
[PoseConversions-url]: source/Applications/Advanced/HandEyeCalibration/PoseConversions/PoseConversions.cpp
[MultiCamera-url]: source/Applications/Advanced/MultiCamera
[MultiCameraTutorial-url]: source/Applications/Advanced/MultiCamera/MultiCameraTutorial.md
[MultiCameraCalibration-url]: source/Applications/Advanced/MultiCamera/MultiCameraCalibration/MultiCameraCalibration.cpp
[MultiCameraCalibrationFromZDF-url]: source/Applications/Advanced/MultiCamera/MultiCameraCalibrationFromZDF/MultiCameraCalibrationFromZDF.cpp
[StitchByTransformation-url]: source/Applications/Advanced/MultiCamera/StitchByTransformation/StitchByTransformation.cpp
[StitchByTransformationFromZDF-url]: source/Applications/Advanced/MultiCamera/StitchByTransformationFromZDF/StitchByTransformationFromZDF.cpp
[Downsample-url]: source/Applications/Advanced/Downsample/Downsample.cpp
[CaptureUndistortRGB-url]: source/Applications/Advanced/CaptureUndistortRGB/CaptureUndistortRGB.cpp
[CreateDepthMap-url]: source/Applications/Advanced/CreateDepthMap/CreateDepthMap.cpp
[MaskPointCloud-url]: source/Applications/Advanced/MaskPointCloud/MaskPointCloud.cpp
