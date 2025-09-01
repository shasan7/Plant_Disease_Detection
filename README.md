# Plant_Disease_Detection

## Dataset Link: https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset

## Kaggle Notebook: https://www.kaggle.com/code/shasan7/plant-disease-detection

The images were transformed and normalized using torch, then we fed them to the **pretrained BiT (Big Transform) with ResNetV2 backbone model for fine-Tuning**

**The best validation accuracy achieved by our model is 99.68%**.

Training Summary:

    Epoch [1/10]  Train Loss: 0.1816 | Train Acc: 94.59%  || Val Loss: 0.1237 | Val Acc: 96.03%
    Saved new best model with val_acc: 96.03%
    Epoch [2/10]  Train Loss: 0.0648 | Train Acc: 98.10%  || Val Loss: 0.0506 | Val Acc: 98.62%
    Saved new best model with val_acc: 98.62%
    Epoch [3/10]  Train Loss: 0.0433 | Train Acc: 98.76%  || Val Loss: 0.0247 | Val Acc: 99.15%
    Saved new best model with val_acc: 99.15%
    Epoch [4/10]  Train Loss: 0.0317 | Train Acc: 99.05%  || Val Loss: 0.0258 | Val Acc: 99.09%
    Epoch [5/10]  Train Loss: 0.0253 | Train Acc: 99.24%  || Val Loss: 0.0223 | Val Acc: 99.29%
    Saved new best model with val_acc: 99.29%
    Epoch [6/10]  Train Loss: 0.0199 | Train Acc: 99.42%  || Val Loss: 0.0112 | Val Acc: 99.68%
    Saved new best model with val_acc: 99.68%
    Epoch [7/10]  Train Loss: 0.0174 | Train Acc: 99.48%  || Val Loss: 0.0269 | Val Acc: 99.24%
    Epoch [8/10]  Train Loss: 0.0146 | Train Acc: 99.54%  || Val Loss: 0.0237 | Val Acc: 99.25%
    Epoch [9/10]  Train Loss: 0.0126 | Train Acc: 99.66%  || Val Loss: 0.0136 | Val Acc: 99.56%
    Epoch [10/10]  Train Loss: 0.0118 | Train Acc: 99.64%  || Val Loss: 0.0114 | Val Acc: 99.67%


Obtained Results:

    Classification Report:

                                                            precision    recall  f1-score   support
        
                                        Apple___Apple_scab       1.00      1.00      1.00       504
                                         Apple___Black_rot       1.00      1.00      1.00       497
                                  Apple___Cedar_apple_rust       1.00      1.00      1.00       440
                                           Apple___healthy       1.00      1.00      1.00       502
                                       Blueberry___healthy       1.00      0.99      1.00       454
                  Cherry_(including_sour)___Powdery_mildew       1.00      0.99      1.00       421
                         Cherry_(including_sour)___healthy       1.00      1.00      1.00       456
        Corn_(maize)___Cercospora_leaf_spot Gray_leaf_spot       0.98      0.99      0.98       410
                               Corn_(maize)___Common_rust_       1.00      1.00      1.00       477
                       Corn_(maize)___Northern_Leaf_Blight       0.99      0.98      0.98       477
                                    Corn_(maize)___healthy       1.00      1.00      1.00       465
                                         Grape___Black_rot       1.00      1.00      1.00       472
                              Grape___Esca_(Black_Measles)       1.00      1.00      1.00       480
                Grape___Leaf_blight_(Isariopsis_Leaf_Spot)       1.00      1.00      1.00       430
                                           Grape___healthy       0.99      1.00      0.99       423
                  Orange___Haunglongbing_(Citrus_greening)       1.00      1.00      1.00       503
                                    Peach___Bacterial_spot       1.00      1.00      1.00       459
                                           Peach___healthy       1.00      1.00      1.00       432
                             Pepper,_bell___Bacterial_spot       1.00      1.00      1.00       478
                                    Pepper,_bell___healthy       1.00      0.99      0.99       497
                                     Potato___Early_blight       1.00      1.00      1.00       485
                                      Potato___Late_blight       1.00      1.00      1.00       485
                                          Potato___healthy       1.00      1.00      1.00       456
                                       Raspberry___healthy       1.00      1.00      1.00       445
                                         Soybean___healthy       1.00      1.00      1.00       506
                                   Squash___Powdery_mildew       1.00      1.00      1.00       434
                                  Strawberry___Leaf_scorch       1.00      1.00      1.00       444
                                      Strawberry___healthy       1.00      1.00      1.00       456
                                   Tomato___Bacterial_spot       1.00      0.99      1.00       425
                                     Tomato___Early_blight       1.00      0.99      0.99       480
                                      Tomato___Late_blight       0.98      1.00      0.99       463
                                        Tomato___Leaf_Mold       1.00      1.00      1.00       470
                               Tomato___Septoria_leaf_spot       1.00      1.00      1.00       436
             Tomato___Spider_mites Two-spotted_spider_mite       1.00      0.99      0.99       435
                                      Tomato___Target_Spot       0.98      1.00      0.99       457
                    Tomato___Tomato_Yellow_Leaf_Curl_Virus       0.99      1.00      1.00       490
                              Tomato___Tomato_mosaic_virus       1.00      1.00      1.00       448
                                          Tomato___healthy       1.00      0.99      1.00       482
        
                                                  accuracy                           1.00     17574
                                                 macro avg       1.00      1.00      1.00     17574
                                              weighted avg       1.00      1.00      1.00     17574


![Confusion Matrix: ](Conf_Mat.png)

![Accuracy Curve: ](Acc.png)

![Loss_Curve): ](Loss.png)
