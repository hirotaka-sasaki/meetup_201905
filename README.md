# meetup_201905

## 環境
- ruby 2.5.3
- bundler 2.0.1
- MySQL 5.6系(5.7系でも多分動きます)

## 設定方法
### cloud9を使う場合
- cloud9 にアクセス(https://ap-northeast-1.console.aws.amazon.com/cloud9/home/product)
- 「Create environment」をクリックして environment を作成(初期設定のままでよい)

### 自身のローカル環境を使う場合はこちらから
- `git clone https://github.com/hirotaka-sasaki/meetup_201905.git` で手元にクローンする
- クローンしたアプリケーションのディレクトリに移動(`git clone`を叩いた場所で、`cd meetup_201905`)
- `bundle install` で必要な gem をインストール
- `rails db:create` でデータベースを作成
- `rails db:migrate` でデータベースにテーブル作成
- `rails s` でサーバーを立ち上げる
- `http://localhost:3000` にアクセスする(cloud9の場合は、「Preview」 → 「Preview Running Application」を押す)

### こんな場合はどうする？
#### bundlerのバージョンで怒られる場合
`gem install bundler -v '2.0.1'`を叩いて、指定のバージョの bundler を入れましょう
#### cloud9 で mysql2 がうまくインストールできない場合
以下2つのコマンドを叩いてください

```
sudo yum install mysql-devel
sudo service mysqld start
```

## 作業方法
- `git checkout -b issue_issueのID` でブランチを切る
- 作業を終えたら git で commit と push
- push をしたら、master ブランチに向けて Pull request を立てて連絡してください
