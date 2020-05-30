# VS Codeとマークダウン
## プレビュー表示
https://www.atmarkit.co.jp/ait/articles/1804/20/news030.html

表示させるものがないと動かないけど、ctlr+K, v

## リンクの貼り付け
参考

https://qiita.com/kamorits/items/6f342da395ad57468ae3
https://www.it-swarm.dev/ja/hyperlink/%E3%83%9E%E3%83%BC%E3%82%AF%E3%83%80%E3%82%A6%E3%83%B3%E6%A7%8B%E6%96%87%E3%82%92%E4%BD%BF%E7%94%A8%E3%81%97%E3%81%A6%E3%83%AD%E3%83%BC%E3%82%AB%E3%83%AB%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%81%AB%E3%81%A9%E3%81%AE%E3%82%88%E3%81%86%E3%81%AB%E3%83%AA%E3%83%B3%E3%82%AF%E3%81%97%E3%81%BE%E3%81%99%E3%81%8B%EF%BC%9F/1055695526/
```
[タイトル](URL)
```
ローカルの場合は、(./folder/file)でいける

# anaconda 仮想環境の構築
[anaconda_prompt履歴](./memo_files/仮想環境作成_anaconda_prompt.txt)

## 仮想環境を作る
https://qiita.com/ozaki_physics/items/985188feb92570e5b82d

仮想環境の閲覧
```
conda info -e
```

python3.6の環境構築
```
conda create -n 環境名 python=3.6
```

仮想環境の起動
```
(conda) activate 環境名
```
condaを入れないと動くときと動かない時がある

## jupyter notebookを入れる(pip base)
https://qiita.com/mzmiyabi/items/b1677e66474933d9a6fc

pipの状態を最新に更新
```
pip install --upgrade pip setuptools
```
エラーがでた
```
(py36) PS C:\Users\Pump PC> pip install --upgrade pip setuptools
Collecting pip
  Downloading pip-20.1.1-py2.py3-none-any.whl (1.5 MB)
     |████████████████████████████████| 1.5 MB 6.4 MB/s
Collecting setuptools
  Downloading setuptools-47.1.1-py3-none-any.whl (583 kB)
     |████████████████████████████████| 583 kB 6.4 MB/s
Installing collected packages: pip, setuptools
  Attempting uninstall: pip
    Found existing installation: pip 20.0.2
    Uninstalling pip-20.0.2:
      Successfully uninstalled pip-20.0.2
ERROR: Could not install packages due to an EnvironmentError: [WinError 5] アクセスが拒否されました。: 'C:\\Users\\PUMPPC~1\\AppData\\Local\\Temp\\pip-uninstall-roxcbls5\\pip.exe'
Consider using the `--user` option or check the permissions.
```
--userを追加して対処（エラーが出た場合は行う）
```
pip install --upgrade pip setuptools --user
```
うまくいった。
```
(py36) PS C:\Users\Pump PC> pip install --upgrade pip setuptools --user
Requirement already up-to-date: pip in c:\users\pump pc\anaconda3\envs\py36\lib\site-packages (20.1.1)
Collecting setuptools
  Using cached setuptools-47.1.1-py3-none-any.whl (583 kB)
Installing collected packages: setuptools
  WARNING: The scripts easy_install-3.6.exe and easy_install.exe are installed in 'C:\Users\Pump PC\AppData\Roaming\Python\Python36\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed setuptools-47.1.1
```
必要パッケージを入れる
```
pip install numpy scipy matplotlib Pillow ipython[all]
```
いざインストール
```
pip install jupyter
```

## さらにパッケージを追加
opencv 
```
pip install opencv-python
```

pytorch
```
pip install torch==1.3.0+cpu torchvision==0.4.1+cpu -f https://download.pytorch.org/whl/torch_stable.html

```
確認
```
import torch

print(torch.__version__)
```
# PyTorchによる発展ディープラーニングの本
git: 
https://github.com/k-ashigaki/pytorch_advanced

ローカルclone: 
```C:\Users\Pump PC\Documents\GitHub\pytorch_advanced```

