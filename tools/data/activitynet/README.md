## Method 1: Crawl videos from YouTube
Follow the steps below to download videos from YouTube. (Code is adapted from the [official crawler](https://github.com/activitynet/ActivityNet/tree/master/Crawler/Kinetics).) Note that some videos are no longer available on YouTube. To download the full dataset, use Method 2.

1. Download annotation [here](https://github.com/activitynet/ActivityNet/blob/master/Evaluation/data/activity_net.v1-3.min.json) and put it in `PROJECT/data/ActivityNet/`.

2. Set up environment
```shell
conda env create -f environment.yml
source activate activitynet
pip install mmcv
pip install tqdm
```

Install the latest youtube-dl from github (`pip install` would not work, see this [issue](https://github.com/ytdl-org/youtube-dl/issues/31530)).
```shell
pip install --upgrade --force-reinstall "git+https://github.com/ytdl-org/youtube-dl.git"
```

3. Download videos from youtube.
```shell
python download.py
```

4. Clean up.
```shell
source deactivate activitynet
conda remove -n activitynet --all
```

References
- https://github.com/activitynet/ActivityNet/tree/master/Crawler
- https://github.com/open-mmlab/mmaction2/tree/main/tools/data/activitynet


## Method 2: Download from Google Drive
The official organizers have made the full dataset available on Google Drive (see [here](https://github.com/activitynet/ActivityNet/tree/master/Crawler#missing-data-requests) and [here](http://activity-net.org/download.html)). Fill in this [form](https://docs.google.com/forms/d/e/1FAIpQLSeKaFq9ZfcmZ7W0B0PbEhfbTHY41GeEgwsa7WobJgGUhn4DTQ/viewform) to request access. (I requested on Sep 27, 2024, and received access after 1 day.)
