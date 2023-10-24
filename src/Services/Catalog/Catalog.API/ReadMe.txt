docker pull mongo
docker run -d -p 27017:27017 --name shopping-mongo mongo
docker logs -f shopping-mongo
docker exec -it shopping-mongo mongosh

show dbs
use CatalogDb
db.createCollection('Products')