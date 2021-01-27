---
layout: post
title: The technology we use
---

## Training the network : 

<p>For this project we built a GAN (Generative Adversarial Network) using the Tensorflow API with Python. </p>
<p>This is what our GAN looks like : </p>
![GAN description](/images/GAN_General.png)
<p>As you can see, our network works with different inputs. We pass it an image of random noise and a real image from our database but randomly masked. 
The Generator will then try to complete the image where the mask was applied. 
Then it passes its result to the Discriminator and tries to fool it, making it believe that his image is an image from the database. 
How much the Discriminator was fooled is indicated by a precision, basically indicating if the Generator did a good job. 
Knowing this the Generator will try again and so on until the end of the training.</p>

<p>The Generator is built like this :</p>
![GAN description](/images/Generator.png)

<p>And the Discriminator like this :</p>
![GAN description](/images/Discriminator.png)

## Using the network : 

<p>Once we are satisfied with the results of the training of our network, we can use it. But how ?
Basically we use Tensorflow to transform our Python model in a Javascript model so that we can use it in a website. </p>

