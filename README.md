Teensy 3.6 Project Template
===========================
 
Purpose
-------

An easy starting point for Teensy 3.6 projects on windows, with the only prerequisite being CMake.

This template is meant to be used along side the TeensyToolchain

This setup is not meant for Unix systems.

This setup is also meant only for the Teensy 3.6 although some tweaking can be done to be used
on other boards

Setup
-----

Download [TeensyToolchain](https://github.com/LeHuman/TeensyToolchain), unzip, and put it next to this template folder

Rename the downloaded folder from `TeensyToolchain-master` to `TeensyToolchain`

Alternatively, you can modify `TOOLCHAIN_OFFSET` inside `.vscode/settings.json` in order to tell the project where the toolchain is. The path must be relative.

Install the Latest Release version of [CMake](https://cmake.org/download/)

As of today, that would be version 3.18.4

Inside `.vscode/tasks.json`, modify the options for `TEENSY_USB_PORTNAME` for the ports that the project should use to connect to your teensy. ( Set to COM6 by default )

You can also modify the defaults for other tasks.

Using
-----

Put your code in `src/main.cpp`
Put any libraries you need in `libraries`

You can also modify the set values and compile flags inside `CmakeLists.txt` if you know what you are doing.
They are mostly under the function calls `add_compile_definitions` and `add_compile_options` towards the beginning.

### VSCode Tasks

* `Clean`: Clean up build files
* `Hard Clean`: Clean up entire CMake project
* `Build`: Compile project
* `Upload`: Upload compiled binary to teensy
* `Monitor`: Monitor teensy over a CLI, select the appropriate options when running

By default, `Ctrl + Shift + B` (Run Build Task) should run all of the above in order except for `Clean` and `Hard Clean`

Alternatively, install the [Tasks](https://marketplace.visualstudio.com/items?itemName=actboy168.tasks) extension so that tasks can instead be on the status bar. Already configured.
