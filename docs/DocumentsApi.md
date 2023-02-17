# KIQR::DocumentsApi

All URIs are relative to *https://content.kiqr.cloud/v1*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_document**](DocumentsApi.md#get_document) | **GET** /{content_type_slug}/{document_slug} | Returns a document |
| [**get_documents**](DocumentsApi.md#get_documents) | **GET** /{content_type_slug}/ | Returns documents by content type |


## get_document

> <Document> get_document(content_type_slug, document_slug)

Returns a document

### Examples

```ruby
require 'time'
require 'kiqr-content-api'
# setup authorization
KIQR.configure do |config|
  # Configure API key authorization: environmentId
  config.api_key['environmentId'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['environmentId'] = 'Bearer'
end

api_instance = KIQR::DocumentsApi.new
content_type_slug = 'posts' # String | 
document_slug = 'doc_LMxzy1KnBRQKxFyZ0aGNdqp5' # String | 

begin
  # Returns a document
  result = api_instance.get_document(content_type_slug, document_slug)
  p result
rescue KIQR::ApiError => e
  puts "Error when calling DocumentsApi->get_document: #{e}"
end
```

#### Using the get_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Document>, Integer, Hash)> get_document_with_http_info(content_type_slug, document_slug)

```ruby
begin
  # Returns a document
  data, status_code, headers = api_instance.get_document_with_http_info(content_type_slug, document_slug)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Document>
rescue KIQR::ApiError => e
  puts "Error when calling DocumentsApi->get_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type_slug** | **String** |  |  |
| **document_slug** | **String** |  |  |

### Return type

[**Document**](Document.md)

### Authorization

[environmentId](../README.md#environmentId)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_documents

> <DocumentsCollection> get_documents(content_type_slug)

Returns documents by content type

### Examples

```ruby
require 'time'
require 'kiqr-content-api'
# setup authorization
KIQR.configure do |config|
  # Configure API key authorization: environmentId
  config.api_key['environmentId'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['environmentId'] = 'Bearer'
end

api_instance = KIQR::DocumentsApi.new
content_type_slug = 'posts' # String | 

begin
  # Returns documents by content type
  result = api_instance.get_documents(content_type_slug)
  p result
rescue KIQR::ApiError => e
  puts "Error when calling DocumentsApi->get_documents: #{e}"
end
```

#### Using the get_documents_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentsCollection>, Integer, Hash)> get_documents_with_http_info(content_type_slug)

```ruby
begin
  # Returns documents by content type
  data, status_code, headers = api_instance.get_documents_with_http_info(content_type_slug)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentsCollection>
rescue KIQR::ApiError => e
  puts "Error when calling DocumentsApi->get_documents_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **content_type_slug** | **String** |  |  |

### Return type

[**DocumentsCollection**](DocumentsCollection.md)

### Authorization

[environmentId](../README.md#environmentId)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json
