# bbssh

Shim to adapt OpenSSH to work with Qodem usernames and passwords stored 
in your dialing directory.

Note that storing usernames and passwords in Qodem is a terrible idea 
from a security perspective, and you should at least chmod 600 your 
`fonebook.txt` file to prevent other users stumbling across your passwords.

PASSWORDS STORED IN QODEM ARE NOT SECURE. YOU HAVE BEEN WARNED

That said, here's how you ignore my warning and enable Qodem to use 
OpenSSH with stored passwords.

## Usage

Place bbssh in the path somewhere and comment out bbs_user in 
`~/.qodem/qodemrc` and add this line instead.

`ssh_user = bbssh $USERNAME $REMOTEHOST $REMOTEPORT`


