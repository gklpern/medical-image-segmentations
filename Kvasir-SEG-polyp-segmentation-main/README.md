# Polyp Segmentation with U-Net (ResNet34)

## Project Overview
This project implements 2D semantic segmentation for polyp detection in endoscopy images using the Kvasir-SEG dataset.  
The baseline model is U-Net with a ResNet34 encoder. Models are trained and evaluated using Dice and IoU metrics.

---

## Dataset
- Kvasir-SEG: 1000 images with corresponding pixel-level polyp masks.  
- Preprocessing: resized to 256×256, normalized, masks binarized (0/1).  
- Augmentations: horizontal/vertical flips, rotations, brightness/contrast changes, zoom, blur.  

<img width="744" height="326" alt="image" src="https://github.com/user-attachments/assets/b133ce4d-7568-43be-80d5-eca82a10cf43" />

<img width="503" height="405" alt="image" src="https://github.com/user-attachments/assets/2f5d0195-0595-4360-92ee-9a2bc3728cf6" />

<img width="606" height="307" alt="image" src="https://github.com/user-attachments/assets/f8d5fc36-5ba5-410d-b596-6e4f3949e1b5" />


---

## Model
- Architecture: U-Net with ResNet34 encoder (ImageNet pretrained).  
- Loss: BCE + Dice combination.  
- Metrics: Dice Score, IoU.  



---

## Training & Evaluation
- Optimizer: Adam (lr = 1e-4)  
- Epochs: 20  
- Batch size: 8  
- Metrics tracked: Loss, Dice, IoU  

<img width="1106" height="416" alt="image" src="https://github.com/user-attachments/assets/b901ddb8-e0e7-4fd1-bc00-852c51c0f269" />


---

## Results
Model: unet_resnet34
Best Val Dice: 0.9758
Best Val IoU:  0.9528
Last Val Dice: 0.9661
Last Val IoU:  0.9348

<img width="839" height="558" alt="image" src="https://github.com/user-attachments/assets/3766431d-dae9-42a9-a256-d6883d06686b" />

---

## How to Run
1. Clone repository and install dependencies:
   ```bash
   git clone https://github.com/<your-repo>/polyp-segmentation.git
   cd polyp-segmentation

