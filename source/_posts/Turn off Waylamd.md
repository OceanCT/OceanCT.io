---
title: Turn off Wayland on Ubuntu
date: 2022-07-31 10:05:52
tags: Ubuntu
categories: Ubuntu Settings
---
# Why I have to turn off Wayland?

In fact, wayland is great. Unfortunately, the "Wemeet"(Tencent meeting) don't support wayland.

# How?

```shell
sudo vi /etc/gdm3/custom.conf
```
find "#WaylandEnable=false", change it to "WaylandEnable=false".
```shell
sudo service gdm3 restart
```

You may have to wait for a moment. Don't try to turn off your computer manually.