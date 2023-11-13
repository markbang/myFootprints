# Flask

## 1. 简介

Flask 是一款轻量级的 Python Web 应用框架。

## 2. 安装

```bash
pip install Flask
```

## 3. 基本使用

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return 'Hello World!'

if __name__ == '__main__':
    app.run()
```

## 4. 路由

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')

@app.route('/user/<username>')