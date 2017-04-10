# ECUSTFD-resized-
# Background
------
Obesity is a medical condition in which excess body fat has accumulated to the extent that it may have a negative effect on health.  Obesity treatment requires the patients to eat healthy food and decrease the amount of daily calorie intake. For those patients, it is helpful that calories can be estimated from photos.<br><br>
Many methods based on computer vision have been created to estimate calories. There are three steps in calorie estimation: capturing food image(s), detecting food and calibration object, estimating calorie of each food.<br><br>
For those methods, especially deep learning methods, they need a corresponding image dataset to train and test. However, most of the image datasets concentrate on the food detection and just provide different categories of objects, which is not helpful in visual measurement. That's why we create our food image dataset named ECUSTFD(ECUST Food Dataset).
# Introduction
---------
ECUSTFD is a free public food image dataset. Our dataset has 19 types of food as shown in  Figure . The number of food images is 2976. The number of images and the number of objects for the same type are shown as follows:
![food samples](https://github.com/Liang-yc/images4readme/blob/master/food_sample.jpg)
    For a single food portion, we took several groups of images by using smart phones; each group of images contains a top view and a side view of this food. For each image, there is only one coin as calibration object and no more than two foods in it. If there are two food in the same image, the type of one food is different from another. We provide two datasets for researchers: one includes original images and another includes resized images. The size of each image in resized dataset is less than 1000*1000.<br> 
![coin](https://github.com/Liang-yc/images4readme/blob/master/coin%20sides.jpg)<br><br>
    As you see, the diameter of the One Yuan Coin is 25.0mm. In ECUSTFD, only 2 kinds of plates are used when taking photos: a white plate and a red plate. If you want to use the circle plate as the calibration object, you may need the diameter of each plate.The white plate's diameter is about 20.7cm and its height is about 2.0cm; the red plate's diameter is about 18.7cm and its height is about 2.0cm.<br><br>
|![white plate](https://github.com/Liang-yc/images4readme/blob/master/white_plate.JPG)|![red plate](https://github.com/Liang-yc/images4readme/blob/master/red_plate.JPG)|
    Despite of food images, our dataset still provide bounding boxes (we only annotated the resized images because the original images are more than screen resolution and is hard for us to annotate), volume and quality information for each image. For example, we have photos of 19 different apples and provide volume and quality information of those apples. For a single apple image, we offer two bounding boxes: one for the apple and another for One Yuan coin. For each kind of food, energy is obtained from nutrition table and the density is calculated with foods in ECUSTFD. <br><br>
    The volumes we measured in ECUSTFD are not as reliable as the qualities we measured due to the limit of containing cup. Considering that we can only get volume from food images rather than quality, we still keep the volume information as a reference. In addition, you can replace our reference density values to your own density values if you can increase the accuracy in quality estimation.
# Assessment
---------
The dataset with original images and no annotations is publicly available at this [BaiduYun](http://pan.baidu.com/s/1dF866Ut). The small image dataset including annotations, volume and quality information is available at this [github](https://github.com/Liang-yc/ECUSTFD-resized-) or [BaiduYun](http://pan.baidu.com/s/1o8qDnXC). <br><br>
    For ECUSTFD with original images, we only provide images as referred. But we provide the food's weight information in [ECUSTFD_WEIGHT](http://pan.baidu.com/s/1dF866Ut#list/path=%2Fcalorie%20estimation%2FECUSTFD_origin%2FECUSTFD_WEIGHT&parentPath=%2Fcalorie%20estimation) folder. If you are interested in character recognition, you can use those images.<br><br>
    For the small-size ECUSTFD, The annotations of images are saved in the folder named Annotations and images are saved in the JPEGImages folder. density.xls saves food's volume and quality information.
