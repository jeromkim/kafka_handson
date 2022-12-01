Kafka Hands-on

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
