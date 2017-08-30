# AAIC Gathering

## 2017年度

* 第1回(2017年5月31日) AAICユーザ説明会
* [第2回(2017年8月31日) ChainerMN](https://github.com/htsst/aaic_gathering/tree/master/2)

## 注意事項

この資料の大部分はAAICなど共有計算機上でJupyter Notebookで動作するように設計されています。
共有計算機へログインし、

```
$ pip install jupyter
$ pip install bash_kernel
$ python -m bash_kernel.install
```
としてインストールした後、
```
$ jupyter notebook --ip='*' --port=8888 --no-browser
```
と実行します。この際、出力されるポート番号とトークンを記録します。
```
[C 10:59:05.646 NotebookApp] 
    
    Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://localhost:<ポート番号>/?token=<トークン>
```
その後、ログイン元のローカルな計算機から以下のコマンドを実行し、
```
$ ssh -L 9999:localhost:<ポート番号> <ユーザ名>@<共有計算機名> -Y
```
以下のリンクをクリックします。<br>
http://localhost:9999 

トークンを要求されたら入力をしてください。
上記の記述がよくわからない場合は、コマンドラインを介して実行してください。
また、共有計算機上のjupyterプロセスは終了後には必ず停止させてください。
