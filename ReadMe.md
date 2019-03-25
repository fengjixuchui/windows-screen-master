### 介绍

该程序实现windows的录屏，投屏功能。

- 屏幕复制

![1553494000066](./pic/1553494000066.jpg)

- 拓展屏投屏

  拓展屏是使用一款软件开启的一个虚拟屏幕

  ![1553494228778](./pic/1553494228778.jpg)

- 屏幕录制

  使用ffmpeg开发库，录制的视频编码格式可指定为h264或者mpeg，会在本地生成文件，使用vlc播放器即可播放，或者使用 `ffmpeg -i save.h264 -codec copy save.mp4` 

  命令转换为mp4格式。

- SDL播放器播放测试

  SDL为windows下的一个播放器，实现实时查看录制的内容。

![1553494687354](./pic/1553494687354.png)



### 编译环境

VS2017 + ffmpeg

其中我已经提供了x86平台下的ffmpeg开发库。


### 代码介绍
- MonitorMaster.cpp 
  枚举显示器，查看显示器的一些信息
- SDLMaster.cpp
  封装一个简单的SDL播放器
- ffmpegEncoder.cpp
  使用ffmpeg库实现mpeg和x264视频编码的功能
- libx264Master.cpp
  使用libx264库实现x264视频编码
- web_stream.cpp
  实现一个简单的web服务器，该服务器传输照片流形成视频（目前视频流还没有做好，因为找不到一款合适的javascript编码解码工具）
