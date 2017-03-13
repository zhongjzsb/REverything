# Setup in Mac.
* Get an account from [pushbullet](https://www.pushbullet.com).
* Find the *Access Tokens* from the __account setting__ page.
* Type in your terminal 
```
 curl --header 'Access-Token: <your_access_token_here>' \
     https://api.pushbullet.com/v2/users/me 
```
* Get the results something like
```
{
  "created": 1.381092887398433e+09,
  "email": "elon@teslamotors.com",
  "email_normalized": "elon@teslamotors.com",
  "iden": "ujpah72o0",
  "image_url": "https://static.pushbullet.com/missing-image/55a7dc-45",
  "max_upload_size": 2.62144e+07,
  "modified": 1.441054560741007e+09,
  "name": "Elon Musk"
}
```
* Create one _.rpushbullet.json_ in your home directory with
```
{
  "key": <your_access_token_here>,
  "created": 1.381092887398433e+09,
  "email": "elon@teslamotors.com",
  "email_normalized": "elon@teslamotors.com",
  "iden": "ujpah72o0",
  "image_url": "https://static.pushbullet.com/missing-image/55a7dc-45",
  "max_upload_size": 2.62144e+07,
  "modified": 1.441054560741007e+09,
  "name": "Elon Musk"
}
```
* install [RPushbullet](http://dirk.eddelbuettel.com/code/rpushbullet.html) in R.
```
install.package("RPushbullet")
```
* Test the RPushbullet with
```
pbPost("note", "A simple title", "A message\nWith a second line")
```

# References
* [Github](https://github.com/eddelbuettel/rpushbullet)
* [Dirk Eddelbuettel](http://dirk.eddelbuettel.com/code/rpushbullet.html)
* [Pushbullet](https://www.pushbullet.com) 

