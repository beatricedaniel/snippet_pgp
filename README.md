# snippet_pgp

source : https://www.linuxfordevices.com/tutorials/linux/generate-pgp-keys-gnupg

## installation sur centos

sudo yum install gnupg

## création de la paire de clés

[devdata@dev-data mnt]$ gpg --gen-key
gpg (GnuPG) 2.0.22; Copyright (C) 2013 Free Software Foundation, Inc.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

gpg: directory `/home/devdata/.gnupg' created
gpg: new configuration file `/home/devdata/.gnupg/gpg.conf' created
gpg: WARNING: options in `/home/devdata/.gnupg/gpg.conf' are not yet active during this run
gpg: keyring `/home/devdata/.gnupg/secring.gpg' created
gpg: keyring `/home/devdata/.gnupg/pubring.gpg' created
Please select what kind of key you want:
   (1) RSA and RSA (default)
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
Your selection?
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (2048)
Requested keysize is 2048 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0)
Key does not expire at all
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: Beatrice DANIEL
Email address: beatrice.daniel@sg.social.gouv.fr
Comment: creating a keypair
You selected this USER-ID:
    "Beatrice DANIEL (creating a keypair) <beatrice.daniel@sg.social.gouv.fr>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? O
You need a Passphrase to protect your secret key.

We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: /home/devdata/.gnupg/trustdb.gpg: trustdb created
gpg: key CD9FCCD5 marked as ultimately trusted
public and secret key created and signed.

gpg: checking the trustdb
gpg: 3 marginal(s) needed, 1 complete(s) needed, PGP trust model
gpg: depth: 0  valid:   1  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 1u
pub   2048R/CD9FCCD5 2022-01-27
      Key fingerprint = 7FA5 F806 761F 0812 F7DE  8E27 76F1 30B8 CD9F CCD5
uid                  Beatrice DANIEL (creating a keypair) <beatrice.daniel@sg.social.gouv.fr>
sub   2048R/03AA331D 2022-01-27

[devdata@dev-data mnt]$ gpg -k
/home/devdata/.gnupg/pubring.gpg
--------------------------------
pub   2048R/CD9FCCD5 2022-01-27
uid                  Beatrice DANIEL (creating a keypair) <beatrice.daniel@sg.social.gouv.fr>
sub   2048R/03AA331D 2022-01-27
