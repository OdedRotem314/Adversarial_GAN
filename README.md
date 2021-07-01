# Adversarial_GAN
Infer a black box (random forrest) classifier output and generate new data using a GAN like architecture.
A black box classifier is trained on diabetes tabular data to classify if a patient may have a diabetese illness.
Then a adversarial network generates samples and feeds it to the black box classifier which outputs a probability score of how likely the patient has diabetes.
Then a random scalar and output of the black box together with the generated sample are fed to a discriminator network which decides if the sample is closer in score to the classifier outpur or random scalar.

![image](https://user-images.githubusercontent.com/63725708/124120645-aab94300-da7c-11eb-8ee3-e45f696b8662.png)

The generator receives two inputs – Z and C – and produces a 
sample. This sample is sent to the discriminator, which also receives C (same C as the generator) and 
the output of the BB model for this sample. The goal of the discriminator is to determine which 
classification is the “real” one (i.e., produced by the BB model)
The goal of the discriminator is to determine which of the two values – C or Y – is the true 
classification produced by the black-box model. The output of the discriminator, denoted by 
�", will be used for the calculation of the loss in the standard fashion
