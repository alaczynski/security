<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Resources](#resources)
- [Java Security](#java-security)
  - [Resources](#resources)
  - [keytool](#keytool)
- [Certificates](#certificates)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Resources
* Network Security with OpenSSL (2002) https://www.amazon.com/Network-Security-OpenSSL-John-Viega/dp/059600270X
* HTTP: The Definitive Guide (2002) https://www.amazon.com/HTTP-Definitive-Guide-Guides/dp/1565925092
  * Chapter 14. Secure HTTP
* Understanding Cryptography (2010) https://www.amazon.com/Understanding-Cryptography-Textbook-Students-Practitioners/dp/3642041000
* High Performance Browser Networking (2013) https://www.amazon.com/High-Performance-Browser-Networking-performance/dp/1449344763
  * Chapter 4. Transport Layer Security (TLS)
* Bulletproof SSL and TLS (2014) https://www.amazon.com/Bulletproof-SSL-TLS-Understanding-Applications/dp/1907117040
* OpenSSL Cookbook (2015) https://www.feistyduck.com/books/openssl-cookbook/
* SSL and TLS Deployment Best Practices https://github.com/ssllabs/research/wiki/SSL-and-TLS-Deployment-Best-Practices
* SSL Labs https://www.ssllabs.com/index.html
* Feisty Duck https://www.feistyduck.com/

# Java Security
## Resources
* Java security overview (2005) - http://www.oracle.com/technetwork/java/js-white-paper-149932.pdf
* Java SE Security Documentation - http://www.oracle.com/technetwork/java/index-139231.html
* Java SE 8 Security Documentation - http://docs.oracle.com/javase/8/docs/technotes/guides/security/
  * Security Tools Summary - http://docs.oracle.com/javase/8/docs/technotes/guides/security/SecurityToolsSummary.html
  * keytool - http://docs.oracle.com/javase/8/docs/technotes/tools/windows/keytool.html

## keytool
```
keytool -list -keystore sample.jks -storepass secret -v
keytool -exportcert -keystore sample.jks -storepass secret -v -alias spring-boot-ssl-sample -file sample.cer
keytool -printcert -file sample.cer
keytool -printcert -file sample.cer -rfc

openssl x509 -in sample.cer -text -noout -inform der
openssl x509 -in sample.pem -text -noout
```

# Certificates
* convert certificate formats - https://www.sslshopper.com/ssl-converter.html

# OpenSSL
## Resources
* OpenSSL Essentials https://www.digitalocean.com/community/tutorials/openssl-essentials-working-with-ssl-certificates-private-keys-and-csrs
* Intro to OpenSSL command line http://users.dcc.uchile.cl/~pcamacho/tutorial/crypto/openssl/openssl_intro.html
* https://konklone.com/post/why-google-is-hurrying-the-web-to-kill-sha-1
## commands
```
# version
openssl version

# help
openssl help      # there is help be error message will list all commands
man openssl
man req           # man <command>

```

