# STEP 1 Running Zookeeper and Kafka Server for Windows
( If You come from linux just read docomentation on https://kafka.apache.org/documentation/#quickstart )
1. RUNNING ZOOKEEPER PROPERTIES
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
2. RUNNING KAFKA SERVICES
.\bin\windows\kafka-server-start.bat .\config\server.properties

# STEP 2 Running the Microservice
1. Run Email-Service Application
2. Run Order-service Application
3. Run Stock-service Application

# STEP 3 Testing the Application
1. You can hit API in your Postman like curl below
curl --location 'http://localhost:8080/api/v1/orders' \
--header 'Content-Type: application/json' \
--data '{
    "name": "Glass",
    "qty": 2,
    "price": 600
}'



nb:
If You cannot ran the kafka server in **Windows** *with tutorial above, you need more step
1. Go to your kafka file Users\laptop\Documents\kafka\bin\windows
2. Edit the kafka-run-class.bat
3. Remove bin path or you can change Java Home Path like this.
   From This
rem Which java to use
            IF ["%JAVA_HOME%"] EQU [""] (
            	set JAVA=java
            ) ELSE (
            	set JAVA="%JAVA_HOME%/bin/java"
            )

   To This
               rem Which java to use
            IF ["%JAVA_HOME%"] EQU [""] (
            	set JAVA=java
            ) ELSE (
            	set JAVA="%JAVA_HOME%/java"
            )
