## Single Sign-On with Spring Boot, OpenID Connect and Okta

This Spring Boot application demonstrates accomplishing Single Sign-On across multiple OpenID Connect applications
with multiple Authorization Servers defined in Okta.

To use this sample application, you need to create a free developer Okta org. You can do that by going to
https://developer.okta.com.

For more detail about OpenID Connect and how to use this app, check out the blog post here (coming soon).

### Build the app

run:

```mvn clean install```

### Run the app

Included in this repo is a shell script to make it easy to run the app. It works on Mac and Linux:

```
./run_app.sh \
    --ci <client id for oidc app>  \
    --cs <client secret for oidc app> \
    --is <issuer for oidc app>
```

If you're on a different system, you can also run the app directly with maven:

```
mvn spring-boot:run \
    -Dokta.oauth2.clientId=<client id for oidc app> \
    -Dokta.oauth2.clientSecret=<client secret for oidc app> \
    -Dokta.oauth2.issuer=<issuer for oidc app>
```

You can also deploy directly to Heroku and provision an Okta org at the same time!

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

======
mxu 08-22-2019
======

https://developer.okta.com/blog/2019/05/02/spring-boot-single-sign-on-oauth-2

OICD app 1
0oadua5oyLuI5kSDe356
MctUA-zdkZV9hjrKcMuw-7pY_nC1vGIDOfZXlbX_

app2
0oaul8cxlVEEfT7BL356
eGjK1lTJcYTgeww_it_w3kfzSivrstaEcHqCgKC4

iuuser url
app 1
https://dev-879975.okta.com/oauth2/aus167i89dLZsUVO4357

app 2
https://dev-879975.okta.com/oauth2/aus16aiyn5ovXzInI357

mvn spring-boot:run \
    -Dokta.oauth2.clientId=0oadua5oyLuI5kSDe356 \
    -Dokta.oauth2.clientSecret=MctUA-zdkZV9hjrKcMuw-7pY_nC1vGIDOfZXlbX_ \
    -Dokta.oauth2.issuer=https://dev-879975.okta.com/oauth2/aus167i89dLZsUVO4357

mvn spring-boot:run \
    -Dokta.oauth2.clientId=0oaul8cxlVEEfT7BL356 \
    -Dokta.oauth2.clientSecret=eGjK1lTJcYTgeww_it_w3kfzSivrstaEcHqCgKC4 \
    -Dokta.oauth2.issuer=https://dev-879975.okta.com/oauth2/aus16aiyn5ovXzInI357 -Dserver.port=8081


export JAVA_HOME=/c/Users/mxu006/downloads/amazon-corretto-11.0.4.11.1-windows-x64/jdk11.0.4_10

export PATH=$JAVA_HOME/bin:$PATH
