# p5.js perlin flow field
the sketch's source code can also be seen and tested here: https://editor.p5js.org/NhatHoang37/sketches/1bloVBYPr

all the other details is in this blog post: https://peterbeshai.com/blog/2018-10-28-p5js-ccapture/

## Create video from ffmpeg

- **Frame rate**: 30 (see `fps` in the code)
- **Dimensions**: 540x540 (should match `createCanvas()` in the code)
- **Frame filenames**: `"%07d.png"` (incrementing numbers, 7 numbers long)
- **Quality (CRF)**: 17 (see [ffmpeg docs](https://trac.ffmpeg.org/wiki/Encode/H.264), but 17–28 is reasonable, 0 is lossless)

```
ffmpeg -r 30 -f image2 -s 540x540 -i "%07d.png" -vcodec libx264 -crf 17 -pix_fmt yuv420p output.mp4
```


