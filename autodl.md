# 1.租用GPU 
选的autodl 2080ti GPU

```bash
git clone https://github.com/nota-github/AIC2024_Track1_Nota.git
```

然后把val的第一个场景上传测试scene_041
```bash
AIC2024_Track1_Nota
└── data
    └── videos
        ├── val
        │   ├── scene_041

```
 
提取图片
```bash
conda install ffmpeg
bash scripts/generate_only_frames.sh
```

```bash
# Install xtcocotools
pip install cython xtcocotools

# Install MMEngine and MMCV
pip install openmim
mim install mmengine "mmcv>=2.0.0"


# Install MMPose
#如果有问题，执行：
#conda clean --all
git clone https://github.com/open-mmlab/mmpose.git /mmpose
cd /mmpose
git checkout main
不执行 ENV FORCE_CUDA="1"
pip install -r requirements/build.txt
pip install --no-cache-dir -e .


mim install mmdet==3.0.0
pip3 install matplotlib \
                scipy \
                Pillow \
                numpy<=1.19\
                prettytable \
                easydict \
                scikit-learn \
                pyyaml \
                yacs \
                termcolor \
                tabulate \
                tensorboard \
                opencv-python \
                pyyaml \
                yacs \
                termcolor \
                scikit-learn \
                tabulate \
                gdown \
                faiss-gpu \
                lap \
                cython-bbox
pip3 install ultralytics



```

直接使用他训练好的模型：
https://drive.google.com/drive/folders/1f9vTZA336qr9JL8nPbA9fmH5hVU8rcuJ?usp=sharing
下载后放到 ./pretrained文件夹里

# Reproduce MCPT Results
```bash
bash scripts/run_mcpt.sh
```
修改eval_mcpt.py第28行
修改trackers/multicam_tracker/cluster_track.py第153行
修改trackers/multicam_tracker/clustering.py第27行
