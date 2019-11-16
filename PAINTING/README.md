# Copying Artistic Style with CNN

![](./writing.gif)

## Creating the environment
The version of the code I used required a few calories to solve. I got it to work with Tensorflow 1.15 and scipy 1.3.1. Since my regular python has TF=2.0, I set up a virtual environment... <BR>

```
> pip install virtualenv
> virtualenv venv
> source venv/bin/activate
(venv)> pip install tensorflow==1.15.0
```
Next, you need to grab the pre-built model file (<b>imagenet-vgg-verydeep-19.mat</b>) and put it in the working directory. It's too large (>500Mb) to include in github: <br>
The file is located in several places. Here's one: https://www.kaggle.com/teksab/imagenetvggverydeep19mat/download

## Running the Code
Note: running the code this way should give you the VanGogh results. <BR>
Swap out your own style and content photos by changing the image locations in <b>paint.py</b> <BR>  
The first few lines will confirm you have the right TF and SciPy versions... <BR>  

```
> source venv/bin/activate
(venv)> python 
Python 3.7.4 (default, Jul  9 2019, 18:13:23)
[Clang 10.0.1 (clang-1001.0.46.4)] on darwin
Type "help", "copyright", "credits" or "license" for more information.

>>> import tensorflow as tf
>>> print(tf.__version__)
1.15.0

>>> import scipy
>>> print(scipy.__version__)
1.3.1
>>> ctrl-D

(venv)> python paint.py
(venv)> deactivate
```
<BR>
If this worked, you should see your results with a datetime stamp in the <b>./output</b> folder.
