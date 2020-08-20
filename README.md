# Fast_Ai-Pytorch-Mobile-Custom-Model-Image_Classification
## Data:   
    this project base on insect image classification( 19 classes)
    ./train/┬ant/ ┬ jgpowejgf.jpg 
            |     ├ djqiopwd.jpg
            |     ├ viowhvwe.jpg
            |     └ ....
            ├bee/ ┬ hjoaf.jpg
            |     ├...
            ...
                
    ./val/┬ant/ ┬ gwgw.jpg 
          |     ├ gwegws.jpg
          |     ├ svsqwv.jpg
          |     └ ....
          ├bee/ ┬ qwf2q3.jpg
          |     ├...
          ...
## Model:
    if you want to use state of art model, you can follow the step:
    git clone https://github.com/rwightman/gen-efficientnet-pytorch
    cd ./geffnet
    pip install .
    
## Train:
    I used fast ai with geffnet to fine tune the model.
    You can choose suitable model from geffnet README.md
    
    train.ipynb
    
    WARNING : If you use Fast-ai to save model weight and want to do pytorch mobile, that may occur some problem, but I don't know the reason!
    
## Pytorch-Mobile
    If you want to apply on mobile you need to change model.pth -> model.pt 
    
    mobile.ipynb

## Mobile
    I use PyTorch Android Examples for classification 
    git clone https://github.com/pytorch/android-demo-app
    Use Android Studio to build PyTorchDemoApp
    
    Follow Pytorch turtorial
    Put your model.pt to ./PyTorchDemoApp\app\src\main\assets and delete other .pt
    Open PyTorchDemoApp in Android Studio
    
    Constants.java : you need to follow your training classes to change the name
    VisionListActivity.java : line 18 change name to your model name (model.pt)
    
    Run in your Mobile 
    Finish!!!
    
    
