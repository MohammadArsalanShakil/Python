import smtplib

sender = "YOUR_EMAIL_ADDRESS"
password = "YOUR_PASSWORD"
reciever = ["RECIEVER_EMAIL"]

SUBJECT = "EMAIL_SUBJECT"
TEXT = "EMAIL_BODY"

message = """From: %s\r\nTo: %s\r\nSubject: %s\r\n\

%s
""" % (sender, ", ".join(reciever), SUBJECT, TEXT)

for recipient in reciever:
    try:
        # s = smtplib.SMTP('smtp-mail.outlook.com', 587)
        s = smtplib.SMTP('SMTP_MAIL_SERVER_ADDRESS', port=)
        s.starttls()
        s.login(sender, password)
        s.sendmail(sender, recipient, message)
        print('sending email from {} to {}'.format(sender, recipient))
    except Exception as e:
        print(e)
    finally:
        print('sent email from {} to {}'.format(sender, recipient))
        s.quit()
