# BriskUI
A hardware-accelerated, graphic user interface **C++** library with data-oriented design.

# Introduction
BriskUI is a modern C++ GUI library and provides GPU acceleration, which powered by Direct2D. It was inspired by [GacUI](https://github.com/vczh-libraries/GacUI).

This GUI library provides the following features:
- GPU acceleration.
- Develop your GUI using pure C++ and XML.
- XML resource supports. You can just describe the window by using XML.
- Rich control library. Container controls supports MVC and virtual list mode.
- Control template system. You can write your own widgets.
- MVVM and Data Binding.
  + You can define interfaces that required to build your own MVVM pattern in XML.
  + Using reflection you can set up data to control during runtime (Under construction).

# Compatibility
Now BriskUI is only support for Windows, but it was designed with cross-platform abilities by implementing the different abstract of window provider and renderer.

In the future, in order to support more platforms, we are considering adding other graphic API such as Vulkan or Mental.

The table below shows the details of the platform to which BriskUI applies:

| Graphic API | Supports Platform                                               |    Developer-side IDE    |
|:-----------:|:----------------------------------------------------------------|:------------------------:|
|   Direct2D  | Windows 7 or Windows Vista with Service Pack 2 (SP2) and later  |    Visual Studio 2019    |
|   Vulkan    | Windows/linux/Android                                           | N/A (Under construction) |
|   Mental    | Mac OS/iOS                                                      | N/A (Under construction) |

# Installation
BriskUI is a header-only C++ library. Just copy the `Import` folder to system or project's include path to simply use it.

BriskUI uses following software as its dependencies:
- [CMake](https://cmake.org/) as a general build tool
- (optional) [Googletest](https://github.com/google/googletest/) for unit and performance testing

# Architecture
```
.
├── Document <- Manual and API reference for user.
├── Import
├── Sample <- Example and Demos.
├── Source <- Here is code of BriskUI.
│   ├── Composition <- Layout and relation system for elements.
│   ├── Control <- GUI assemblies and template for customize it.
│   ├── CoreCpp <- Common coss-platform C++ construction.
│   ├── CoreGraphic <- Windows provider and renderer.
│   └── Element <- Basic picture primitives.
├── Test
└── Tools
```