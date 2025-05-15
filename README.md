環境構築方法：
バックエンド
npm i -g @nestjs/cli　　　　＃nestjsのインストール

cd backend
npm i @nestjs/graphql @nestjs/apollo @apollo/server graphql    #GraqhQLのインストール

npm run start :dev    #GraphQLサーバーの立ち上げ

http://localhost:3000/graphql    #GraphQL playground 

npm i class-validator class-transformer   #バリデーションを行うためのライブラリインストール

------------------------------------------------------------------------------------
データベース
docker-compose up -d   　　 #コンテナ起動

docker exec -it postgres psql -U  udemy_user udemydb　＃データベース接続の確認

-------------------------------------------------------------------------------------
Prismaのセットアップ
npm install prisma --save-dev 　　　#Prismaインストール

npx prisma init     #初期セットアップ

DATABASE_URL="postgresql://<dbのユーザ名>:<password>@localhost:<ポート番号>/udemydb?schema=public"＃.envファイルの修正

npx prisma studio　　　　＃prisma studioの起動

npm i @prisma/client   #prisma clientのインストール

-------------------------------------------------------------------------------------------------------------------------
認証機能
npm i @nestjs/passport passport passport-local
npm i --save-dev @types/passport-local　　　　　　＃ローカル認証を行うためのライブラリのインストール

npm i @nestjs/jwt passport-jwt  
npm i --save-dev @types/passport-jwt        #jwtに必要なライブラリのインストール

JWT_SECRET="jwt@secret#key"                 #.envファイルの修正(jwt鍵の設定)

-----------------------------------------------------------------------------------------------------------------
フロントエンド
cd frontend 
npm install 
npm run dev    　　　　　　　#Reactの起動

npm i modern-css-reset　　 ＃ブラウザ間のCSSの差分を無くすためのライブラリ　

npm install @mui/material @emotion/react @emotion/styled　　 
npm i @mui/icons-material　 ＃CSS関連のライブラリ

npm i react-router-dom　　 ＃ルーディングを実装するためのライブラリ

npm i @apollo/client graphql    #ReactからGraphQLを扱うためのライブラリ

npm i jwt-decode　　　　　　　＃backendから受け取ったtokenのdecodeを行うためのライブラリ

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
