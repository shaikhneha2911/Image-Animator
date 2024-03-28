# Motion Representations for Articulated Animation

This repository contains the source code for the CVPR'2021 paper [Motion Representations for Articulated Animation](https://arxiv.org/abs/2104.11280) by [Aliaksandr Siarohin](https://aliaksandrsiarohin.github.io/aliaksandr-siarohin-website/), [Oliver  Woodford](https://ojwoodford.github.io/), [Jian Ren](https://alanspike.github.io/), [Menglei Chai](https://mlchai.com/) and [Sergey Tulyakov](http://www.stulyakov.com/). 

## Example animation

Here is an example of several images produced by the method. In the first column, the driving video is shown. For the remaining columns, the top image is animated by using motions extracted from the driving. 

![Screenshot](sup-mat/teaser.gif)

### YAML configs

There are several configuration files one for each `dataset` in the `config` folder named as ```config/dataset_name.yaml```. See ```config/dataset.yaml``` to get the description of each parameter.

See the description of the parameters in the ```config/vox256.yaml```, adjusted the configuration to run on 1 V100 GPU, training on 256x256 dataset takes approximately 2 days.

### Pre-trained checkpoints
Checkpoints can be found at https://drive.google.com/drive/folders/1jCeFPqfU_wKNYwof0ONICwsj3xHlr_tb?usp=sharing.

### Animation Demo
To run a demo, download a checkpoint and run the following command:
```bash
python demo.py  --config config/dataset_name.yaml --driving_video path/to/driving --source_image path/to/source --checkpoint path/to/checkpoint
```
The result will be stored in ```result.mp4```. To use Animation via Disentaglemet add ```--mode avd```, for standard animation add  ```--mode standard``` instead.

### Colab Demo 
A demo runnable in google-colab, see: ```demo.ipynb```.

#### Additional notes

Citation: 
```
@inproceedings{siarohin2021motion,
        author={Siarohin, Aliaksandr and Woodford, Oliver and Ren, Jian and Chai, Menglei and Tulyakov, Sergey},
        title={Motion Representations for Articulated Animation},
        booktitle = {CVPR},
        year = {2021}
}
```

