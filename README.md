# dlb_mp4base

The Dolby MP4 streaming muxer (dlb_mp4base) is a software implementation of a muxer of fragmented or unfragmented ISO base media file format (mp4). It supports muxing of Dolby Digital (AC-3), Dolby Digital Plus (E-AC-3), and Dolby AC-4 audio formats as well as Dolby Vision.

## Getting Started

These instructions will help you get a copy of the project up and running on your local machine for development and testing purposes. 

### Folder Structure

The "dlb_mp4base" folder consists of:

- README.md         This file.
- doc/              Doxygen documentation of the dlb_mp4base.
- frontend/         MP4Muxer frontend with corresponding EMA interface as source code.
- include/          Necessary header files of the dlb_mp4base library.
- make/             Makefiles and Visual Studio projects/solutions for building the Dolby MP4 multiplexer library with frontends and test harnesses.
- src/              Contains the MP4 multiplexer source code.
- test/             Test harnesses for unit and developer system tests including test signals.

### Prerequisites

For Windows platform development, msbuild must be installed: https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild?view=vs-2022

### Building instructions

#### Using the msbuild (on Windows)

    Install msbuild:
    https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild?view=vs-2022

    From a cmd execute (depending on your machine architecture):
    - for windows_amd64: "msbuild make\mp4muxer\windows_amd64\mp4muxer_2022.vcxproj /p:Configuration=Release /p:Platform=x64 /t:Rebuild"
    - for windows_x86: "msbuild make\mp4muxer\windows_x86\mp4muxer_2022.vcxproj /p:Configuration=Release /p:Platform=x64 /t:Rebuild"

#### Using the makefiles (on Linux and MacOS)

    After cloning the dlb_mp4base repository to your local machine, go to the appropriate directory, depending on your machine OS and architecture, such as:
    "cd dlb_mp4base/make/mp4muxer<architecture>"

    Then build one of the following make targets:
    "make mp4muxer_release"
    "make mp4muxer_debug"

## Release Notes

See the [Release Notes](ReleaseNotes.md) file for details

## License

This project is licensed under the BSD-3 License - see the [LICENSE](LICENSE) file for details
