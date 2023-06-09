# 3D-Object-Detection
Midterm second course in the Udacity Self-Driving Car Engineer Nanodegree Program.

## **Task :**
When the code is functional, you are supposed to use the viewer to locate and closely inspect point-clouds on vehicles and write a short report that includes the following items:
* Find and display 10 examples of vehicles with varying degrees of visibility in the point-cloud
* Create a Birds-Eye-View
* Detect vehicles in BEV

## **Computing Lidar Point-Cloud from Range Image :**

### **--> Visualize range image channels :**

The show_range_image function located in the file objdet_pcl.py is edited, where we can then extract the lidar data from the frame and extract the range image, it is then converted to 8-bit scale.

![Figure_1](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_1.png)

In the file **loop_over_dataset.py**, the **"exec_visualization"** is edited to be **"exec_visualization = ['show_range_image']"** to display the **range_image**.

### **--> Visualize lidar point-cloud :**
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

**objdet_pcl.py** in **student** folder is edited where a the lidar pcl is made a copy of and transform all metrix into bev-image corrdinates. Elements in lidar are re-arranged by sorting x,y, and -z respectively. Then the intensity value of each unique entry is assigned in lidar_top_pcl to the intensity map. Finally the results are converted to image using OpenCv to got the following results. 

![Figure_7](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_7.png)

## **Model-based Object Detection in BEV Image :**
**objdet_detect.py** file is edited and, **show_labels_in_image** and **show_objects_and_labels_in_bev**, are added to **exec_visualization** in **loop_over_dataset.py** file. The resulting images are shown below.

![Figure_8](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_8.png)
![Figure_9](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_9.png)

## **Performance Evaluation for Object Detection :**
Input frames range is set starting from 100 to 150. **exec_visualization** in **loop_over_dataset.py** is edited by adding **'show_detection_performance'** to it. The resulting performance can be seen in the following images.

![Figure_10](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_10.png)
![Figure_11](https://github.com/DishaJr/3D-Object-Detection/blob/main/Figure_11.png)
