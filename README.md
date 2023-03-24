# Computer Vision Research Project: Stereo Disparity
 
## Guide
### Import the images.
The images should be store in the folder "Dataset". And the research_project.ipynb should be at the same directory.
 
|-Dataset
|  |───2018-07-09-16-11-56_2018-07-09-16-11-56-702-disparity.png
|  |───2018-07-09-16-11-56_2018-07-09-16-11-56-702-left.jpg
|  |───2018-07-09-16-11-56_2018-07-09-16-11-56-702-right.jpg
|  |───....
|-research_project.ipynb
 
### Create the object
The computation process is implemented in OOP in the class **ComputeDisparity**. To compute the disparity map of two images, we need to initialize an object with 3 elements, 1)path of left image, 2)path of right image and 3)path of ground_truth disparity map.
 
    ```python
     dis_object = ComputeDisparity("./Dataset/2018-07-09-16-11-56_2018-07-09-16-11-56-702-left.jpg",
                             "./Dataset/2018-07-09-16-11-56_2018-07-09-16-11-56-702-right.jpg", 
                             "./Dataset/2018-07-09-16-11-56_2018-07-09-16-11-56-702-disparity.png")
    ```

### Apply the available algorithm 
In the ComputeDisparity, There are lots of algorithms being implemented to compute the disparity map, Take the accelerated SSD as example:

    ```python
     dis_object = ComputeDisparity("./Dataset/2018-07-09-16-11-56_2018-07-09-16-11-56-702-left.jpg",
                             "./Dataset/2018-07-09-16-11-56_2018-07-09-16-11-56-702-right.jpg", 
                             "./Dataset/2018-07-09-16-11-56_2018-07-09-16-11-56-702-disparity.png")

    dis_object.compute_ssd_disparity_acc2(3,70)#3 is the window size and 70 is the search range
    ```

### Analysis the result 
In the ComputeDisparity, The analysis function is being implmented, we can see the result of the implementation with simply call the function analysis()

    ```python
     dis_object = ComputeDisparity("./Dataset/2018-07-09-16-11-56_2018-07-09-16-11-56-702-left.jpg",
                             "./Dataset/2018-07-09-16-11-56_2018-07-09-16-11-56-702-right.jpg", 
                             "./Dataset/2018-07-09-16-11-56_2018-07-09-16-11-56-702-disparity.png")

    dis_object.compute_ssd_disparity_acc2(3,70)#3 is the window size and 70 is the search range
    dis_object.analysis()
    ```

### There are lots of examples of result at second half of the research_project file.



