# Initialize system with a Yubikey

How to decrypt a file using a Yubikey if the key is not configured on the system:

```
rm -rf ~/.gnupg
gpg --import < gnupg-pubkey.txt
gpg --card-status
```

# Encrypt a file using GnuPG

```gpg -z0 --output encrypted-file.txt.gpg --encrypt --recipient "John Smith" original-file.txt```

# Decrypt a file using GnuPG

```gpg --output original-file.txt --decrypt encrypted-file.txt.gpg```
