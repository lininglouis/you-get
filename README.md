# You-Get
## 原始repo: https://github.com/soimort/you-get

## 改进

Here's how you use `you-get` to download a video from bilibili

```console
$ you-get https://www.bilibili.com/video/BV1PJ411g7S9 -O myvide
site:                Bilibili
title:               【木鱼微剧场】18天拍摄，120万预算，却拍出了本世纪豆瓣评分最高的恐怖片《电锯惊魂》
stream:
    - format:        dash-flv
      container:     mp4
      quality:       高清 1080P
      size:          425.5 MiB (446205490 bytes)
    # download-with: you-get --format=dash-flv [URL]
```

设定-O参数的情况下
原始youget的repo，会将视频存储为myvide.mp4，但是弹幕cmt.xml文件，仍然按照title存储，这个例子里面title就会存成下面这样，导致视频名和弹幕文件不一致。
```
视频名：myvideo.mp4
弹幕文件名: 【木鱼微剧场】18天拍摄，120万预算，却拍出了本世纪豆瓣评分最高的恐怖片《电锯惊魂》.cmt.xml
```

我的改进是指定-O的话，存储的视频文件名和弹幕网文件名是一致的。 如下
```
myvideo.mp4
myvideo.cmt.xml
```
