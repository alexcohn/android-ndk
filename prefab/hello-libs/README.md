hello-libs
=========
hello-libs is a sample that shows you how to manage prefab C/C++ libraries with Android Studio.

Introduction
------------
This sample uses the [Android Studio CMake plugin](http://tools.android.com/tech-docs/external-c-builds) with external library support. It demos how to:

* include a pre-built static library (gmath) in your app
* include a pre-built shared library (gperf) in your app

Description
-----------
The sample includes 3 modules:
*    app -- imports a shared library (libgperf.so) and a static library (libgmath.a) from a prefab AAR
*    gen-libs -- contains the source code and CMake build script for the gmath and gperf example libraries. The resulting binaries are prefabbed into the normal output AAR.

The main goal of the sample is to demo how to use 3rd party libs, it is not to demonstrate lib package generation. Toward that goal, the pre-built AAR is included in the `distribution` folder.

When importing libraries into your app, include the following in your app's `CMakeLists.txt` file (in the following order): 

*    import libraries (using `find_package(external REQUIRED CONFIG)`)
*    attach them to your target import libraries (using `target_link_libraries(app external::gperf)`)

Pre-requisites
--------------
- Android Studio 4.2 with [NDK](https://developer.android.com/ndk/).

Getting Started
---------------
1. [Download Android Studio](http://developer.android.com/sdk/index.html)
1. Launch Android Studio.
1. Open the sample directory.
1. Open *File/Project Structure...*
  - Click *Download* or *Select NDK location*.
1. Click *Tools/Android/Sync Project with Gradle Files*.
1. Click *Run/Run*.


Screenshots
-----------
![screenshot](screenshot.png)

Support
-------
If you've found an error in these samples, please [file an issue](https://github.com/googlesamples/android-ndk/issues/new).

Patches are encouraged, and may be submitted by [forking this project](https://github.com/googlesamples/android-ndk/fork) and
submitting a pull request through GitHub. Please see [CONTRIBUTING.md](../CONTRIBUTING.md) for more details.

- [Stack Overflow](http://stackoverflow.com/questions/tagged/android-ndk)
- [Android Tools Feedbacks](http://tools.android.com/feedback)

License
-------
Copyright 2015 Google, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.

 
