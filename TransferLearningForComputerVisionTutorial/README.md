# official_demo_finetuning.py
Finetuning the convnet: Instead of random initializaion, we initialize the network with a pretrained network, like the one that is trained on imagenet 1000 dataset. Rest of the training looks as usual.  
使用resnet18网络的参数，将全连接层改为2个输出，然后训练

# official_demo_freeze.py
Here, we need to freeze all the network except the final layer. We need to set requires_grad == False to freeze the parameters so that the gradients are not computed in backward().  
冻结卷积层参数，将全连接层改为2个输出，只训练全连接层
