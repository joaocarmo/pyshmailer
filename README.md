# PyShMailer

A simple CLI tool to send emails using Python 3, because the End of Life (EOL)
for Python 2.7 is coming January 1, 2020.

## Install

```bash
pip install -r requirements.txt
```

## Configuration

Use a `YAML` file with the following structure.

```yaml
---  # config start

#################
# Mailer Config #
#################

smtp_server:
  plain: 'mail.server.com'
  base64: ''
smtp_user:
  plain: 'username@server.com'
  base64: ''
smtp_pass:
  plain: 'password'
  base64: ''

proxy:
  user: 'fake-user@hostname.com'
  host: '127.0.0.1'
  port: 1080
  type: 'socks5'

...  # config end
```

## Usage

A simple example.

```bash
./pyshmailer -to janedoe@server.com -from "John Doe <johndoe@server.com>" -s
"Hello, there !" -m "Hi, this is John. Long time no see!"
```
