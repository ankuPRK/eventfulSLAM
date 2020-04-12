# Current Issue
Figure out why the camera goes super far after a few seconds from initializaiton (is it because there's not enough features? If the device moving too fast?

# To Do
1) Double check camera configuration file ```VINS-Mono/config/dvs/dvs_config.yaml```
2) Test with a different rosbag file. To remap topic name, look at the configureTopics.launch. Also, remember to edit the parameters in the ```dvs_config.yaml```. Some parameters you may need to change according to the dataset are fx, fy, px, py, cx, cy, k1, k2 and image pixel.

The camera parameter fx, fy, px, py, cx, cy, k1, k2  can be found from downloading the txt.zip files from here: http://rpg.ifi.uzh.ch/davis_data.html

Check camera pixel by https://superuser.com/questions/275502/how-to-get-information-about-an-image-picture-from-the-linux-command-line

```roslaunch vins_estimator dvs.launch```


```rosbag play \PATH TO FILE\boxes_translation.bag```


```roslaunch \VINS-Mono\launch\configureTopics.launch ```