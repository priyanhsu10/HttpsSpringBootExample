# HttpsSpringBootExample
keytool -genkey -alias spring-https -storetype PKCS12 -keyalg RSA -keysize 2048 -validity 365 -keystore test.p12

User bellow configuration

server:
  
  ssl:
  
  enabled: true

    keyAlias: spring-https
    key-store: classpath:test.p12
    keyStoreType: PKCS12
    key-store-password: priya123
    
  port: 8443
  
  
 Dont user below configuration other wise will get error  "keystore is corrupt or invalid pasword"
 
 server.port=8443
 
server.ssl.key-alias=Https-example

server.ssl.store-type=JKS ------------------this key name changed to keyStoreType

server.ssl.key-password=password------------this key name changed to keyStoreType

server.ssl.key-store=classpath:https-example.jks

