# Rviz PointCloud

In order to get Rviz PointCloud working to have to set a transformation. In a terminal on the client run the command:

`rosrun tf static_transform_publisher 0 0 0 0 0 0 1 map trunk 100`

Then in the another terminal on the client, run:

`rosrun rviz rviz`

Under global options in Rviz set fixed frame to **trunk**. Add a **pointcloud2**. 
Set the topic to one of the camera topics for **pointcloud2**. Change the style
to **Points**. You may want to change the size pixels.
