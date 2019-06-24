Steps for setting kafka on windows:
  -1>Download kafka Binary file
  -2>unzip kafka in c:\kafka-2.1.12.0
  -3>start zokeeper instance: zkserver
  -4>go to c:\kafka-2.1.12.0-> start kafka server : C:\kafka_2.12-2.2.0>.\bin\windows\kafka-server-start.bat .\config\server.properties
  -5>go to kafka\bin\windows, open new cmd and create kafka topic:(producer)
                   kafka-console-producer.bat --broker-list localhost:9092 --topic test(topic name)
  -6>go to kafka\bin\windows, open new cmd, we need to consume from this particular topic:(consumer)
                   kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test(topic name) --from-beginning
  
  ***********************************************************************************************************************
  To create topic:
                    got to bin-windows-->kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic KAFKA_MSG(topicname)
                    
 **************************************************************************************************************************************
 
 TO consume from that topic:
 go to bin-windows-->kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic KAFKA_MSG(topicname) --from-beginning
  
 ************************************************************************************************************************************
 Default Port: 
    Kafka: 9092
    Zookeeper: 2181
        

--> Downloading and setting up zookeeper -- https://www.edureka.co/community/39059/installing-zookeeper-on-windows
    After installing, start zkserver.sh and zkserver.cmd 

                
