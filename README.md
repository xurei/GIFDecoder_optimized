This is an optimized version of the GIFDecoder and GIFEncoder classes, by László Zsidi. (source: http://www.phpclasses.org/package/3234-PHP-Split-GIF-animations-into-multiple-images.html
and http://www.phpclasses.org/package/3163-PHP-Generate-GIF-animations-from-a-set-of-GIF-images.html)

It avoid GIFGetByte/GIFPutByte for the images content. Instead, it is copied directly to the returned images. This eliminates a lot of ord() and chr() calls, which leads to about x4 speed improvement for large images.

Some other improvements :
- it uses the SplFixedArray to improve the performances of GIFGetByte, so it requires PHP >=5.3.
- it allows you to extrct the dimensions and position of each frame, if you want to rebuild your animation after some modifications.
- GIFEncoder : added transparency feature
