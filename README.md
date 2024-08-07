# hyperspace
The test functionality and Query testing

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.python.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import hyperspace 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import hyperspace
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = [hyperspace.Document()] # list[Document] | 
collection_name = 'collection_name_example' # str | 

try:
    # Add a new batch to the collection
    api_response = api_instance.add_batch(body, collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->add_batch: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.Document() # Document | 
collection_name = 'collection_name_example' # str | 

try:
    # Add a new document to the collection
    api_response = api_instance.add_document(body, collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->add_document: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 

try:
    # Clear all collection vectors
    api_response = api_instance.clear_collection(collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->clear_collection: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))

try:
    # Get the information of all the collections
    api_response = api_instance.collections_info()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->collections_info: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 

try:
    # Commit
    api_response = api_instance.commit(collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->commit: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.CollectionCollectionNameBody() # CollectionCollectionNameBody | 
collection_name = 'collection_name_example' # str | 

try:
    # Create a new collection
    api_response = api_instance.create_collection(body, collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->create_collection: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.DeleteByQueryRequest() # DeleteByQueryRequest | 
collection_name = 'collection_name_example' # str | 

try:
    # Deletes documents that match the specified query.
    api_response = api_instance.delete_by_query(body, collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->delete_by_query: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 

try:
    # Delete a collection
    api_response = api_instance.delete_collection(collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->delete_collection: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 
document_id = 'document_id_example' # str | 

try:
    # Delete document by Id
    api_response = api_instance.delete_document(collection_name, document_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->delete_document: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 
function_name = 'function_name_example' # str | 

try:
    # Delete function by name
    api_response = api_instance.delete_function(collection_name, function_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->delete_function: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.CollectionNameDslSearchBody() # CollectionNameDslSearchBody | 
size = 56 # int | 
collection_name = 'collection_name_example' # str | 
options = 'options_example' # str |  (optional)
source = true # bool | Indicates whether source fields are returned for matching documents.These fields are returned in the hits._source property of the search response.Defaults to false. (optional)

try:
    # Find top X similar documents in the dataset using Elasticsearch DSL query
    api_response = api_instance.dsl_search(body, size, collection_name, options=options, source=source)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->dsl_search: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 
document_id = 'document_id_example' # str | 
metadata_only = true # bool |  (optional)

try:
    # Find document by Id
    api_response = api_instance.get_document(collection_name, document_id, metadata_only=metadata_only)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->get_document: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 
function_name = 'function_name_example' # str | 

try:
    # Get Function
    api_response = api_instance.get_function(collection_name, function_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->get_function: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 

try:
    # Get schema of collection
    api_response = api_instance.get_schema(collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->get_schema: %s\n" % e)

# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.LoginDto() # LoginDto | 

try:
    # Login
    api_response = api_instance.login(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->login: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))

try:
    # Reset password
    api_response = api_instance.reset_password()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->reset_password: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.Document() # Document | 
size = 56 # int | 
collection_name = 'collection_name_example' # str | 
function_name = 'function_name_example' # str |  (optional)
options = 'options_example' # str |  (optional)
source = true # bool | Indicates whether source fields are returned for matching documents.These fields are returned in the hits._source property of the search response.Defaults to false. (optional)

try:
    # Find top X similar documents in the dataset according to the selected search option.
    api_response = api_instance.search(body, size, collection_name, function_name=function_name, options=options, source=source)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->search: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.FunctionFunctionNameBody() # FunctionFunctionNameBody | 
collection_name = 'collection_name_example' # str | 
function_name = 'function_name_example' # str | 

try:
    # Set Function
    api_response = api_instance.set_function(body, collection_name, function_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->set_function: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.UpdateByQuery() # UpdateByQuery | 
collection_name = 'collection_name_example' # str | 

try:
    # Update documents that match a query using a script
    api_response = api_instance.update_by_query(body, collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->update_by_query: %s\n" % e)


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.Document() # Document | 
collection_name = 'collection_name_example' # str | 
partial_update = true # bool |  (optional)
doc_as_upsert = true # bool |  (optional)

try:
    # Update document by Id in the collection
    api_response = api_instance.update_document(body, collection_name, partial_update=partial_update, doc_as_upsert=doc_as_upsert)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->update_document: %s\n" % e)
```

## Documentation for API Endpoints

All URIs are relative to */*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*HyperspaceApi* | [**add_batch**](docs/HyperspaceApi.md#add_batch) | **POST** /api/v1/{collectionName}/batch | Add a new batch to the collection
*HyperspaceApi* | [**add_document**](docs/HyperspaceApi.md#add_document) | **PUT** /api/v1/{collectionName}/document/add | Add a new document to the collection
*HyperspaceApi* | [**clear_collection**](docs/HyperspaceApi.md#clear_collection) | **GET** /api/v1/{collectionName}/delete | Clear all collection vectors
*HyperspaceApi* | [**collections_info**](docs/HyperspaceApi.md#collections_info) | **GET** /api/v1/collectionsInfo | Get the information of all the collections
*HyperspaceApi* | [**commit**](docs/HyperspaceApi.md#commit) | **GET** /api/v1/{collectionName}/commit | Commit
*HyperspaceApi* | [**create_collection**](docs/HyperspaceApi.md#create_collection) | **PUT** /api/v1/collection/{collectionName} | Create a new collection
*HyperspaceApi* | [**delete_by_query**](docs/HyperspaceApi.md#delete_by_query) | **POST** /api/v1/{collectionName}/delete_by_query | Deletes documents that match the specified query.
*HyperspaceApi* | [**delete_collection**](docs/HyperspaceApi.md#delete_collection) | **GET** /api/v1/collection/{collectionName} | Delete a collection
*HyperspaceApi* | [**delete_document**](docs/HyperspaceApi.md#delete_document) | **GET** /api/v1/{collectionName}/document/delete | Delete document by Id
*HyperspaceApi* | [**delete_function**](docs/HyperspaceApi.md#delete_function) | **GET** /api/v1/{collectionName}/function/delete/{functionName} | Delete function by name
*HyperspaceApi* | [**dsl_search**](docs/HyperspaceApi.md#dsl_search) | **POST** /api/v1/{collectionName}/dsl_search | Find top X similar documents in the dataset using Elasticsearch DSL query
*HyperspaceApi* | [**get_document**](docs/HyperspaceApi.md#get_document) | **GET** /api/v1/{collectionName}/document/get | Find document by Id
*HyperspaceApi* | [**get_function**](docs/HyperspaceApi.md#get_function) | **GET** /api/v1/{collectionName}/function/{functionName} | Get Function
*HyperspaceApi* | [**get_schema**](docs/HyperspaceApi.md#get_schema) | **GET** /api/v1/{collectionName}/schema | Get schema of collection
*HyperspaceApi* | [**login**](docs/HyperspaceApi.md#login) | **POST** /api/v1/login | Login
*HyperspaceApi* | [**reset_password**](docs/HyperspaceApi.md#reset_password) | **POST** /api/v1/reset_password | Reset password
*HyperspaceApi* | [**search**](docs/HyperspaceApi.md#search) | **POST** /api/v1/{collectionName}/search | Find top X similar documents in the dataset according to the selected search option.
*HyperspaceApi* | [**set_function**](docs/HyperspaceApi.md#set_function) | **PUT** /api/v1/{collectionName}/function/{functionName} | Set Function
*HyperspaceApi* | [**update_by_query**](docs/HyperspaceApi.md#update_by_query) | **POST** /api/v1/{collectionName}/update_by_query | Update documents that match a query using a script
*HyperspaceApi* | [**update_document**](docs/HyperspaceApi.md#update_document) | **POST** /api/v1/{collectionName}/document/update | Update document by Id in the collection

## Documentation For Models

 - [AnyOfUpdateByQueryQuery](docs/AnyOfUpdateByQueryQuery.md)
 - [AuthDto](docs/AuthDto.md)
 - [CollectionCollectionNameBody](docs/CollectionCollectionNameBody.md)
 - [CollectionNameDslSearchBody](docs/CollectionNameDslSearchBody.md)
 - [DeleteByQueryRequest](docs/DeleteByQueryRequest.md)
 - [DeleteByQueryResponse](docs/DeleteByQueryResponse.md)
 - [Document](docs/Document.md)
 - [FunctionFunctionNameBody](docs/FunctionFunctionNameBody.md)
 - [LoginDto](docs/LoginDto.md)
 - [Script](docs/Script.md)
 - [StatusDto](docs/StatusDto.md)
 - [UpdateByQuery](docs/UpdateByQuery.md)

## Documentation For Authorization


## bearer



## Author

support@hyper-space.io
