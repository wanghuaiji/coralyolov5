# coralyolov5
# coralyolov5 environment setup
git clone https://github.com/wanghuaiji/coralyolov5 # clone 

cd coralyolov5 

pip install -r requirements.txt # install
# Tutorial
#Download data named coral-data from kaggle

kaggle datasets download -d huaijiwang/coral-data

#Modify the dataset.py path of the train.py file in the segment folder to your own path, and modify the data storage path in the dataset.py file to your own path.
#run coralyolov5/segment/train.py to train a model. If you want to use pretrained weight, you can get my trained weight best.pt from https://www.kaggle.com/datasets/huaijiwang/coral-data

cd segment python train.py

#run coralyolov5/segment/train.py to verify my trained model or your trained model, you also need to modify the path in the file. You can get my trained weight best.pt from https://www.kaggle.com/datasets/huaijiwang/coral-data

python val.py

#run coralyolov5/segment/predict2coral.py to get the whitening rate and the health rate, you also need to modify the path in the file. You can get my trained weight best.pt from https://www.kaggle.com/datasets/huaijiwang/coral-data

python predict2coral.py
