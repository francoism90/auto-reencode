# Auto-reencode

## Purpose

Mass convert almost any video format to mp4 contained h264 files using two-pass video encoding.

### Features

* Tries to retain the original video/audio bitrate and copy inbuilt subtitles.
* To keep devices cool, [cpulimit](https://github.com/opsengine/cpulimit) is used to control the max. CPU usage.
* Functions recursively automatically.
* Use `tmpfs` (or any other preferred processing path) to speedup encoding and preventing SSD degradation.

### Dependencies

* `bash`
* `bc`
* `coreutils`
* `cpulimit`
* `ffmpeg` including `ffprobe`

Most Linux-distributions should offer these in the official repository.

## Usage

Call the script in the directory containing the target files:

```bash
cd /path/to/videos
auto-reencode
```

### Script Parameters

* `PATH_TEMP`: temporary path used for encoding and logging.
* `BIT_VIDEO`: sets the maxrate of the video.
* `BIT_AUDIO`: sets the maxrate of the audio.
* `CPU_LIMIT`: max. allowed CPU usage.
