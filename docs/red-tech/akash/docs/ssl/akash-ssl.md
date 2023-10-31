# Welcome to Akash SSL Guideline
# SSL Certificate Setup with Sectigo Certs

In this guide, we will walk through the steps to set up an SSL certificate using Sectigo certificates. You'll learn how to concatenate certificate and CA files to create a certificate bundle.
## Step 1: Copy Certificate and Key Files

To begin, copy the certificate and key files to your desired location. Replace `STAR_akashdth_com.crt` and `STAR_akashdth_com.key` with your actual certificate and key filenames.

```bash
cp STAR_akashdth_com.crt certificate.crt
cp STAR_akashdth_com.key private.key

## Step 2: Concatenate CA Bundle

To create a certificate bundle, you need to concatenate the certificate file with the Sectigo CA file. Use the following command:

```bash
cat STAR_akashdth_com.crt SectigoRSADomainValidationSecureServerCA.crt >> ca_bundle.crt

## Conclusio

You have successfully converted an SSL certificate using Sectigo certificates. The certificate bundle (`ca_bundle.crt`) can now be used for securing your web server. Ensure that you follow the specific requirements of your web server or hosting platform to install and configure the SSL certificate properly.
