# Swagger\Client\TodoApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteTodoItem**](TodoApi.md#deletetodoitem) | **DELETE** /api/todos/{id} | Removes the todo resource.
[**getTodoCollection**](TodoApi.md#gettodocollection) | **GET** /api/todos | Retrieves the collection of todo resources.
[**getTodoItem**](TodoApi.md#gettodoitem) | **GET** /api/todos/{id} | Retrieves a todo resource.
[**postTodoCollection**](TodoApi.md#posttodocollection) | **POST** /api/todos | Creates a todo resource.
[**putTodoItem**](TodoApi.md#puttodoitem) | **PUT** /api/todos/{id} | Replaces the todo resource.

# **deleteTodoItem**
> deleteTodoItem($id)

Removes the todo resource.

Removes the todo resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TodoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | Resource identifier

try {
    $apiInstance->deleteTodoItem($id);
} catch (Exception $e) {
    echo 'Exception when calling TodoApi->deleteTodoItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Resource identifier |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTodoCollection**
> \Swagger\Client\Model\InlineResponse200 getTodoCollection($page, $finished, $title, $properties)

Retrieves the collection of todo resources.

Retrieves the collection of todo resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TodoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | The collection page number
$finished = true; // bool | 
$title = "title_example"; // string | 
$properties = array("properties_example"); // string[] | 

try {
    $result = $apiInstance->getTodoCollection($page, $finished, $title, $properties);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodoApi->getTodoCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]
 **finished** | **bool**|  | [optional]
 **title** | **string**|  | [optional]
 **properties** | [**string[]**](../Model/string.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTodoItem**
> \Swagger\Client\Model\TodoJsonldTaskRead getTodoItem($id)

Retrieves a todo resource.

Retrieves a todo resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TodoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | Resource identifier

try {
    $result = $apiInstance->getTodoItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodoApi->getTodoItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Resource identifier |

### Return type

[**\Swagger\Client\Model\TodoJsonldTaskRead**](../Model/TodoJsonldTaskRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTodoCollection**
> \Swagger\Client\Model\TodoJsonldTaskRead postTodoCollection($body)

Creates a todo resource.

Creates a todo resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TodoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\TodoJsonldTaskRead(); // \Swagger\Client\Model\TodoJsonldTaskRead | The new todo resource

try {
    $result = $apiInstance->postTodoCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodoApi->postTodoCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TodoJsonldTaskRead**](../Model/TodoJsonldTaskRead.md)| The new todo resource |

### Return type

[**\Swagger\Client\Model\TodoJsonldTaskRead**](../Model/TodoJsonldTaskRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json, text/html
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putTodoItem**
> \Swagger\Client\Model\TodoJsonldTaskRead putTodoItem($body, $id)

Replaces the todo resource.

Replaces the todo resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TodoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\TodoJsonldTaskRead(); // \Swagger\Client\Model\TodoJsonldTaskRead | The updated todo resource
$id = "id_example"; // string | Resource identifier

try {
    $result = $apiInstance->putTodoItem($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TodoApi->putTodoItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TodoJsonldTaskRead**](../Model/TodoJsonldTaskRead.md)| The updated todo resource |
 **id** | **string**| Resource identifier |

### Return type

[**\Swagger\Client\Model\TodoJsonldTaskRead**](../Model/TodoJsonldTaskRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json, text/html
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

