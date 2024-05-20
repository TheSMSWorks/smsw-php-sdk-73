# OpenAPI\Client\MessagesApi

All URIs are relative to https://api.thesmsworks.co.uk/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**binarySendPost()**](MessagesApi.md#binarySendPost) | **POST** /binary/send | Send a binary SMS message
[**messageFlashPost()**](MessagesApi.md#messageFlashPost) | **POST** /message/flash | 
[**messageSchedulePost()**](MessagesApi.md#messageSchedulePost) | **POST** /message/schedule | Schedule an SMS message
[**messageSendPost()**](MessagesApi.md#messageSendPost) | **POST** /message/send | 
[**messagesFailedPost()**](MessagesApi.md#messagesFailedPost) | **POST** /messages/failed | 
[**messagesInboxPost()**](MessagesApi.md#messagesInboxPost) | **POST** /messages/inbox | Retrieve unread uncoming messages
[**messagesMessageidDelete()**](MessagesApi.md#messagesMessageidDelete) | **DELETE** /messages/{messageid} | 
[**messagesMessageidGet()**](MessagesApi.md#messagesMessageidGet) | **GET** /messages/{messageid} | Get message by messageid
[**messagesPost()**](MessagesApi.md#messagesPost) | **POST** /messages | Get messages matching your criteria
[**messagesScheduleGet()**](MessagesApi.md#messagesScheduleGet) | **GET** /messages/schedule | Retrieve scheduled messages
[**messagesScheduleMessageidDelete()**](MessagesApi.md#messagesScheduleMessageidDelete) | **DELETE** /messages/schedule/{messageid} | Cancel scheduled SMS message
[**messagesVolumeGet()**](MessagesApi.md#messagesVolumeGet) | **GET** /messages/volume | Volume of messages sent since midnight


## `binarySendPost()`

```php
binarySendPost($sms_message): \OpenAPI\Client\Model\SendMessageResponse
```

Send a binary SMS message

Sends an SMS Message in Binary format. This can be used to send files and data to devices that process binary content. Especially useful for Internet of Things (IoT). Message content should be encoded in hex pairs (e.g. '65 54 74 73 6d 20 73 65 61 73 65 67 2e')

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_message = new \OpenAPI\Client\Model\Message(); // \OpenAPI\Client\Model\Message | Message properties

try {
    $result = $apiInstance->binarySendPost($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->binarySendPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_message** | [**\OpenAPI\Client\Model\Message**](../Model/Message.md)| Message properties |

### Return type

[**\OpenAPI\Client\Model\SendMessageResponse**](../Model/SendMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messageFlashPost()`

```php
messageFlashPost($sms_message): \OpenAPI\Client\Model\SendMessageResponse
```



Send an SMS flash message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_message = new \OpenAPI\Client\Model\Message(); // \OpenAPI\Client\Model\Message | Message properties

try {
    $result = $apiInstance->messageFlashPost($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messageFlashPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_message** | [**\OpenAPI\Client\Model\Message**](../Model/Message.md)| Message properties |

### Return type

[**\OpenAPI\Client\Model\SendMessageResponse**](../Model/SendMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messageSchedulePost()`

```php
messageSchedulePost($sms_message): \OpenAPI\Client\Model\ScheduledMessageResponse[]
```

Schedule an SMS message

Schedules an SMS message to be sent at the date/time you specify

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_message = new \OpenAPI\Client\Model\Message(); // \OpenAPI\Client\Model\Message | Message properties

try {
    $result = $apiInstance->messageSchedulePost($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messageSchedulePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_message** | [**\OpenAPI\Client\Model\Message**](../Model/Message.md)| Message properties |

### Return type

[**\OpenAPI\Client\Model\ScheduledMessageResponse[]**](../Model/ScheduledMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messageSendPost()`

```php
messageSendPost($sms_message): \OpenAPI\Client\Model\SendMessageResponse
```



Send an SMS Message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_message = new \OpenAPI\Client\Model\Message(); // \OpenAPI\Client\Model\Message | Message properties

try {
    $result = $apiInstance->messageSendPost($sms_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messageSendPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_message** | [**\OpenAPI\Client\Model\Message**](../Model/Message.md)| Message properties |

### Return type

[**\OpenAPI\Client\Model\SendMessageResponse**](../Model/SendMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesFailedPost()`

```php
messagesFailedPost($query): \OpenAPI\Client\Model\MessageResponse[]
```



Retrieve failed messages matching your criteria

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = new \OpenAPI\Client\Model\Query(); // \OpenAPI\Client\Model\Query

try {
    $result = $apiInstance->messagesFailedPost($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesFailedPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**\OpenAPI\Client\Model\Query**](../Model/Query.md)|  |

### Return type

[**\OpenAPI\Client\Model\MessageResponse[]**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesInboxPost()`

```php
messagesInboxPost($query): \OpenAPI\Client\Model\MessageResponse[]
```

Retrieve unread uncoming messages

Retrieve unread uncoming messages matching your criteria

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = new \OpenAPI\Client\Model\Query(); // \OpenAPI\Client\Model\Query

try {
    $result = $apiInstance->messagesInboxPost($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesInboxPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**\OpenAPI\Client\Model\Query**](../Model/Query.md)|  |

### Return type

[**\OpenAPI\Client\Model\MessageResponse[]**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesMessageidDelete()`

```php
messagesMessageidDelete($messageid): \OpenAPI\Client\Model\DeletedMessageResponse
```



Delete the message with the matching messageid

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messageid = 'messageid_example'; // string | The ID of the message you would like returned

try {
    $result = $apiInstance->messagesMessageidDelete($messageid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesMessageidDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageid** | **string**| The ID of the message you would like returned |

### Return type

[**\OpenAPI\Client\Model\DeletedMessageResponse**](../Model/DeletedMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesMessageidGet()`

```php
messagesMessageidGet($messageid): \OpenAPI\Client\Model\MessageResponse
```

Get message by messageid

Retrieve a delivery report by the message ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messageid = 'messageid_example'; // string | The ID of the message you would like returned

try {
    $result = $apiInstance->messagesMessageidGet($messageid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesMessageidGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageid** | **string**| The ID of the message you would like returned |

### Return type

[**\OpenAPI\Client\Model\MessageResponse**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesPost()`

```php
messagesPost($query): \OpenAPI\Client\Model\MessageResponse[]
```

Get messages matching your criteria

Retrieve up to 1000 messages matching criteria specified in the request

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$query = new \OpenAPI\Client\Model\Query(); // \OpenAPI\Client\Model\Query

try {
    $result = $apiInstance->messagesPost($query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | [**\OpenAPI\Client\Model\Query**](../Model/Query.md)|  |

### Return type

[**\OpenAPI\Client\Model\MessageResponse[]**](../Model/MessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesScheduleGet()`

```php
messagesScheduleGet(): \OpenAPI\Client\Model\ScheduledMessagesResponse
```

Retrieve scheduled messages

Return a list of messages scheduled from your account, comprising any messages scheduled in the last 3 months and any scheduled to send in the future

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->messagesScheduleGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesScheduleGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ScheduledMessagesResponse**](../Model/ScheduledMessagesResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesScheduleMessageidDelete()`

```php
messagesScheduleMessageidDelete($messageid): \OpenAPI\Client\Model\CancelledMessageResponse
```

Cancel scheduled SMS message

Cancels a scheduled SMS message matching the provided messageid

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$messageid = 'messageid_example'; // string | The ID of the message you would like returned

try {
    $result = $apiInstance->messagesScheduleMessageidDelete($messageid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesScheduleMessageidDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messageid** | **string**| The ID of the message you would like returned |

### Return type

[**\OpenAPI\Client\Model\CancelledMessageResponse**](../Model/CancelledMessageResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `messagesVolumeGet()`

```php
messagesVolumeGet(): \OpenAPI\Client\Model\MessageVolumeResponse
```

Volume of messages sent since midnight

Retrieve the number of messages sent since midnight last night

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: JWT
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->messagesVolumeGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->messagesVolumeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\MessageVolumeResponse**](../Model/MessageVolumeResponse.md)

### Authorization

[JWT](../../README.md#JWT)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json;charset=UTF-8`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
