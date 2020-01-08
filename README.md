# お試し

#### １、localhost:8080で立ち上げる
```
php artisan serve --port=8080
```

<br>

#### ２、ユーザー作成
http://localhost:8080/registerで、ユーザーを作成。

<br>

#### ３、クライアントアプリを登録
OAuth Clientsの「Create New Client」ボタンでクライアントを登録。

「Name」は自由に。「Redirect URL」を
```
http://localhost:8000/login/passport/callback
```
にする。

<br>

#### ４、クライアントアプリ側の.envファイルに、登録した情報を記入
「Client ID」と「Secret」を、[クライアントアプリ(Laravel\-passportでログインさせる側)](https://github.com/tobibako45/laravel-socialite-practice)の「.env」に記入。
```
PASSPORT_ID=<登録したクライアントID>
PASSPORT_SECRET=＜登録したクライアントsecret＞
```


<br>

#### ５、クライアントアプリ側を立ち上げてログイン
[クライアントアプリ(Laravel\-passportでログインさせる側)](https://github.com/tobibako45/laravel-socialite-practice)を、
```
php artisan serve
```
で立ち上げる。

```
http://localhost:8000
```
にアクセスして、「Laravel-Passportでログインする」からログイン。
