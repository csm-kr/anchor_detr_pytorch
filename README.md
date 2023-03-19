# ANCHOR DETR pytorch

re-implementation of anchor detr
Please refer to https://arxiv.org/abs/2109.07107
 
### Properties of this repo.
- Use our DETR repo (https://github.com/csm-kr/detr_pytorch) as baseline
- Paper claims that due to the query design, detr converges fast.
- Implementation new query design

### Training Setting
```
- batch size : 36 (official - 64)
- optimizer : Adamw
- epoch : 50
- lr : 1e-4 
- weight decay : 1e-4
- scheduler : step LR (*0.1 at epoch 40)
```

### Results

- quantitative results

|methods        | Traning Dataset        |    Testing Dataset     | Resolution.  | AP               |
|---------------|------------------------| ---------------------- | ------------ | ---------------- |
|papers         | COCOtrain2017          |  COCO val2017(minival) | 800 ~ 1333   | 42.0 (500 epoch) |
|this repo      | COCOtrain2017          |  COCO val2017(minival) | 1024 x 1024  | 41.1 (300 epoch) |

- qualitative reusults

![results](https://user-images.githubusercontent.com/18729104/221108742-09ded1a8-dcf2-41df-9485-b659e3b6ca08.png)
