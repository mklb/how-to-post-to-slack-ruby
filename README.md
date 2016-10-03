# How to post to a Slack channel from your Ruby/Rails backend
## Setup & usage
1. Copy the 35 lines small, self explaining 'SlackNotifier' class and use it as follows
2. Go to: https://slack.com/apps/A0F7XDUAZ-incoming-webhooks, add the app to your slack team, setup the webhooks default channel and copy your webhook url
3. You are ready to post! Use the class as follows:

```ruby
# Initialize
# this notifier posts to your default channel which you setup in step 2)
notifier = SlackNotifier.new "YOUR-URL"
# or send to another channel with a username and icon
notifier = SlackNotifier.new "YOUR-URL", "#channel", "username", ":ghost:"

# send a message, returns a boolean
notifier.send 'Fancy text containing a cool link: <https://popflakeapp.com|Try me>'
```
## Dependencies
- [Httparty](https://github.com/jnunemaker/httparty)