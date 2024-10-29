# gpg_msg
**A simple facade for encryption + signing/decryption data to a recipient with extra nifty utilities. Ideal for the workplace!**

<ins>*This script has ONLY been tested and developed for Mac/Linux.*</ins>  

I actively encrypt/decrypt files with GPG at work, though always forget the commands for the process.Thus, I made this very simple _gpg_msg_ bash script.
...Emphasis on the simple part: Features such as batch encryption, specific compression techniques etc. are omitted here. In this case, refer to the [gpg documentation](https://www.gnupg.org/documentation/manuals/gnupg24/gpg.1.html). 

This implementation is just intended for simple cryptography tasks, ensuring armoring, signatures etc. are by default enabled, benefitting from the security of GPG (If you're forgetful, lazy or just ensure consistency.

## Setup (Recommended)
Although there is no real setup (besides sharing each other's public keys), it is recommended to set it up as an alias in your zsh/bash configuration file:

1. Move the script to your bin folder: ```sudo mv gpg_msg.sh /usr/local/bin/gpg_msg```
2. Add an alias (can be anything, but I named it "gpgmsg": ```echo 'alias gpgmsg="gpg_msg"' >> ~/.zshrc```
3. Done!

## To encrypt and sign

for a file:
```gpgmsg encrypt <RECIPIENT> <FILE_TO_ENCRYPT>```

for clipboard:
```gpgmsg pb_encrypt <RECIPIENT>```

## To decrypt

for a file: 
```gpgmsg decrypt <FILE_TO_DECRYPT>```

for clipboard:
```gpgmsg pb_decrypt```
