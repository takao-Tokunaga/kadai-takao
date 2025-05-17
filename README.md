環境構築方法：
バックエンド

npm i      #packageのインストール

・データベースの立ち上げ

docker-compose up -d   　　 #コンテナ起動

docker exec -it postgres psql -U  udemy_user udemydb　＃データベース接続の確認

npm run start :dev    #GraphQLサーバーの立ち上げ

http://localhost:3000/graphql    #GraphQL playground 

・Prismaのセットアップ

npx prisma init     #初期セットアップ

DATABASE_URL="postgresql://<dbのユーザ名>:<password>@localhost:<ポート番号>/udemydb?schema=public"＃.envファイルの修正

npx prisma studio　　　　＃prisma studioの起動

・認証機能

JWT_SECRET="jwt@secret#key"                 #.envファイルの修正(jwt鍵の設定)

-----------------------------------------------------------------------------------------------------------------
フロントエンド

cd frontend 

npm i      #packageのインストール

npm run dev    　　　　　　　#Reactの起動


・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・


技術スタック

API: GraphQL

バックエンド:NestJS

ORM:　prisma

DB: PostgreSQL

認証用ライブラリ：passportJS

フロントエンド:React

ルーティング:ReactRouter

CSSライブラリ:muimaterial

・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・
感想 Webアプリ開発の流れを体系的に学ぶことができた。 
途中でうまく動作しないこともあったが、その都度エラーを調べることで、より理解を深めることができた。
チーム開発においてDockerの便利さに感心しました。
今回学んだ技術を今後のWebアプリ開発に活かしていきます。
