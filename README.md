# creating-_DCGAN
created a DC_GAN using the MNSIT dataset
Use convolutions without any pooling layers

Use batchnorm in both the generator and the discriminator

Don't use fully connected hidden layers

Use ReLU activation in the generator for all layers except for the output, which uses a Tanh activation.

Use LeakyReLU activation in the discriminator for all layers except for the output, which does not use an activation

Here's roughly the progression you should be expecting. On GPU this takes about 30 seconds per thousand steps. On CPU, this can take about 8 hours per thousand steps. You might notice that in the image of Step 5000, the generator is disproprotionately producing things that look like ones. If the discriminator didn't learn to detect this imbalance quickly enough, then the generator could just produce more ones. As a result, it may have ended up tricking the discriminator so well that there would be no more improvement, known as mode collapse

<img width="688" alt="image" src="https://github.com/Nicole09999/creating-_DCGAN/assets/106644205/92712e87-4b83-4531-8ede-9b3fb4092eaa">
