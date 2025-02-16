docker run --name sonu-postgres -p 5431:5432 -e POSTGRES_USER=sonupostgres -e POSTGRES_DB=postgresDB -e  POSTGRES_PASSWORD=root -d postgres:15.10-bookworm


-e PGDATA=/var/lib/postgresql/data/pgdata \
	-v /custom/mount:/var/lib/postgresql/data \
    

docker run -it --rm --network some-network postgres:15.10-bookworm psql -h sonu-postgres -U postgres
docker run -it --rm postgres:15.10-bookworm psql -h sonu-postgres -U postgres
psql (14.3)
Type "help" for help.

postgres=# SELECT 1;
 ?column? 
----------
        1
(1 row)
