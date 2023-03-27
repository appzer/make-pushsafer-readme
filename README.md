# Pushsafer
The Pushsafer modules allow you to send messages and interact with the Pushsafer API.

## Getting Stared with Pushsafer
Prerequisites
- Pushsafer account
- a valid device

In order to use Pushsafer with Make, you must have a Pushsafer account. If you do not have one, you can create one at [pushsafer.com](https://www.pushsafer.com).

## Connecting Pushsafer to Make
To connect your Pushsafer account to Make, you need your Private Key.
1. Log in to your Pushsafer account.
2. You can find your Private Key in your dashboard. ![You can find your Private Key in your dashboard.](https://www.pushsafer.com/en/assets/examples/privatekey_en.jpg)
3. In Make, choose the Pushsafer module you want to use. Next to Connection, click Add.
4. Enter your Private Key in the respective field.
5. Click Save.

You have established the connection.

## Actions
### Send a Message
Sends a message to your Pushsafer devices.

| **Connection** | [Establish a connection to your Pushsafer account.](#connecting-pushsafer-to-make) |
| --- | --- |
| **Message** | Message / text of the push notification (required), max. 5000 characters, but the push notification will show fewer characters depending on the system. The client APP shows all characters. |
| **Title** | Subject / title of a push-notification, max. 255 characters |
| **Device** | Choose one of your devices or device groups to send just to that device/group, instead of all devices. |
| **Icon** | Choose the notifications icon |
| **Sound** | Choose the notifications sound |
| **URL** | Enter a URL to show with your message. This URL can be opened directly from the push notification or from the client-app. Instead of an URL, URL schemes can also be transmitted. URL schemes open other APPs if they are installed on the device. Here are some examples of [URL Schemes](https://www.pushsafer.com/url_schemes). |
| **URL Title** | Describes the title of the URL. If this parameter is not passed, the URL title is equal to the URL. |
| **Icon Color** | Set the Icons color with a hexadecimal color code (example for red: #FF0000) |
| **Vibration** | How often the device should vibrate when receiving a push-notification. blank=device default or a number 1-3 |
| **Priority** | Choose the notifications priority |
| **Time2Live** | Specifies how long a message should be kept in the client APP until it is automatically deleted. 0 or empty = do not automatically delete, an integer value 1-43200 the time in minutes before automatic deletion. |
| **Retry** | With the retry / resend Parameter, a message will be resent after a certain time (60-10800 seconds, 60's steps). Resending can be stopped by opening the message in the Client APP or on the Pushsafer website or using the parameter **Expire**. |
| **Expire** | The Expire parameter stops resending push-notifications after a specified time (60-10800 seconds). Example: a message should sent again every 2 minutes for two hours. The following values must be passed! **Retry**=120 **Expire**=7200 |
| **Confirm** | With the Confirm Parameter, a message will be resent after a specified period of time (10-10800 seconds, steps of 10s) until the message confirmed by opening the client APP or on the Pushsafer website. **Confirm** has priority over **Retry** and **Expire**! |
| **Answer** | Ability to respond to push notifications. Answers can be written or viewed via the Client APP, via the Pushsafer website or API. |
| **Answer Options** | Specify predefined answer options divided by a pipe character, e.g. Yes\|No\|Maybe. These serve as a quick selection in the Pushsafer Client APP. The parameter **Answer** must be **yes**! |
| **Anwser Force** | The user will be prompted to answer, the message will be open directly. The parameter **Answer** must be **yes**! |

### Make an API Call
Performs an arbitrary authorized API call.

| **Connection** | [Establish a connection to your Pushsafer account.](#connecting-pushsafer-to-make) |
| --- | --- |
| **URL** | Enter a path relative to `https://www.pushsafer.com`. For example: `/api-d` **Note** For the list of available endpoints, refer to the [Pushsafer API Documentation](https://www.pushsafer.com/pushapi). |
| **Method** | Select the HTTP method you want to use: **GET** or **POST** |
| **Query String** | Enter the request query string **keys** and **values**. |
| **Body** | Enter the body content for your API call. |

### Example of Use - List Devices and Groups
The following API call returns all the devices and groups from your Pushsafer account:

**URL:** `\api-d`

**Method:** POST

![Pushsafer API Call with MAKE.](https://www.pushsafer.com/en/assets/examples/make-api-call.jpg)

Matches of the search can be found in the module's Output under Bundle > Body. Our example returned all users devices and groups:

![Pushsafer API Call Output.](https://www.pushsafer.com/en/assets/examples/make-output.jpg)
