# 3D-Object-Detection
Midterm second course in the Udacity Self-Driving Car Engineer Nanodegree Program.

## **Task :**
When the code is functional, you are supposed to use the viewer to locate and closely inspect point-clouds on vehicles and write a short report that includes the following items:
* Find and display 10 examples of vehicles with varying degrees of visibility in the point-cloud
* Identify vehicle features that appear as a stable feature on most vehicles (e.g. rear-bumper, tail-lights) and describe them briefly. Also, use the range image viewer from the last example to underpin your findings using the lidar intensity channel.

## **Computing Lidar Point-Cloud from Range Image :**

### **--> Visualize range image channels [ID_S1_EX1] :**

The show_range_image function located in the file objdet_pcl.py is edited, where we can then extract the lidar data from the frame and extract the range image, it is then converted to 8-bit scale.

![Figure_1](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_1.png)

In the file **loop_over_dataset.py**, the **"exec_visualization"** is edited to be **"exec_visualization = ['show_range_image']"** to display the **range_image**.

### **--> Visualize lidar point-cloud [ID_S1_EX2] :**
**Steps:**
* Initialize th open3d
* Great the instace of open3d point-cloud
* Convert the point-cloud into 3d

In the file **loop_over_dataset.py**, the **"exec_visualization"** is edited to be **"exec_visualization = ['show_pcl']"** to display the **point cloud visualization**. The following are captures of different point clouds with marking of cars and trucks.

![Figure_2](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_2.png)
![Figure_3](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_3.png)
![Figure_4](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_4.png)
![Figure_5](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_5.png)
![Figure_6](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_6.png)

## **Create Birds-Eye View from Lidar PCL :**

### **Convert sensor coordinates to BEV-map coordinates [ID_S2_EX1] :**
