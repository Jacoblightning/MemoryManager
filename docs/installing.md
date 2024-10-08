---
tags:
  - UserDocs
---
# Installation
## CMake FetchContent (Recommended)
You can install directly from a CMake project by adding the following to your CMakeLists.txt
```cmake
include(FetchContent)

fetchcontent_declare(
        MemoryManage
        GIT_REPOSITORY https://github.com/Jacoblightning/MemoryManage
        GIT_TAG main
)
fetchcontent_makeavailable(
        MemoryManage
)

target_link_libraries(<Your executable> PRIVATE MemoryManage<Static or Dynamic>)
```
Remember to include the header:
```c++
#include <MemoryManage/MemoryManage.h>
```
## Installation from GitHub:
You can install from the latest GitHub commit by running the following in your shell:
```shell
git clone https://github.com/Jacoblightning/MemoryManage
cd MemoryManage
mkdir build
cd build
cmake ..
cmake --build .
sudo cmake --install .
```
## Binary from GitHub actions (x64 only)
You can use a binary from GitHub actions in two ways:

- Nightly.link (Recommended):
    - Use [this nightly.link url](https://nightly.link/Jacoblightning/MemoryManage/workflows/cmake-single-platform-release/main) and download the binary you want.
- Directly from actions (Requires a GitHub account):
    - Go to [the actions page for the publisher action](https://github.com/Jacoblightning/MemoryManage/actions/workflows/cmake-single-platform-release.yml)
    - Click on the latest action (the top one)
    - Scroll to actions and click the one you want.

## Binary from GitHub Releases (Not Recommended)
You can use a binary from GitHub releases, but I can't promise how up-to-date it will be.

1. Go to the [latest release page](https://github.com/Jacoblightning/MemoryManage/releases/latest)
2. Download the binary you want.

## What's next?
### Now that you have installed MemoryManage, head to the [QuickStart](quickstart.md) page