This service uses SOTA model ViTMatte to remove background image for any images especially for retailer product images. 
It's recommended to run Nvidia A40 GPU. To test it without GPU, please change gpu to false in cog.yaml file and run `cog predict -i image=@test.png`
