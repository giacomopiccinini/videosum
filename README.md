# videosum

This Rust script is to summarise important info on one or more video files. The usage is

```
videosum <TARGET>
```
where the target could either be a (nested) directory or a single file. In case it is a directory, all videos in the directory (thereby including those in subdirectories) are found and analysed. The output is of the form

```
Total videos: 11
Total Duration: 02:16:15
Unique FPS: {(4, 1), (30000, 1001)}
Unique Dimensions: {(480, 640), (360, 640)}
Equal Length: false
Unique Lengths: 3
Min Length: 13 s
Max Length: 907 s
```
Instead, if it is a single file, the output looks like
```
Total videos: 1
Total Duration: 00:00:13
FPS: 30000/1001
Dimensions: 360x640
```

## Installation

Before building the Rust environment with Cargo, make sure to install the appropriate FFMPEG-related dependencies. For example:

```
sudo apt install -y clang libavcodec-dev libavformat-dev libavutil-dev libavdevice-dev pkg-config
```
Add all the necessary dependencies until solved. After that, build the optimise executable with

```
cargo build --release
```