# micro-service-with-ssl
# Calling Course-Service Microservice(service can access via certificates) from Enroll-Service Microservice using certificates.


1.  A microservice is exposed and can accessable through secured way. Assume it's a Course-Service, which is exposed and can accessable through secured way. Generated certificates for Course Service, which can be used by Enroll-Service.
<br>
<br>


2.  Another microservice is, Enroll-Service trying to access the previous service in step 1. Please follow the below steps to access the above service.
<br>
    a.  once received the certificate of Course-Service. Import the certificate using the keytool command. Go to the cacerts folder location: %JAVA_HOME%/jre/lib/security
    keytool -import -alias alias_name -file file_location -keystore cacerts - defualt password is changeit.
    <br>
    <br>
    b.  Please configre the same jdk to Enroll-Service and call the Course-Service.
