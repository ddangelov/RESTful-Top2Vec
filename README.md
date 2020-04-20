[![](https://img.shields.io/docker/v/ddangelov/restful-top2vec?label=docker)](https://hub.docker.com/r/ddangelov/restful-top2vec)
[![](https://img.shields.io/pypi/l/top2vec.svg)](https://github.com/ddangelov/RESTful-Top2Vec/blob/master/LICENSE)
[![Documentation Status](https://readthedocs.org/projects/restful-top2vec/badge/?version=latest)](https://restful-top2vec.readthedocs.io/en/latest/?badge=latest)


Top2Vec Model REST API
======================

Expose a trained and saved [Top2Vec](https://github.com/ddangelov/Top2Vec) model with a REST API.

Get Docker Image
------------
```bash
docker pull ddangelov/restful-top2vec
```

Run Container 
-------------

Docker Run Arguments:

  * ``model_path``: Path to a saved Top2Vec model.
  * ``model_name``: Name of Top2Vec model. (Should not contain spaces.)
  
```bash
export model_path="/path_to_top2vec_model"
export model_name="model_name"

docker run -v $model_path:/app/top2vec_model -e model_name=$model_name -d --name $model_name -p 80:80 ddangelov/restful-top2vec
```

Documentation
-------------

Go to <http://localhost:80/docs>

![](https://raw.githubusercontent.com/ddangelov/RESTful-Top2Vec/master/images/restful-top2vec.png)
