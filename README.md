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
if you wanna plot loss, pandas is needed for aggregate csv.

```sh
pip install torch torchaudio lightning pandas
```

# Result

WIP