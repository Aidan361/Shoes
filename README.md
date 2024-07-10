# Shoe Types using NVIDIA

Ever curious as to what type of shoes you wear? Probably not, but if were interested, you can use the AI program to fulfill your curiousity.

![Boat Shoe](https://github.com/Aidan361/Shoes/assets/175229980/05d8f318-48f8-4d7e-b312-9d0229042b99)

## The Algorithm and how it Works

It takes a photo of some shoes that you give it, and detects what kind of shoes they are. It detects several types of shoes such as Sneakers or Boat Shoes, but not all types of shoes.
Included Shoe Types:
 - Ballet Flat Shoes
 - Boat Shoes
 - Brogue Shoes
 - Clog Shoes
 - Sneakers

## Running The Algorithm

1. Setup and install Jetson Nano and VSCode
2. Connect Jetson Nano to your computer hotspot, write down your Jetson Nano's IP for later use
3. Connect your VSCode to your jetson nano with 'ssh nvidia@IPAddress'
4. Open the NVIDIA home folder
5. Open terminal and use 'cd jetson-inference/python/training/classification' to enter the needed directory
6. Use 'DATASET=data/FOLDER_NAME' to set NET and DATASET for later use, replace FOLDER_NAME with whatever the file you create
7. Move the picture you're using into 'classification' folder
8. Run the model 'imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt IMAGE_RELATIVE_PATH output/FILE_OUTPUT_NAME' Replace IMAGE_RELATIVE_PATH of your image and IMAGE_OUTPUT_NAME with the name of the output image.
