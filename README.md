# ANCHOR DETR pytorch

re-implementation of anchor detr
Please refer to https://arxiv.org/abs/2109.07107
 
### Properties of this repo.
- Use our DETR repo (https://github.com/csm-kr/detr_pytorch) as baseline
- Paper claims that due to the query design, detr converges fast.
- Implementation new query design

### Training Setting
```
- batch size : 36 (official - 8 :  8 GPUs with 1 image per GPU)
- optimizer : Adamw
- epoch : 50
- lr : 1e-4 
- weight decay : 1e-4
- scheduler : step LR (*0.1 at epoch 40)
```

### Results

- quantitative results

- qualitative reusults
