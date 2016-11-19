<hr>
# Simulating a Self Driving Car

![Demo](https://github.com/Aniruddha-Tapas/Simulating-a-Self-Driving-Car/blob/master/screencast/output.gif)

Overview
============
A project that trains a virtual car to how to move an object around a screen (drive itself) without running into obstacles using a type of reinforcement learning called Q-Learning. More information can be found on the writeup about this project in [part 1](https://medium.com/@harvitronix/using-reinforcement-learning-in-python-to-teach-a-virtual-car-to-avoid-obstacles-6e782cc7d4c6), [part 2](https://medium.com/@harvitronix/reinforcement-learning-in-python-to-teach-a-virtual-car-to-avoid-obstacles-part-2-93e614fcd238#.vbakopk4o), and [part 3](https://medium.com/@harvitronix/reinforcement-learning-in-python-to-teach-an-rc-car-to-avoid-obstacles-part-3-a1d063ac962f). 

Dependencies
============

* Numpy (http://www.numpy.org/)
* Pygame. I used these instructions: http://askubuntu.com/questions/401342/how-to-download-pygame-in-python3-3 but with ```pip3 install hg+http://bitbucket.org/pygame/pygame``` after I installed the dependencies
* Pymunk. Use Pymunk 4. Using version 5 will not work as it was a major refactor. V4 is [here](https://github.com/viblo/pymunk/releases/tag/pymunk-4.0.0)
* Keras ```pip3 install keras```
* Theanos ```pip3 install git+git://github.com/Theano/Theano.git --upgrade --no-deps```
* h5py ```pip3 install h5py```

Basic Usage
===========

1. Update pymunk to python3 by CDing into its directory and running  ```2to3 -w *.py```. Then copy and replace the sub-folder "pymunk" from this directory with your installed "pymunk" sub-folder.

2. First, you need to train a model. This will save weights to the `saved-models` folder. You can train the model by running `python3 learning.py` It can take anywhere from an hour to 36 hours to train a model, depending on the complexity of the network and the size of your sample. However, it will output weights every 25,000 frames, so you can move on to the next step in much less time.

3. Edit the `nn.py` file to change the path name for the model you want to load. I've uploaded my own trained models, you can directly use them as a demo, or go ahead to train the system yourself. 

4. Then finally, watch the car drive itself around the obstacles! Run `python3 playing.py`


Credits
===========
This project is inspired and built with the help of this [blog](https://medium.com/@harvitronix/using-reinforcement-learning-in-python-to-teach-a-virtual-car-to-avoid-obstacles-6e782cc7d4c6) at [medium.com](https://medium.com/). Hence, credit for the majority of code here goes to [Harvitronix](https://github.com/harvitronix/reinforcement-learning-car). Below are a few references he cited. 

- Playing Atari with Deep Reinforcement Learning - http://arxiv.org/pdf/1312.5602.pdf
- Deep learning to play Atari games: https://github.com/spragunr/deep_q_rl
- Another deep learning project for video games: https://github.com/asrivat1/DeepLearningVideoGames
- A great tutorial on reinforcement learning that a lot of my project is based on: http://outlace.com/Reinforcement-Learning-Part-3/

<hr>
