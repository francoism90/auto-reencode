# Auto-reencode
### Purpose
Mass convert lesser known formats such as asd, flv, and wmv to mp4 contained x264 files using ffmpeg.
* Retains file's original bitrates (audio/video) with limits by setting `BIT_VIDEO` and `BIT_AUDIO`.
* Functions recursively automatically.
* Use ramdisk (`/tmp`) to speedup encoding.
* Use Intel VAAPI hardware acceleration with software fallback.

### Usage
Call the script in the directory containing the target files to convert.

### Dependencies
* ffmpeg
* ffprobe
* bc
* intel-media-driver or libva-intel-driver
