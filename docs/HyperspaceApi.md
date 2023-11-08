# hyperspace.HyperspaceApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_batch**](HyperspaceApi.md#add_batch) | **PUT** /api/v1/{collectionName}/batch | Add a new batch to the collection
[**add_document**](HyperspaceApi.md#add_document) | **PUT** /api/v1/{collectionName}/document/add | Add a new document to the collection
[**clear_collection**](HyperspaceApi.md#clear_collection) | **GET** /api/v1/{collectionName}/delete | Clear all collection vectors
[**collections_info**](HyperspaceApi.md#collections_info) | **GET** /api/v1/collectionsInfo | Get the information of all the collections
[**commit**](HyperspaceApi.md#commit) | **GET** /api/v1/{collectionName}/commit | Commit
[**create_collection**](HyperspaceApi.md#create_collection) | **PUT** /api/v1/collection/{collectionName} | Create a new collection
[**delete_collection**](HyperspaceApi.md#delete_collection) | **GET** /api/v1/collection/{collectionName} | Delete a collection
[**delete_document**](HyperspaceApi.md#delete_document) | **GET** /api/v1/{collectionName}/document/delete | Delete document by Id
[**delete_function**](HyperspaceApi.md#delete_function) | **GET** /api/v1/{collectionName}/function/delete/{functionName} | Delete function by name
[**get_document**](HyperspaceApi.md#get_document) | **GET** /api/v1/{collectionName}/document/get | Find document by Id
[**get_function**](HyperspaceApi.md#get_function) | **GET** /api/v1/{collectionName}/function/{functionName} | Get Function
[**get_schema**](HyperspaceApi.md#get_schema) | **GET** /api/v1/{collectionName}/schema | Get schema of collection
[**login**](HyperspaceApi.md#login) | **POST** /api/v1/login | Login
[**search**](HyperspaceApi.md#search) | **POST** /api/v1/{collectionName}/search | Find top X similar documents in the dataset according to the selected search option.
[**set_function**](HyperspaceApi.md#set_function) | **PUT** /api/v1/{collectionName}/function/{functionName} | Set Function
[**update_document**](HyperspaceApi.md#update_document) | **POST** /api/v1/{collectionName}/document/update | Update document by Id in the collection

# **add_batch**
> StatusDto add_batch(body, collection_name)

Add a new batch to the collection

### Example
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
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**list[Document]**](Document.md)|  | 
 **collection_name** | **str**|  | 

### Return type

[**StatusDto**](StatusDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/msgpack
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_document**
> StatusDto add_document(body, collection_name)

Add a new document to the collection

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


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
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Document**](Document.md)|  | 
 **collection_name** | **str**|  | 

### Return type

[**StatusDto**](StatusDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/msgpack
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clear_collection**
> StatusDto clear_collection(collection_name)

Clear all collection vectors

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 

try:
    # Clear all collection vectors
    api_response = api_instance.clear_collection(collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->clear_collection: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_name** | **str**|  | 

### Return type

[**StatusDto**](StatusDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **collections_info**
> CollectionNameSearchBody collections_info()

Get the information of all the collections

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))

try:
    # Get the information of all the collections
    api_response = api_instance.collections_info()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->collections_info: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CollectionNameSearchBody**](CollectionNameSearchBody.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **commit**
> StatusDto commit(collection_name)

Commit

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 

try:
    # Commit
    api_response = api_instance.commit(collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->commit: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_name** | **str**|  | 

### Return type

[**StatusDto**](StatusDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_collection**
> InlineResponse200 create_collection(file, collection_name)

Create a new collection

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
file = 'file_example' # str | 
collection_name = 'collection_name_example' # str | 

try:
    # Create a new collection
    api_response = api_instance.create_collection(file, collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->create_collection: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **str**|  | 
 **collection_name** | **str**|  | 

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_collection**
> StatusDto delete_collection(collection_name)

Delete a collection

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 

try:
    # Delete a collection
    api_response = api_instance.delete_collection(collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->delete_collection: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_name** | **str**|  | 

### Return type

[**StatusDto**](StatusDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_document**
> StatusDto delete_document(collection_name, document_id)

Delete document by Id

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


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
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_name** | **str**|  | 
 **document_id** | **str**|  | 

### Return type

[**StatusDto**](StatusDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_function**
> StatusDto delete_function(collection_name, function_name)

Delete function by name

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


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
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_name** | **str**|  | 
 **function_name** | **str**|  | 

### Return type

[**StatusDto**](StatusDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_document**
> InlineResponse200 get_document(collection_name, document_id)

Find document by Id

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 
document_id = 'document_id_example' # str | 

try:
    # Find document by Id
    api_response = api_instance.get_document(collection_name, document_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->get_document: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_name** | **str**|  | 
 **document_id** | **str**|  | 

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/msgpack

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_function**
> CollectionNameSearchBody get_function(collection_name, function_name)

Get Function

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


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
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_name** | **str**|  | 
 **function_name** | **str**|  | 

### Return type

[**CollectionNameSearchBody**](CollectionNameSearchBody.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_schema**
> CollectionNameSearchBody get_schema(collection_name)

Get schema of collection

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
collection_name = 'collection_name_example' # str | 

try:
    # Get schema of collection
    api_response = api_instance.get_schema(collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->get_schema: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **collection_name** | **str**|  | 

### Return type

[**CollectionNameSearchBody**](CollectionNameSearchBody.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login**
> AuthDto login(body)

Login

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = hyperspace.HyperspaceApi()
body = hyperspace.LoginDto() # LoginDto | 

try:
    # Login
    api_response = api_instance.login(body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->login: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**LoginDto**](LoginDto.md)|  | 

### Return type

[**AuthDto**](AuthDto.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **search**
> CollectionNameSearchBody search(body, size, collection_name, function_name=function_name)

Find top X similar documents in the dataset according to the selected search option.

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.CollectionNameSearchBody() # CollectionNameSearchBody | 
size = 56 # int | 
collection_name = 'collection_name_example' # str | 
function_name = 'function_name_example' # str |  (optional)

try:
    # Find top X similar documents in the dataset according to the selected search option.
    api_response = api_instance.search(body, size, collection_name, function_name=function_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->search: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**CollectionNameSearchBody**](CollectionNameSearchBody.md)|  | 
 **size** | **int**|  | 
 **collection_name** | **str**|  | 
 **function_name** | **str**|  | [optional] 

### Return type

[**CollectionNameSearchBody**](CollectionNameSearchBody.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_function**
> StatusDto set_function(file, collection_name, function_name)

Set Function

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
file = 'file_example' # str | 
collection_name = 'collection_name_example' # str | 
function_name = 'function_name_example' # str | 

try:
    # Set Function
    api_response = api_instance.set_function(file, collection_name, function_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->set_function: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **str**|  | 
 **collection_name** | **str**|  | 
 **function_name** | **str**|  | 

### Return type

[**StatusDto**](StatusDto.md)

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_document**
> str update_document(body, collection_name)

Update document by Id in the collection

### Example
```python
from __future__ import print_function
import time
import hyperspace
from hyperspace.rest import ApiException
from pprint import pprint


# create an instance of the API class
api_instance = hyperspace.HyperspaceApi(hyperspace.ApiClient(configuration))
body = hyperspace.Document() # Document | 
collection_name = 'collection_name_example' # str | 

try:
    # Update document by Id in the collection
    api_response = api_instance.update_document(body, collection_name)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling HyperspaceApi->update_document: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Document**](Document.md)|  | 
 **collection_name** | **str**|  | 

### Return type

**str**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: application/msgpack
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

