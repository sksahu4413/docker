docker-compose down --volumes --remove-orphans

docker-compose up airflow-init

docker-compose up

db init

airflow users create \
    --username airflow \
    --firstname Airflow \
    --lastname Sharma \
    --role Admin \
    --email admin@example.com \
    --password airflow
