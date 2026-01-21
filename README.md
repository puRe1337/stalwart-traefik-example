# Stalwart Setup with Traefik
I created this repo since I get more comments on my gist [here](https://gist.github.com/puRe1337/cdecc97307cc19c6d899a204b510834e). Feel free to open an Issue to ask something or share your thoughts.

# Test commands with openssl

### SMTP 25
`openssl s_client -quiet -crlf -starttls smtp -connect mail.example.com:25`
### SMTP 587
`openssl s_client -starttls smtp -quiet -crlf -connect mail.example.com:587`
### SMTP 465
`openssl s_client -quiet -crlf -connect mail.example.com:465`
### IMAP 143
`openssl s_client -crlf -connect mail.example.com:143 -starttls imap -servername mail.example.com`
### IMAP 993
`openssl s_client -quiet -crlf -connect mail.example.com:993`
### SIEVE 4190
`openssl s_client -showcerts -servername mail.example.com -connect mail.example.com:4190`
### JMAP 443
`curl -iL -u admin:'password' https://mail.example.com/.well-known/jmap`
