# K67 HUST Data Science COURSE Capstone Project: Realtime-Sentiment Analysis on Social Media

## Member
- Quach Tuan Anh 
- Pham Tran Tuan Khang
- Dinh Van Kien
- Nguyen Tran Nghia

![Image Alt Text](assets/Pipeline.png)


Check demo at imgs

Usage

```
docker-compose -f zk-single-kafka-single.yml up -d
pip install -r requirements.txt

# if no mongodb service
docker pull mongo:6.0 
# run mongodb
docker run -d -p 27017:27017 --name mongodb mongo:6.0\
cd Kafka-PySpark
docker exec -it <kafka-container-id> /bin/bash

# setting kafka
kafka-topics --create --topic twitter --bootstrap-server localhost:9092
kafka-topics --describe --topic twitter --bootstrap-server localhost:9092

py producer-validation-tweets.py

py consumer-pyspark.py

# check app
cd Django-Dashboard 
python manage.py collectstatic
python manage.py runserver

```
