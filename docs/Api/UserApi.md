# Swagger\Client\UserApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteUserItem**](UserApi.md#deleteuseritem) | **DELETE** /api/users/{id} | Removes the User resource.
[**getUserCollection**](UserApi.md#getusercollection) | **GET** /api/users | Retrieves the collection of User resources.
[**getUserItem**](UserApi.md#getuseritem) | **GET** /api/users/{id} | Retrieves a User resource.
[**patchUserItem**](UserApi.md#patchuseritem) | **PATCH** /api/users/{id} | Updates the User resource.
[**postUserCollection**](UserApi.md#postusercollection) | **POST** /api/users | Creates a User resource.
[**putUserItem**](UserApi.md#putuseritem) | **PUT** /api/users/{id} | Replaces the User resource.

# **deleteUserItem**
> deleteUserItem($id)

Removes the User resource.

Removes the User resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | Resource identifier

try {
    $apiInstance->deleteUserItem($id);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->deleteUserItem: ', $e->getMessage(), PHP_EOL;
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

# **getUserCollection**
> \Swagger\Client\Model\InlineResponse2001 getUserCollection($page, $email, $properties)

Retrieves the collection of User resources.

Retrieves the collection of User resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | The collection page number
$email = "email_example"; // string | 
$properties = array("properties_example"); // string[] | 

try {
    $result = $apiInstance->getUserCollection($page, $email, $properties);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->getUserCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| The collection page number | [optional] [default to 1]
 **email** | **string**|  | [optional]
 **properties** | [**string[]**](../Model/string.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getUserItem**
> \Swagger\Client\Model\UserJsonldUserRead getUserItem($id)

Retrieves a User resource.

Retrieves a User resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = "id_example"; // string | Resource identifier

try {
    $result = $apiInstance->getUserItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->getUserItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| Resource identifier |

### Return type

[**\Swagger\Client\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **patchUserItem**
> \Swagger\Client\Model\UserJsonldUserRead patchUserItem($body, $id)

Updates the User resource.

Updates the User resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\UserJsonldUserRead(); // \Swagger\Client\Model\UserJsonldUserRead | The updated User resource
$id = "id_example"; // string | Resource identifier

try {
    $result = $apiInstance->patchUserItem($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->patchUserItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)| The updated User resource |
 **id** | **string**| Resource identifier |

### Return type

[**\Swagger\Client\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/merge-patch+json
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postUserCollection**
> \Swagger\Client\Model\UserJsonldUserRead postUserCollection($body)

Creates a User resource.

Creates a User resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\UserJsonldUserRead(); // \Swagger\Client\Model\UserJsonldUserRead | The new User resource

try {
    $result = $apiInstance->postUserCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->postUserCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)| The new User resource |

### Return type

[**\Swagger\Client\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json, text/html
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putUserItem**
> \Swagger\Client\Model\UserJsonldUserRead putUserItem($body, $id)

Replaces the User resource.

Replaces the User resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \Swagger\Client\Model\UserJsonldUserRead(); // \Swagger\Client\Model\UserJsonldUserRead | The updated User resource
$id = "id_example"; // string | Resource identifier

try {
    $result = $apiInstance->putUserItem($body, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->putUserItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)| The updated User resource |
 **id** | **string**| Resource identifier |

### Return type

[**\Swagger\Client\Model\UserJsonldUserRead**](../Model/UserJsonldUserRead.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/ld+json, application/json, text/html
 - **Accept**: application/ld+json, application/json, text/html

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

