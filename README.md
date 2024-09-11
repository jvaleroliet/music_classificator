# music_classificator
Music classificator with pytorch.

## 1. Data Collection


The first jupyter will generate this structure:


``` 
songs/
├── psytrance/
│   ├── preview_1.mp3
│   ├── preview_2.mp3
│   └── ...
├── house/
│   ├── preview_1.mp3
│   ├── preview_2.mp3
│   └── ...
├── dubstep/
│   ├── preview_1.mp3
│   ├── preview_2.mp3
│   └── ...
├── hardcore_breaks/
│   ├── preview_1.mp3
│   ├── preview_2.mp3
│   └── ...
└── techno/
    ├── preview_1.mp3
    ├── preview_2.mp3
    └── ...
```

You can try with your own data if you structure the folders like this.

## Model

First approach: to finetune resnet18 form the spectograms. With the fast-retrieved dataset and without doing finetuning the accuracy of the model on the evaluation set is 0.648649, pretty good for the time needed to construct everything.

Next step: Finetune wav2vec.
