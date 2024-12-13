# Padel ball tracker

 this is a ball tracker for padel which tells you where the ball is and where it hit and if the move is legal or not i made this because i thought tracking a padel ball would be convenient for knowing if the ball is in or out or if the move is legal or not so basically a virtual refferre like football but in padel, i play padel and i know how frustrating it is to hit shots that bounce but are called off when they are not or if it was in or out or if it hit the ball this frustrates almost every padel player so i think this virtual ref can help out some people in game or even help me in game

![image of padel players](https://github.com/dashingbukarsha/padel/blob/main/predict/frame_174_jpg.rf.42b506db27ac8122297e08eea028fbd5.jpg?raw=true)

## The Algorithm

i made the tracker by using code and pictures so identify certain things and i trained a yolov8 model to learn how to track a ball properly and the model works by scanning the picture/video and looking for a ball or an object in motion and it identifies it as the ball to see where it is going and this can be convenient for replays or for shots that were out so basically by tracking the ball and where it went or is going

i downloaded the data base from https://universe.roboflow.com/tennisballs/padel-balls 

## Running this project

1. turn on the jetson nano and connecting to it
2. clone repository
3. run this command to download the docker container `sudo docker run -it --rm --volume $(pwd)/padel:/padel --runtime nvidia us-central1-docker.pkg.dev/woven-edge-323322/jetson/ultralytics`
4. use this for predictions `yolo task=detect mode=predict model=/padel/best.pt conf=0.25 source=/padel/test/images save=True`
5.  and now you get the results in the runs folder

[View a video explanation here](https://youtu.be/5TZpUgW1oRw)
