# Kivy-Environment
This document describes step by step to prepare the [**Kivy**](https://kivy.org) Environment on SO Ubuntu 16

## Install Dependencies ##
```sh
$ sudo apt-get update && sudo apt-get upgrade
```
```sh
$ sudo apt-get install -y python-pip python3-pip build-essential git python python3 python-dev python3-dev libsdl2-dev  libsdl2-image-dev libsdl2-mixer-dev libsdl2-ttf-dev libportmidi-dev libswscale-dev libavformat-dev libavcodec-dev zlib1g-dev ffmpeg
```
If `ffmeg` installation fail, do:
```sh
$ sudo apt-get install libav-tools
```

## Python Virtual Environment ##
**Install Python Virtual Environment** - We will use [**pipenv**](https://docs.pipenv.org/) but feel free to use [**venv**](https://docs.python.org/3/library/venv.html#module-venv), [**virtualenv**](https://virtualenv.pypa.io/en/stable/) or [**virtualenvwrap**](https://virtualenvwrapper.readthedocs.io/en/latest/).

Install pipenv: 
```sh
$ sudo pip install pipenv
```

In your _project directory_, create Python3 Virtual Enviroment: 
```sh
$ pipenv --three
```
Install [**Cython**](http://cython.org/). **Warning:** [**See correct version reference in Kivy documentation**](https://kivy.org/doc/stable/installation/deps-cython.html).
```sh
$ pipenv install Cython==0.25
```
## Install Kivy ##
```sh
$ pipenv install kivy
```
Check kivy version:
```sh
$ pipenv run python
```
```py
import kivy
print(kivy.__version__)
```
[**See installation on Linux in Kivy Documentation**](https://kivy.org/docs/installation/installation-linux.html)
