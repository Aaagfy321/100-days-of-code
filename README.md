My 100 days journey with coding to improve my Machine Learning, Deep Learning, Data Science skills. Posting current updates on twitter: https://twitter.com/AgnMikolajczyk

Day 1
I continued with wav2wav #autoencoder for audio style transfer. Loss decreased gradually during the training, so I've started writing audio generation script Nuty Also, I've added json configuration files with parameters of e.g. melspectrogram.



Wav2wav autoencoder: https://arxiv.org/pdf/1904.08983.pdf
Day 2
Had a little fun with casual convolutions in wav-to-wav autoencoder in #pytorch. Reimplemented&tried to understand it better. Later, experimented a bit with different architectures.

Casual convolutions: https://medium.com/the-artificial-impostor/notes-understanding-tensorflow-part-3-7f6633fcc7c7
Day 3
I came up with an idea for a fun project after working hours. I always wanted to train GANs but popular datasets seemed boring -> I started scraping data with Selenium! It's my first time trying it out and first successfully clicked button felt awesome

Selenium: https://www.selenium.dev/
Selenium for data scraping: https://medium.com/the-andela-way/introduction-to-web-scraping-using-selenium-7ec377a8cf72
BeautifulSoup: https://www.crummy.com/software/BeautifulSoup/bs4/doc/
Day 4
Started generating random RPG-like pixel characters with LPC spritesheet: http://tinyurl.com/yb6yg7kw. I'm creating my own dataset for my experiment with Generative Adversarial Networks. Soon I'll start implementing it in #pytorch

LPC spritesheet: http://tinyurl.com/yb6yg7kw.
Pytorch: https://pytorch.org/
My notebooks:

Download random spritesheet with Selenium
Extract character from spritesheet
           

Day 5
Implemented DCGAN from pytorch tutorial.

Experimented with latent size (input for Generator) and feature map sizes

Added soft and noisy labels

Added Wasserstein loss which is a good solution for mode collapse

Wasserstein loss - https://developers.google.com/machine-learning/gan/loss
mode collapse - https://machinelearningmastery.com/practical-guide-to-gan-failure-modes/
Added dropout in both generator and discriminator

DCGAN Tutorial

Dataset


Download dataset here
Results
My final code with modified DCGAN


Day 6
Today practiced a bit with custom data loaders in pytorch: https://pytorch.org/tutorials/beginner/data_loading_tutorial.html Started writing generator code for my wav-to-wav autoencoder.

Day 7
First week finished! Today, I've experimented with a XLA for TPU with multiprocessing, the notebook shared on Kaggle for Flower classification challenge. https://kaggle.com/dhananjay3/fast-pytorch-xla-for-tpu-with-multiprocessing https://www.kaggle.com/c/flower-classification-with-tpus/notebooks?sortBy=relevance&group=everyone&search=pytorch&page=1&pageSize=20&competitionId=18278

Day 8
Continued having fun with #GenerativeAdversarialNetwork - this time Conditional GANs on retro pixel game dataset - http://github.com/AgaMiko/pixel_character_generator I've managed to modify code and run the training, can't wait to see the results

Day 9
Today finished Conditional DCGAN experiments! GAN generates a pixel character seen from selected angle.

different learning rate for discriminator and generator
soft labels
added classification loss to the discriminator. Discriminator have to guess fake/real but also the character angle
generator is conditioned with embedding from trainable look-up table that gives the info about the character view angle


notebook with modified Conditional DCGAN
