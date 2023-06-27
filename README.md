# MB-HiFi-GAN

My implementation of Multi-Band HiFi-GAN for JSUT([link](https://sites.google.com/site/shinnosuketakamichi/publication/jsut)) powerd by lightning.

It is multi-band version of HiFi-GAN([paper](https://arxiv.org/abs/2010.05646)).

# Usage
Running run.sh will automatically download the data and begin training.  
So just execute the following commands to begin training.

```sh
cd scripts
./run.sh
```

synthesize.sh uses last.ckpt by default, so if you want to use a specific weight, change it.

```sh
cd scripts
./synthesis.sh
```

# Requirements

```sh
pip install torch torchaudio lightning pandas
```

# Result

Trained 1000 epochs(612000 steps) with batch_size = 16.

Pretrained model ckpt is here.
[https://huggingface.co/reppy4620/mb_hifi_gan/blob/main/jsut_1000.ckpt](https://huggingface.co/reppy4620/mb_hifi_gan/blob/main/jsut_1000.ckpt)

Some audio samples are in `asset/sample/`

| loss | plot |
| --- | --- |
| Discriminator | ![mel](./asset/loss/disc.png) |
| Generator | ![mel](./asset/loss/gen.png) |
| Feature Matching | ![mel](./asset/loss/fm.png) |
| Mel | ![mel](./asset/loss/mel.png) |
