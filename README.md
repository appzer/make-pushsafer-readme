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
| **Devices** | Choose one of your devices or device groups to send just to that device/group, instead of all devices. |
| **Icon** | Choose the notifications icon |
| **Sound** | Choose the notifications sound |
