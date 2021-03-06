# Creating Bot Users

In order to talk to your chat bot there must be a bot user pre-configured on the Rocket.Chat server.

## Creating a User on the Server

An admin user is required to create the account for the bot to login to.

1. From **Administration** > **Users** menu
2. Select `+` to make a new user
3. Enter *Name*, *Username*, *Email* (tick verified) and *Passwword*
4. Disable *Require password change*
5. Select `bot` from role selection and click *Add Role*
6. Disable *Join default channels* recommended, to avoid accidental listening
7. Disable *Send welcome email*
8. *Save*

Your bot will be configured to login to Rocket.Chat server with the designated bot username and password by using these credentials in the bot's environment `ROCKETCHAT_USER` and `ROCKETCHAT_PASSWORD`

Note that for bots email, a common workaround to avoid creating multiple accounts is to use gmail +addresses, e.g. `youremail+botnam@gmail.com`.
[See this issue for more](https://github.com/RocketChat/Rocket.Chat/issues/7125)

## Talk to your bot

Your bot will respond to all messages addressed directly to the bot user, i.e. prepended with `<bot_name>` or a preconfigured `<bot_alias>`.

If the chat bot is configured to listen on Direct Messages ```RESPOND_TO_DM=true```, the prepend is not neccessary and the chat bot will respond to all messages in the DM channel.