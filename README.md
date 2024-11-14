# link to this page/domain:

https://tatitati.github.io/rentadvisor_domain/


## deep link stuff:

Deep linking needs a sha256_cert_fingerprints
This cert fingerprint is usually obtained in play store once you have the app ready to release. However, until then, i need one to test.
To have one during the development I can produce locally one doing:


1. Create a keystore. This is a file that stores cryptographic keys, including the one I'll use to sign my app.
```
$ keytool -genkeypair -v -keystore key-rentadvisor.jks -keyalg RSA -keysize 2048 -validity 10000 -alias key-rentadisor


Enter keystore password: XXXXX
Re-enter new password:   XXXXX
What is your first and last name?
  [Unknown]:
What is the name of your organizational unit?
  [Unknown]:
What is the name of your organization?
  [Unknown]:
What is the name of your City or Locality?
  [Unknown]:
What is the name of your State or Province?
  [Unknown]:
What is the two-letter country code for this unit?
  [Unknown]:
Is CN=Unknown, OU=Unknown, O=Unknown, L=Unknown, ST=Unknown, C=Unknown correct?
  [no]:  yes

Generating 2,048 bit RSA key pair and self-signed certificate (SHA256withRSA) with a validity of 10,000 days
	for: CN=Unknown, OU=Unknown, O=Unknown, L=Unknown, ST=Unknown, C=Unknown
[Storing key-rentadvisor.jks]
```

2. Extract the fingerprint doing:

```
keytool -list -v -keystore key-rentadvisor.jks -alias key-rentadisor
```