Kafka Hands-on

KAFKA_BROKER_ID
    클러스터 각 노드에 할당할 브로커의 아이디(중복불가) 
# KAFKA_ZOOKEEPER_CONNECT 
    클러스터 구성에 사용할 주키퍼 호스트 정보
# KAFKA_ADVERTISEMENT_LISTENERS
    카프카 브로커를 가리키는 주소 목록. 카프카 브로커는 초기 연결 시 이를 클라이언트에게 보낸다.
# KAFKA_INTER_BROKER_LISTENER_NAME
    브로커 간 통신에 사용할 리스너명
# KAFKA_LISTENER_SECURITY_PROTOCOL_MAP
    보안 프로토콜 지정. PLAINTEXT는 리스너가 암호화되지 않은 것을 말함.
# KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR
    토픽 파티션의 복제 개수

# kafka topic 생성
./kafka-topics --bootstrap-server localhost:19092 --create --topic ldcc01 --partitions 20 --replication-factor 3

# kafka에 생성된 토픽 리스트 확인
./kafka-topics --bootstrap-server localhost:19092 --list

# 특정 토픽의 파티션 수, 리플리카 수 등의 상세정보 확인
./kafka-topics --describe --bootstrap-server localhost:19092 --topic ldcc01

# kafka 콘솔 컨슈머 실행
./kafka-console-consumer --bootstrap-server localhost:19092 --topic ldcc01 --from-beginning

# kafka 콘솔 프로듀서 실행
./kafka-console-producer --bootstrap-server localhost:19092 --topic ldcc01
