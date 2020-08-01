# Basic Project to learn ElasticSearch

## Requisites

- vm.max_map_count=262144
  - sysctl -w vm.max_map_count=262144
- Docker
- Docker-Compose
- Postman

## Create the first index (users)

Using PUT method, needs to declare the `_id`
````
PUT /users/_doc/1
````
````
{
  "Name": "Piper",
  "Surname": "Talley"
}
````

Using POST method, no needs to declare the `_id`
````
POST /users/_doc?refresh
````
````
{
  "Name": "Annette Bellamy"
}
````

Bulk method
````
POST /users/_bulk
````
````
{ "index" : { "_id" : "6" } }
{ "Name" : "Dalia", "Surname": "Hensley" }
{ "index" : { "_id" : "7" } }
{ "Name" : "Rahima", "Surname": "Weston" }
{ "index" : { "_id" : "8" } }
{ "Name" : "Buster", "Surname": "Sims" }
{ "index" : { "_id" : "9" } }
{ "Name" : "Aalia", "Surname": "Stephenson" }
{ "index" : { "_id" : "10" } }
{ "Name" : "Zacharias", "Surname": "Fischer" }

````

## License

<img src="./img/by-sa.png">

This work is under [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Please read the LICENSE files for more details.
