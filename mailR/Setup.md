# Setup in Windows 10
* install mailR in R
```
install.packages("mailR")
```
when call the library, find an error same as [stackoverflow](http://stackoverflow.com/questions/37735108/r-error-onload-failed-in-loadnamespace-for-rjava). Then I change the JAVA_HOME variable by
```
Sys.setenv("JAVA_HOME"="C:\\Program Files\\Java\\jre1.8.0_121")
```


* Test it works or not
```
send.mail(from = "sender@gmail.com",
          to = c("recipient1@gmail.com", "Recipient 2 <recipient2@gmail.com>"),
          replyTo = c("Reply to someone else <someone.else@gmail.com>")
          subject = "Subject of the email",
          body = "Body of the email",
          smtp = list(host.name = "smtp.gmail.com", port = 465, user.name = "gmail_username", passwd = "password", ssl = TRUE),
          authenticate = TRUE,
          send = TRUE)
```


# References
[Github](https://github.com/rpremraj/mailR)