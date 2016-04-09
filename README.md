# alliance-broadband-auto-reconnect
Automatically Reconnects Alliance Broadband (Kolkata) Connection on Linux / Mac OSX

Copy the ca (stands for Connect Alliance) to a directory in your path like /usr/bin. In some installations in ~/bin works too. You can anyways add any directory to your $PATH in `~/.bashrc` file.

Make ca executable with:
`chmod 755 ca`

Opn the file ca and make the following changes:
- Replace **Login Name** with your name as shown after Welcome post login.
- Replace **user_name** with the Username provided by Alliance. 
- Replace **password** with the Password provided by Alliance.

Save it and run to test:
ca

Now add it to crontab with crontab -e:
`* * * * * /absolute/path/to/ca >/dev/null 2>&1`

This run ca every minute which reconnects only if required

