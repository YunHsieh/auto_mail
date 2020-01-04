# Auto send mail simple model

```python
from mail_module import SendMail
```

Set user config for example:
```python
user_config = {}
user_config['userid'] = '{user account}'
user_config['userpw'] = '{user password}'
user_config['smtp_server'] = 'gmail'
```
or
```python
user_config = {}
user_config['userid'] = '{user account}'
user_config['userpw'] = '{user password}'
user_config['smtp_server'] = ['smtp.gmail.com', 587]
```


Setting content for mail to target:
```python=
send_content = {}
send_content['mail_target'] = ['{email account}']
send_content['cc_id'] = ['{email account}']
send_content['subject'] = '{Mail subject}'
send_content['attached'] = [{filePath}]
send_content['msg'] = u"""Hi Sir,
<br><br><b> HELLO WORLD! </b><br><br> 
Best Regards,
"""
```
Msg is reading the HTML.


Run to function

```python
try:
    send_mail.sendEmail(**send_content)
except Exception as e:
    print(e)
finally:
    send_mail.close()
```