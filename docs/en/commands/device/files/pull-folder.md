# Pull Folder

Retrieve a folder from the device's file system
## Example Usage

```java
// Java
byte[] folder = driver.pullFolder("/path/to/device/foo.bar");

```

```python
# Python
folder_base64 = self.driver.pull_folder('/path/to/device/foo.bar');

```

```javascript
// Javascript
// webdriver.io example
let data = driver.pullFolder('/data/local/tmp/file.txt');



// wd example
let folderBase64 = await driver.pullFolder('/path/to/device/foo.bar');

```

```ruby
# Ruby
@driver.pull_folder('/data/local/tmp/file.txt');

```

```php
# PHP
// TODO PHP sample

```

```csharp
// C#
// TODO C# sample

```



## Support

### Appium Server

|Platform|Driver|Platform Versions|Appium Version|Driver Version|
|--------|----------------|------|--------------|--------------|
| iOS | [XCUITest](/docs/en/drivers/ios-xcuitest.md) | 9.3+ | 1.6.0+ | All |
|  | [UIAutomation](/docs/en/drivers/ios-uiautomation.md) | 8.0 to 9.3 | All | All |
| Android | [UiAutomator2](/docs/en/drivers/android-uiautomator2.md) | ?+ | 1.6.0+ | All |
|  | [UiAutomator](/docs/en/drivers/android-uiautomator.md) | 4.2+ | All | All |
| Mac | [Mac](/docs/en/drivers/mac.md) | None | None | None |
| Windows | [Windows](/docs/en/drivers/windows.md) | None | None | None |

### Appium Clients

|Language|Support|Documentation|
|--------|-------|-------------|
|[Java](https://github.com/appium/java-client/releases/latest)| All |  [appium.github.io](http://appium.github.io/java-client/io/appium/java_client/InteractsWithFiles.html#pullFolder-java.lang.String-)  |
|[Python](https://github.com/appium/python-client/releases/latest)| All |  [github.com](https://github.com/appium/python-client/blob/master/appium/webdriver/webdriver.py#L503)  |
|[Javascript (WebdriverIO)](http://webdriver.io/index.html)| All |  [webdriver.io](http://webdriver.io/api/mobile/pullFolder.html)  |
|[Javascript (WD)](https://github.com/admc/wd/releases/latest)| All |  [github.com](https://github.com/admc/wd/blob/master/lib/commands.js#L2688)  |
|[Ruby](https://github.com/appium/ruby_lib/releases/latest)| All |  [www.rubydoc.info](http://www.rubydoc.info/github/appium/ruby_lib/Appium/Core/Device:pull_folder)  |
|[PHP](https://github.com/appium/php-client/releases/latest)| All |  [github.com](https://github.com/appium/php-client/)  |
|[C#](https://github.com/appium/appium-dotnet-driver/releases/latest)| All |  [github.com](https://github.com/appium/appium-dotnet-driver/)  |

## HTTP API Specifications

### Endpoint

`POST /wd/hub/session/:session_id/device/pull_folder`

### URL Parameters

|name|description|
|----|-----------|
|session_id|ID of the session to route the command to|

### JSON Parameters

|name|type|description|
|----|----|-----------|
| path | `string` | Path to an entire folder on the device |

### Response

A string of Base64 encoded data, representing a zip archive of the contents of the requested folder. (`string`)

## See Also

* [JSONWP Specification](https://github.com/appium/appium-base-driver/blob/master/lib/mjsonwp/routes.js#L393)
