====================
Datasets
====================


the Use of

Download: baidu link: https://pan.baidu.com/s/1ORx2GiM8YoM2iPw5iJWX4A?pwd=uluw 

Extraction code: uluw

This data set is only for academic research and exchange, and does not support commercial use. 
Some materials refer to network resources, and the copyright belongs to the original author of 
the materials, and the copyright of the rest belongs to Zhejiang University of Media and Communication 
(No. 998 Xueyuan Street, Qiantang District, Hangzhou, Zhejiang Province, China).

This data set continues to be updated, please pay attention.



========================
For training and evaluation, we collected video clips from various types of film and television works,
and have done a lot of work to these data.Here we give an overview of our datasets FEASSTM, 
which consists of 3 parts (Video Datasets, Face-Alignment Frame Datasets, Acting Skill Annotation Datasets)
/*(FEASSTM-V, FEASSTM-FAF, FEASSTM-ASA)*/, and make further explanation of its source and method of acquisition.

Video Dataset (FEASSTM-V)
The dataset consists of 94 video clips, which from 24 film and television works and involved 47 actors. 
Ensuring the diversity of data,the film and television works we selected covering a wide range of subjects,
 from love to war.Among them, the actors' acting performance also has different levels.Each video clip is 
cut according to the actor's role and based on the original film and television clip,and the length of the clip ranges from 1 ~ 155 seconds.

Face-Alignment Frame Dataset (FEASSTM-FAF)
We converted FEASSTM-V into frame image and output the corresponding text file which contains the image name of the corresponding image
 frame sequence , and we label the frame image of emotion expression of the text file artificially . The corresponding relationship of expression
 labeling is as follows : 1 - Surprise, 2 - Fear , 3 - Disgust , 4 - Happy , 5 - Sadness , 6 - Anger , 7 - Neutral . 
In order to improve the efficiency of subsequent face alignment, we preprocess video frames. Firstly ,we delete irrelevant frame images and
 retain human frame images. After the first step is completed,we use Emotion-FAN【a】 for face detection and alignment of frames,and resize
 cropped frames to 100×100.
Based on the results of face alignment, we manually delete some images,which may have problems as follows: Face alignment failure,
 incomplete facial features, facial blurring, etc. Then we normalize the image name to ensure that the image name is continuous, 
and update the annotation TXT file. We ended up with 22,213 images, which we called Face-Alignment Frame Dataset (FEASSTM-FAF). 
And we divided it into two splits: Train (4443 samples) and Test (7770 samples).

【a】ICIP 2019 Frame Attention Networks for Facial Expression Recognition in Videos

Acting Skill Annotation Dataset (FEASSTM-ASA)
We divided FEASSTM-V into three groups (A-33 clips, B-21 clips and C-40 clips),every group has 4 raters.Our experiment settings were similar to 【x,y】.
In the experiment, raters are required to describe the expression changes of actors in the scenes in the questionnaire and rate their acting skills
 on a scale of 5. The rating relationship of actors' acting skill performance is as follows : 1- very bad, 2- bad, 3- competent, 4- good, 5- excellent. 
And raters were also required to select 5 frames from the corresponding face-frame which could best reflect the performance level of the rated
 actors.Each actor in each segment would be scored by four people and four different acting scores were accumulated so as to obtain acting
 scores with more obvious quantitative level as test and training data.


【x】JHU-ISI Gesture and Skill Assessment Working Set (JIGSAWS): A Surgical Activity Dataset for 
Human Motion Modeling 
【y】CVPR21-Towards Unified Surgical Skill Assessment
