![Rules](https://cdn.ebaumsworld.com/mediaFiles/picture/1903451/85895170.gif)

# _**Detection of Helmet and Number Plate extraction from videos or images**_
Don’t Break Traffic Rules is basically a small yet massive background application model, which allows the users to detect and even capture the riders riding their vehicle without wearing helmet. So obviously yolo has been used to perform this type of task, since due to its scalability and efficiency it detects the objects in an image or video accurately, Since it was manually trained on 1000’s of images to perform this task. Along with yolo we have also used OpenCV and Tkinter gui to build a front-end framework.

# _**Base paper**_
+ https://www.irjet.net/archives/V6/i12/IRJET-V6I1214.pdf
+ https://www.academia.edu/36368794/VEHICLE_NUMBER_PLATE_DETECTION_USING_IMAGE_PROCESSING
+ https://ijariie.com/AdminUploadPdf/HELMET_DETECTION_AND_LICENSE_PLATE_RECOGNITION_USING_YOLO_MODEL_ijariie16847.pdf


# _**Algorithm Description**_
YOLOv5 is an abbreviation word for You look only once, where this algorithm has shaken most of the developers all around the world in the past 5 years, due to its immense ability to quickly learn and remember any object we have trained or labelled it. There is a unique method to work with yolo models where we require the images to be labelled firstly using specific tools available online or installing it in your local machine. (Labelling software’s links are provided below). the labelling process might take a long time depending upon on your dataset. The images are labelled according to the specification made by the user, whether we'd like to detect multiple objects in an image are single object, depending on it, the text file is created with following parameters,
+ The class of the obejcts, startting from 0,1,2..
+ The coordinates of the bounding box drawn.

# _**Reference**_
+ https://machinelearningknowledge.ai/introduction-to-yolov5-object-detection-with-tutorial/
+ https://pytorch.org/hub/ultralytics_yolov5/
+ https://github.com/ultralytics/yolov5

# _**Sample Images**_

![YOLOv5](https://d25j9w72xt9yi4.cloudfront.net/eyJidWNrZXQiOiJkb2Nrc2hpcC1pbWFnZXMiLCJrZXkiOiI1M2Y3ZjRjOGVkM2VmMWJjMjU5ZDY1MWY3Y2YyN2M2OCIsImVkaXRzIjp7InJvdGF0ZSI6bnVsbCwicmVzaXplIjp7ImZpdCI6ImNvdmVyIiwiaGVpZ2h0IjoyNTZ9fX0=)

# _**Sample Label File**_

![Label File](https://upload-images.jianshu.io/upload_images/25249612-97060de553715884.png)

The Label file consists of following items.
+ The class of the object
+ Top_left coordinate of the bounsing box
+ Top_right coordinate of the bounding box
+ Bottom_left coordinate of the bounding box
+ Bottom_right coordinate of the bounding box

# _**How to Execute?**_
So, before execution we have some pre-requisites that we need to download or install i.e., anaconda environment, python and a code editor.
**Anaconda**: Anaconda is like a package of libraries and offers a great deal of information which allows a data engineer to create multiple environments and install required libraries easy and neat.

**Download link:**

![Anaconda](https://1.bp.blogspot.com/-UJ1Ws2zZ9V4/TtMbG2ynJiI/AAAAAAAABbM/m6t2kuEhKdY/s1600/The-biggest-anaconda-snake-3.jpg)

https://www.anaconda.com/

**Python**: Python is a most popular interpreter programming language, which is used in almost every field. Its syntax is very similar to English language and even children and learning it nowadays, due to its readability and easy syntax and large community of users to help you whenever you face any issues.

**Download link:**

![Python](https://i0.wp.com/reptileworldfacts.com/wp-content/uploads/2019/05/male-blonde-super-tiger-reticulated-python.jpg?resize=351%2C351&ssl=1)

https://www.python.org/downloads/

**Code editor**: Code editor is like a notepad for a programming language which allows user to write, run and execute program which we have written. Along with these some code editors also allows us to debug, which usually allows users to execute the code line by line and allows them to see where and how to solve the errors. But I personally feel visual code is very good to work with any programming language and makes a great deal of attachment with user.

**Download links:**

![Vs code](https://schwabencode.com/contents/logos/VS2019-Badge.png) ![Pycharm](https://i0.wp.com/scracked.com/wp-content/uploads/2020/01/PyCharm-2019.3.4-Crack.png?fit=200%2C200&ssl=1)

+ https://code.visualstudio.com/Download, 
+ https://www.jetbrains.com/pycharm/download/#section=windows

# _**How to create a new environment and configure jupyter notebook with it.**_
Let us define an environment and why we need different environments. An environment is a collection of libraries that are required to run our project. When we already have an environment with the necessary libraries, why do we need a new environment?
To avoid version mismatches, we create a new environment for each project. For example, in your previous project, you used "tf env" with tensorflow 2.4 and keras 2.4, but in your current project, you must use tensorflow 2.6 and keras 2.6. If you continue your project in the "tf env" environment, there will be a version mismatch and you will need to update tensorflow and keras, but this will cause problems with the previous project's execution. To avoid this, we create a new environment with tensorflow 2.6 and keras 2.6 and resume our project.

# _**How to create an environment in anaconda.**_
+ Type “conda create –n <<name_of_your_env>>”
example: conda create -n env
+ It will ask to proceed with the environment location, type ‘y’ and press enter.
+ When you press ‘y’, the environment will be created. To activate your environment type conda activate <<your_env_name>> . E.g., conda activate myenv.
+ You can see that the environment got changed after conda activate myenv line. It changed from “base” to “myenv” which means you are now working in “myenv” environment.
+ To install a library in your virtual environment type pip install <library_name>.
e.g., pip install pandas
+ Instead of installing libraries one by one you can even install by bunch, i.e., we have a txt file called requirements.tx which consists of all the libraries required to proceed with the project, so we can use it.
+ so, before installing requirements.txt, make sure you are in the specific path where your requirements.txt is located, basically this file is located in the folder where our executable files are located, so we need to move to that directory by following command.
**cd C:\folder_name**
+ Here A -> drive, folder name -> path where your executable file is saved
+ I go to that file path in anaconda using cd command 
1.	Go to drive where your project file is.
2.	Go to the path of your project using cd <path>
3.	Type pip install –r requirements.txt 
+ And all your required libraries will be downloaded and you can start your project.
+ But if you want to use jupyter notebook on the new environment you have to set it up for the new environment.
+ After you have installed all the libraries and created an environment, you need an editor to run the code, that is starting jupyter notebook, as soon as you enter jupyter notebook in the terminal you will definitely get this error. “Jupiter” is not recognized as an internal or external command.
So, to solve it it we have 2 commands.
1.	conda install –c conda-forge jupyterlab
2.	conda install –c anaconda python
Now you are ready to use jupyter on this environment and start with your project!

![thanks](https://media1.giphy.com/media/ZfK4cXKJTTay1Ava29/giphy.gif)

# _Steps to execute._

**Note:** Make sure you have added path while installing the softwares.

1. Install the prerequisites mentioned above.
2. Open anaconda prompt and create a new environment.
  - conda create -n "env_name" (python==3.6/3.5)
  - conda activate "env_name"
3. Install necessary libraries from requirements.txt file provided.
4. Run pip install -r requirements.txt or conda install requirements.txt (Requirements.txt is a text file consisting of all the necessary libraries required for executing this python file. If it gives any error while installing libraries, you might need to install them individually.)
5. Run python main_image.py in your terminal, make sure that you have your main_image.py and main_image_my_fucntions file in same location, since we import main_image_my_fucntions files into main_image.
(The .py files should be executed on your terminal or if you ahev code editor you can directly execute it from there.)
**Note:** There are 2 different files, if you want to pass an image and extract the number palte and rider images, you need to execute main_image.py, if you want to run the code with video file you need to run main_video.py

# _Labelling the images._
If you guys ever feel like bored and wanna spend your time for something good, you can sit idle and label images, which might really help people around you to do some crazy things.(Whatever im saying it is done in python)
### Steps to label images.
1. Download the labelimg.zip file from the below link provided.
https://github.com/tzutalin/labelImg
2. Open your anaconda prompt and create a new environment in the location where you have unzipped your labelling files.
3. After that, past the following line of code in your terminal and press enter.
**pyrcc5 -o libs/resources.py resources’**
4. pip install lxml
5. Run python labeling.py, it will open the window, where you can start labelling.
6. Run python labeling.py [image_path_folder] [pre_defined_class_file], here pre_defined_class_file represents the number of classes you need to your data, so you need to change it before starting to label your images, you can find that file in data folder.
7. Make sure to change the format to yolo on the left-hand side, where by default it might be in pascal file format.
8. Finally, click on create bounding box icon and start drawing and make sure to provide class to your bounding box every time you draw a box in an image.

![Happy](https://media0.giphy.com/media/l1J9vjZgVNYsSTTeo/giphy.gif)

# _How to run a custom YOLOv5 model in google colab._
+ Click on the mentioned official GitHub repository of yolov5 and either fork it or open it in google colab or you can even run it in your local machine by downloading the files if you have a good system specification.
https://github.com/ultralytics/yolov5
+ Scroll down and open the file in google colab.
+ Make sure your labelled dataset is your drive and ready to be connected with the yolov5 model.
+ Run the first cell and see the magic at the left-hand side of the colab screen.
+ Click on data folder, double click on coco128.yaml file and replace the path of the dataset with your dataset files saved in the drive and also make sure to change the number of classes, the class names should be in **same order** as you have given while labelling.
+ Locate down to training cell and alter the code accordingly, such as number of epochs depending on the accuracy you are getting and also batch size.
**!python train.py --img 640 --batch 16 --epochs 3 --data coco128.yaml --weights yolov5s.pt --cache**
+ Finally, the model will be saved in weights folder, which will be created separate folder **runs** along with the results and evaluation metrics.

# _**Data Description**_
The model has been trained by labelling several images of people riding bikes, the 2 classes which are important for our model is helmet and number plate, so we draw 2 bounding boxes around the person's helmet and around the number plate if it is visible. the .txt file is then saved along with the image automatically. These files are then loaded on top of our YOLOv5 model which has certain specific rules and steps to be followed to train and save our model. After saving we can load our model in different machine and use it for actual production or to test the model by passing in different images and video files.

# _**Issues Faced**_
1. Installing specific face recognition library.
3. We might face an issue while installing specific libraries.
4. Make sure you have the latest version of python, since sometimes it might cause version mismatch.
5. Adding path to environment variables in order to run python files and anaconda environment in code editor, specifically in visual studio code.
6. Make sure to change the path in the code where your dataset/model is saved.
7. **AttributeError: Upsample has no attribute 'recompute_scalr_factor**, This error can be solved by locating **Upsampling.py** file in your **anaconda/lib/site_pcakages/torch/nn/mopdules**, got to 154 line and comment out recompute_scale_factor = self.recompute_scale_factor and amke sure you ahve closed the paranthesis. This is the most common issue where every one have faced.

# _**Note:**_
**All the required data hasn't been provided over here. Please feel free to contact me for model weights and if you face any issues.** 

# _**Lets Connect!!**_
<a href="https://linkedin.com/in/mudassiruddin21" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg" alt="mudassiruddin21" height="30" width="40" /></a>

![Connect](https://media2.giphy.com/media/l1O6zvqu7O317887HF/source.gif)

# _**Yes, You now have more knowledge than yesterday, Keep Going.**_

![Congrats](https://lh3.googleusercontent.com/proxy/hQPDYkEAsrtTY4xcM4ZpU_BYIXbv2gsAXNmoADRg0RQS0A3YlCkFHpWaeAnvOvhTR4fCdpxEd67hBrGkC8fXElkDbaCHvIYOGZhetvvrmh0ZTTnd5YjXTGOcLgT5RPxPu7UQpqh9OpWkAzqwKqw32w=s0-d)
