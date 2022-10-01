# Face-Gan
First attempt with generative adversarial networks! 

I've been having some fun with open-source Kaggle dataset recently. You can find it here https://www.kaggle.com/datasets/jonathanoheix/face-expression-recognition-dataset

Although the dataset is ""small"" a gan still made some decent results! Not photorealistic but more like 'WWI black and white' style. 

I'm testing different generative architectures, one using keras layer UpSampling2d() and another one using Conv2DTranspose(). 

Here's the difference:<br><br>
## GAN 1 (Upsapling2D):
Initial Random Input: *very gaussian*
![upsampling](https://user-images.githubusercontent.com/49094051/193403332-16958b10-55a8-4bf5-9978-00907191030e.PNG)

training progress:<br>
1000 epochs:<br>
![generated_img_1_0](https://user-images.githubusercontent.com/49094051/193402829-e602d784-c233-4730-a85c-8c8bd8c5e13b.png)
![generated_img_122_1](https://user-images.githubusercontent.com/49094051/193403130-2585c258-3999-4c56-bec8-963c316d8484.png)
![generated_img_280_1](https://user-images.githubusercontent.com/49094051/193403132-e267f19a-a1c3-4c75-ab4b-f4d83a1c8037.png)
![generated_img_332_1](https://user-images.githubusercontent.com/49094051/193403133-b65a34e3-83f7-42cd-8045-d617629cd597.png)
![generated_img_7_0](https://user-images.githubusercontent.com/49094051/193403140-8e9242a2-d78b-4a4d-b3a5-dad97fad688a.png)

many more epochs: (best results) <br>
![generated_img_200_1](https://user-images.githubusercontent.com/49094051/193403166-8b97b946-1717-49e6-aa4c-b7820c626bea.png)
![generated_img_94_1](https://user-images.githubusercontent.com/49094051/193403168-2580c737-634c-47e6-a6af-efcf03e4dccb.png)
![generated_img_24_1](https://user-images.githubusercontent.com/49094051/193403170-38d9ddfc-fc99-4c80-b44a-11704ec7c4f6.png)
![generated_img_88_2](https://user-images.githubusercontent.com/49094051/193403171-3d11bcbb-0d79-4ba4-8517-75805262884c.png)
![generated_img_58_2](https://user-images.githubusercontent.com/49094051/193403172-1ec5a6fd-aaed-4982-b525-a7634d2f6662.png)
![generated_img_52_0](https://user-images.githubusercontent.com/49094051/193403173-b1a51304-5b26-4493-87d6-e87db24f99e8.png)
![generated_img_5_0a](https://user-images.githubusercontent.com/49094051/193403174-6a10639c-acee-4446-aa02-462e36846bab.png)
![generated_img_11_0a](https://user-images.githubusercontent.com/49094051/193403176-da440522-cde1-42b7-a3a6-c21499324e94.png)
![a](https://user-images.githubusercontent.com/49094051/193403177-a744bee1-c729-4ead-ab4b-9f45146e6285.png)
![generated_img_76_0](https://user-images.githubusercontent.com/49094051/193403179-775c81c0-8f21-4bed-b4c4-f1ba97ca60b8.png)
![gena](https://user-images.githubusercontent.com/49094051/193403180-6f54d2c7-9cda-4d28-bab3-ad7ed4da4542.png)
![generated_img_10_0](https://user-images.githubusercontent.com/49094051/193403181-ba15fa7a-a69f-4d6c-bad1-970275923f6d.png)

## GAN 2 (Conv2DTranspose): 
Initial Random Input: *more uniform* 
![transpose](https://user-images.githubusercontent.com/49094051/193403255-bbea3c81-e01a-4e62-b31a-3e5406099b06.png)

100 epochs:
![generated_img_98_0](https://user-images.githubusercontent.com/49094051/193403387-221ada17-f159-4351-ac44-1cafb73960da.png)
![generated_img_7_0](https://user-images.githubusercontent.com/49094051/193403397-dc98ad2a-059b-4c87-b350-8e86112cdc60.png)

1000 epochs: *still training...*

many more epochs: *still training...*
