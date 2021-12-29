## Clonar el repositorio de YoloV5

git clone https://github.com/ultralytics/yolov5
cd yolov5
pip install -r requirements.txt

## Configuración de archivo peces.yml

YOLOv5 🚀 by Ultralytics, GPL-3.0 license
COCO128 dataset https://www.kaggle.com/ultralytics/coco128 (first 128 images from COCO train2017) by Ultralytics
Example usage: python train.py --data coco128.yaml
parent
├── yolov5
└── datasets
     └── peces  ← base de datos de peces


Train/val/test sets as 1) dir: path/to/imgs, 2) file: path/to/imgs.txt, or 3) list: [path/to/imgs1, path/to/imgs2, ..]
path: ../datasets/peces  # dataset root dir
train: images/train2017  # train images (relative to 'path') 128 images
val: images/train2017  # val images (relative to 'path') 128 images
test:  # test images (optional)

# Classes
nc: 2  # number of classes
names: ['carbonero','trucha']  # class names

## Comando utilizado

python train.py --img 640 --batch 16 --epochs 3 --data peces.yaml --weights yolov5s.pt

