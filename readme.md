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
pip install cython
pip install xtcocotools




```
