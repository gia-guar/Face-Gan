# Face-Gan
First attempt with generative adversarial networks! 

:warning: COMMENT :warning: these lines in GAN1 notebook if you intend to run it for the firs time!<br>
*generator = load_model(os.path.join('models','face_generator.h5'))*<br>
*discriminator = load_model(os.path.join('models','face_discriminator.h5'))*
these lines are made to train the model in different sessions 

I've been having some fun with open-source Kaggle dataset recently. You can find it here: https://www.kaggle.com/datasets/jonathanoheix/face-expression-recognition-dataset <br>
some examples:<br>
![33](https://user-images.githubusercontent.com/49094051/193403879-1ccab13e-9005-4e0c-bbef-5e9c50ec5112.jpg)
![4](https://user-images.githubusercontent.com/49094051/193403891-720cf792-929d-4b17-9369-530476395d89.jpg)
![1907](https://user-images.githubusercontent.com/49094051/193403909-251536d6-7755-4466-ba92-e7bcf5fc94bd.jpg)
![317](https://user-images.githubusercontent.com/49094051/193403929-7eee066b-9ba6-451c-9c93-6d262c3bc59a.jpg)
![1112](https://user-images.githubusercontent.com/49094051/193403933-b8745056-16e1-4d0d-bf81-32824aef1e3b.jpg)
![2787](https://user-images.githubusercontent.com/49094051/193403940-4502852f-7ad3-471d-ae88-4f77750dd12f.jpg)
![9366](https://user-images.githubusercontent.com/49094051/193403945-bfb5c4c9-c82d-41d4-a361-41863d04464e.jpg)
![34](https://user-images.githubusercontent.com/49094051/193403959-cc5d7de4-6c01-4a1c-9ca0-d788d2108c5d.jpg)

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

100 epochs:<br>
![generated_img_98_0](https://user-images.githubusercontent.com/49094051/193403387-221ada17-f159-4351-ac44-1cafb73960da.png)
![generated_img_7_0](https://user-images.githubusercontent.com/49094051/193403397-dc98ad2a-059b-4c87-b350-8e86112cdc60.png)
![generated_img_2_0](https://user-images.githubusercontent.com/49094051/193403710-ced6974b-3db0-40e8-9ff2-b46aa95c090d.png)

1000 epochs:<br>
![generated_img_32_0](https://user-images.githubusercontent.com/49094051/193418022-6eea7d42-b450-41b3-8bb1-3f606af4e126.png)
![generated_img_21_0](https://user-images.githubusercontent.com/49094051/193418023-88571059-62c9-43a7-8e9d-81b5ac665701.png)
![generated_img_61_0](https://user-images.githubusercontent.com/49094051/193418024-5ac5a729-b2db-4068-ba68-3dcac4825727.png)

many more epochs: <br>
![generated_img_19_0](https://user-images.githubusercontent.com/49094051/193428705-44a4836e-1194-4904-a93a-1a0ffc60a1dc.png)
![generated_img_93_0](https://user-images.githubusercontent.com/49094051/193428706-729e82fd-5cdd-48f8-8de9-36057793f0ed.png)
![generated_img_94_0](https://user-images.githubusercontent.com/49094051/193428707-7bff618e-0041-4177-a967-762a6c0ecaa7.png)


## OBSERVATIONS
- both GANSs doesn't seem to be able to converge even after days of training. This may be due to the size of the dataset
- gan 1 permorms overall better 
- the generator can't generalize different faces, only one. This means that the input noise should have bigger dimension (*not sure, investivage*)

## TO DO LIST
- try with bigger dataset available at https://drive.google.com/drive/folders/1-5oQoEdAecNTFr8zLk5sUUvrEUN4WHXa
- explore different architectures
- Manage a way to handle bigger size images without buying a new GPU (OOM problem)


# 3/10/2022 UPDATE
After having tried with a different dataset (30 k faces from FFHQ dataset) mentioned above the imporvements were astonishing. I'm happy to share some results below. 

![generated_img_43_1](https://user-images.githubusercontent.com/49094051/193564425-7a1f8c31-e835-4426-a063-550c1e7aa256.png)
![generated_img_45_2](https://user-images.githubusercontent.com/49094051/193564427-007df028-e275-4d29-9d8f-1c641a9218ad.png)
![generated_img_47_0](https://user-images.githubusercontent.com/49094051/193564428-4ce10fe6-d1d1-4c9a-b80f-3da6a44e8439.png)
![generated_img_48_2](https://user-images.githubusercontent.com/49094051/193564429-12968501-32f5-488e-a528-ef7e523ef025.png)
![generated_img_13_1](https://user-images.githubusercontent.com/49094051/193564431-ce70a5dc-d904-4982-aa30-d009970f8ef5.png)
![generated_img_15_0](https://user-images.githubusercontent.com/49094051/193564432-549cef74-1229-4710-9f2b-e3776d78a450.png)
![generated_img_22_2](https://user-images.githubusercontent.com/49094051/193564436-e8933452-9084-4975-aaa0-7be57d1477be.png)
![generated_img_44_1](https://user-images.githubusercontent.com/49094051/193564449-52d4a08b-3cc0-4414-895c-291fc82f872e.png)
<br>
<br>
*...currently working of dataset expansion up to 50 k items*
