# pinelli_post
convert AVCHD C100 clips in prores and from 50 fps to 25 fps

ffmpeg -i 00001.MTS -c:v prores_ks -profile:3 -o -r 25 00001.MTS.mov


