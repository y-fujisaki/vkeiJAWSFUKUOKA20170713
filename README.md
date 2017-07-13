# ヴィジュアル系カレンダー取得
## 概要
2017年07月13日のJAWS-UG福岡@集団山見せとAWS Summit Tokyo振り返らNight#5の発表で利用したソースです。
https://jaws-ug-kyushu.doorkeeper.jp/events/62480

【Serverless Frameworkで気軽にAPIを公開してみる？(Python3.6編)】

#### 2017年07月13日<br>
#### JAWS-UG福岡@集団山見せとAWS Summit Tokyo振り返らNight#5

201707

## リポジトリのclone
```
git clone https://github.com/y-fujisaki/vkeiJAWSFUKUOKA20170713.git
```


## serverless-python-requirementsインストール
* PGで必要なPythonパッケージリスト(requirements.txt)をデプロイ時のパッケージに含めるプラグイン

```
npm install --save serverless-python-requirements
```

## Serverless Frameworkでデプロイ
```
# デプロイ
sls deploy -v 

# 作成されたLambda関数を実行
sls invoke -f calendar
```

## 取れるJSON例
```
 [
    [
      "date",
      "2017-8-3"
    ],
    [
      "artist",
      "C4"
    ],
    [
      "title",
      " ULTIMATE BEST   ALBUM [-S A G A-]  "
    ],
    [
      "media",
      "CD"
    ],
    [
      "price",
      "¥3,800"
    ]
  ]
```

## Serverless Framework環境構築参考HP

http://dev.classmethod.jp/cloud/aws/easy-deploy-of-lambda-with-serverless-framework/