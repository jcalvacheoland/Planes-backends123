comandos para buscar en produccion:
GET vehicle_plans/_search
{
  "query": {
    "match": {

        "company_social_reason" : "Equisuiza"
      
    }
  }
}
comandos para buscar en desarrollo:
GET dev_plans/_search
{
  "size": 100,          
  "query": {
    "match_all": {}
  },
  "sort": [
    { "_doc": { "order": "asc" } }
  ]
}

comandos para agregar:
POST dev_plans/_doc
//insertar json

comando para editar en modo desarrollo:
PUT dev_plans/_doc/yYhisZoBzxiqX-1vzXlA