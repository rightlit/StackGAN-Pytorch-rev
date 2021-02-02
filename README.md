# StackGAN-Pytorch revision for Colab

This is StackGAN-Pytorch revised version for Google Colab.

Refer to [https://github.com/hanzhanggit/StackGAN-Pytorch](https://github.com/hanzhanggit/StackGAN-Pytorch) for original source version,<br>
it is implementation for the paper [StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks](https://arxiv.org/pdf/1612.03242v1.pdf).

Refer to troubleshooting [issues](https://github.com/rightlit/StackGAN-Pytorch-rev/issues) while running with original source 


### Dependencies
python == 3.6

pytorch == 1.2

Torch7 (http://torch.ch/docs/getting-started.html#_)

In addition, please add the project folder to PYTHONPATH and `pip install` the following packages:
- `torchfile`
- `lupa`
- `scipy==1.1.0`
- `torchvision==0.4.0`



**Data**

1. Download preprocessed char-CNN-RNN text embeddings for [training coco](https://drive.google.com/open?id=0B3y_msrWZaXLQXVzOENCY2E3TlU) and  [evaluating coco](https://drive.google.com/open?id=0B3y_msrWZaXLeEs5MTg0RC1fa0U), save them to `data/coco`.
  - [Optional] Follow the instructions [reedscot/icml2016](https://github.com/reedscot/icml2016) to download the pretrained char-CNN-RNN text encoders and extract text embeddings.
2. Download the [coco](http://cocodataset.org/#download) image data. Extract them to `data/coco/`.



**Evaluating**
- Run `python main.py --cfg cfg/coco_eval.yml --gpu 2` to generate samples from captions in COCO validation set.

Examples for COCO:
 
![](examples/coco_2.png)
![](examples/coco_3.png)



**References**

- Generative Adversarial Text-to-Image Synthesis [Paper](https://arxiv.org/abs/1605.05396) [Code](https://github.com/reedscot/icml2016)
- Learning Deep Representations of Fine-grained Visual Descriptions [Paper](https://arxiv.org/abs/1605.05395) [Code](https://github.com/reedscot/cvpr2016)
