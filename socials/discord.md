---
description: List of the available moderation tools to manage the Discord server.
---

# Discord

## Managements

{% tabs %}
{% tab title="Commands" %}
#### Player Management

1. **!kick** 'user' 'reason'
2. **!ban** 'user' 'time' 'reason'
3. **!softban** 'user' 'time' 'reason'
4. **!tempban** 'user' 'time' 'reason'

5. **!mute** 'user' 'time' 'reason'
6. **!hardmute** 'user' 'time' 'reason' 
7. **!warn** 'user' 'reason'

#### Channel Management

1. **!purge**
   * **!purge** 'limit'
   * **!purge user** 'user' 'limit'
   * **!purge contains** 'limit' ****'content'
   * **!purge embeds** 'limit'
   * **!purge links** 'limit'
   * **!purge emoji** 'limit'
   * **!purge images** 'limit'

  
2. **!lockdown** '\#channel' 'time'

#### Revoke Actions

1. **!unban** 'user' 'reason'
2. **!unmute** 'user'
3. **!unlockdown** '\#channel'
{% endtab %}

{% tab title="Explaination" %}
#### Player Management

1. **!kick** **-** Kicks a user
2. **!ban** **-** Ban a user
3. **!softban** **-** Bans and immediately unbans a member to clear 48 hours of message history.
4. **!tempban -** Bans a user for the specified duration regardless if they're on the server or not.

5. **!mute** **-** Mute a member so they cannot type or speak, a time limit in minutes
6. **!hardmute -** Functions similar to mute, but removes all of the specified user's other roles. If the hardmute is temporary the roles will be given back upon it expiring. 
7. **!warn -** Warns a user

#### Channel Management

1. **!purge**
   * **!purge -** Purges the last howmany messages.
   * **!purge user -** Purges messages from the specified user.
   * **!purge contains -** Purges messages containing the specified substring.
   * **!purge embeds -** Purges messages with embeds.
   * **!purge links -** Purges messages that contain links.
   * **!purge emoji -** Purges messages that contain custom emoji.
   * **!purge images -** Purges messages with attachments or embeds

  
2. **!lockdown** **-**  Lockdowns a channel with an optional timer and message 
{% endtab %}
{% endtabs %}



