---
title: Python MDSplus
date: 2019-01-17 21:42:59
tags: Python
---
# Install MDSplus
MDSplus is the uniform data format for fusion research, however installing MDSplus package for python on linux is rather a boring work. Many bugs occurred. First you should download the MDSplus package [1]. Here is some approach to install it. The python3 has been installed on the linux. First we follow the official instruction[2].

## Install with pip
```
# Install via official MDSplus rpm packages/yum source.
# sudo yum install mdsplus-repo.rpm
# sudo yum install mdsplus
$ ~/anaconda3/bin/pip install /usr/local/mdsplus/mdsobjects/python
```

This approach will install the official MDSplus to the desired python version. But sometimes, the official MDSplus cause some error such as:

Exception: Could not load library: Mdsdcl

This kinds of bug almost makes me break down.


## Install by copying
You can also install it by coping the effective MDSplus python module to the site-package. I first copied the effective MDSplus package from my mac notebook. Then copy it to the similar location on Linux desktop.

```
mac_notebook$ cp -r ~/anaconda3/lib/python3.7/site-packages/MDSplus MDSplus_mac
linux_desktop$ cp -r MDSplus_mac ~/anaconda3/lib/python3.7/site-packages/MDSplus
```

Sometimes, there maybe some bugs with python, you can try to install the latest python from Anaconda official site.


# Reference
[1] http://www.mdsplus.org/index.php?title=Downloads&open=147569449264929046577&page=Software%2FDownloads

[2] http://www.mdsplus.org/index.php/Documentation:Users:MDSobjects:Python
