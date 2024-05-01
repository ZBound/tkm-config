# tkm-config

self-use collection of mpv config files.

### Credits

- [dyphire/mpv-config](https://github.com/dyphire/mpv-config)
- [hooke007/MPV_lazy](https://github.com/hooke007/MPV_lazy)

### Input

Q：单击左键无操作 双击左键暂停播放 怎么改

A：\mpv\input.conf  16,17行替换成这两个
```
MBTN_LEFT           ignore
MBTN_LEFT_DBL    cycle pause;script-message-to uosc flash-pause-indicator
```
删除 \mpv\inputevent_key.conf 最底下这两行
```
MBTN_LEFT       cycle pause;script-message-to uosc flash-pause-indicator  #@click
MBTN_LEFT       cycle fullscreen                                                           #@double_click
```