# Pneu-CT-Dataset
The Pneu-CT dataset contains CT images, pneumonia segmentation labels, and medical reports from 200 patients diagnosed with pulmonary infections. The data is provided by Shandong Provincial Qianfoshan Hospital and annotated by its physicians. The dataset is split into a training set of 160 cases, a validation set of 20 cases, and a test set of 20 cases.
## Download Link
https://drive.google.com/file/d/1n5WsxQugsJMnLlz7le1RO_0wt3FkODjx/view?usp=sharing
## Use in LanGuideMedSeg/LViT Code
       # --------training.yaml----------
        train_csv_path: ./Pneu-CT/prompt/train.CSV
        train_root_path: ./Pneu-CT/Train
        
        val_csv_path: ./Pneu-CT/prompt/val.CSV
        val_root_path: ./Pneu-CT/Val
        
        test_csv_path: ./Pneu-CT/prompt/test.CSV
        test_root_path: ./Pneu-CT/Test
       # --------dataset.py----------
        image = os.path.join(self.root_path,'Images',self.image_list[idx].replace('L.png','.jpg'))
        gt_ = os.path.join(self.root_path,'GTs', self.image_list[idx]) 
