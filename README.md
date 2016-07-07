# pinelli_post
create prores 422 HQ master files to be used in Davinci Resolve for conforming

convert AVCHD C100 clips in prores and from 50 fps to 25 fps

create batch file:
$ ls > file_list.txt
$ cat file_list.txt | awk '{print "ffmpeg -i "$1" -c:v prores_ks -profile:3 -o -r 25 "$1".mov"}' > transcode_script.sh

create a script which is a list of terminal commands like this below:

$ ffmpeg -i 00001.MTS -c:v prores_ks -profile:3 -o -r 25 00001.MTS.mov

add #!/bin/bash and do chmod 777 transcode_script.sh

$ ./transcode_script.sh


