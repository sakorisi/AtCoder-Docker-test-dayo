# AtCoderの環境構築をDockerで行うテスト

主に、個人用です。


## 使い方

### 1. ファイルのダウンロード、または、クローンを行います。
下はクローンする場合です。
```
git clone https://github.com/sakorisi/AtCoder-Docker-test-dayo.git
```
以降、"./AtCoder-Docker-test-dayo/"ディレクトリにいる想定です。

### 2. サービスを上げます。
よいしょ。

初回
```
docker-compose up --build -d
```

2回目以降
```
docker-compose up -d
```

### 3. コンテナに入ります。
```
docker-compose exec atcoder bash
```

### 4. ファイルを実行します。(例)
test.cpp と test.py を実行する例です。

```
cd src

g++ -std=c++20 test.cpp
./a.out

python test.py
```

### 5. サービスを下げます。
停止とも言います。
```
exit

docker-compose down
```


## 参考文献
有り難い資料。

[AtCoder の環境を Docker で作りたい](https://qiita.com/tf63/items/c93c6f24d73599e637d8)

[DockerでAtCoderができる環境を作る【Python・C++】](https://qiita.com/hinamimi/items/b3dd159f956628cebdbb)
