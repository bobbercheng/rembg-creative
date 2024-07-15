This service uses SOTA model ViTMatte to remove background image for any images especially for retailer product images. It uses cog as container, refer to https://cog.run/.
It's recommended to run Nvidia A40 GPU. To test it without GPU, please change gpu to false in cog.yaml file and run ```cog predict -i image=@test.png```

To test http service locally, you need to run
```
cog build -t r8.im/bobbercheng/rembg-creative
docker run -d -p 5000:5000 --gpus all r8.im/bobbercheng/rembg-creative
curl http://localhost:5000/predictions -X POST \
    -H 'Content-Type: application/json' \
    -d '{"input": {"image": "https://.../test.jpg"}}'
```
