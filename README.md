dbは、postgres。詳細は./config/database.yml参照  
username: rails  
password: password  

### dbを作成  
```  
rails db:schema:load
```  

### dbへ初期データ投入  
```  
rails db:seed
```  

### Railsアプリ立ち上げ  
```  
rails s
```  

### heroku への push

```
  heroku login
     * windows環境では、gitbashなどでのログインがうまく行かなかったため、cmdでheroku loginを行った
  heroku git:remote -a omoide-falk
     * herokuでは予め「omodie-falk」アプリケーションを作成しておく
  git push heroku master
  heroku run:detached rake db:schema:load
  heroku run:detached rake db:seed
```
