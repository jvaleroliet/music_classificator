# music_classificator
Music classificator with pytorch.

Clone the repo:

```
git clone https://github.com/jvaleroliet/music_classificator.git
```

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

You need a [spotify api](https://developer.spotify.com/documentation/web-api) secret and client. 

You can try with your own data if you structure the folders like this and go directly to the second notebook.

## Model

First approach: to finetune resnet18 form the spectograms. With the fast-retrieved dataset and without doing finetuning the accuracy of the model on the evaluation set is 0.648649, pretty good for the time needed to construct everything.

Next step: Finetune wav2vec.
