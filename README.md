# Slack Flow Steps
This Workflow contains an **Archive Channel** step for interacting with Slack.

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

# Pre-Requisites

- xMatters account - If you don't have one, [get one](https://www.xmatters.com)!
- Slack account

# Files

- [SlackSteps.zip](SlackSteps.zip)

# Example Usage
This flow shows the inbound HTTP Trigger on the left flowing into a switch step. Based on the state the flow will create a new xM Event for open or Breach, but for Closed will archive the associated Slack channel. 

The response trigger shows that Acknowledge will create a new channel, post a message, then invite several people to the new channel. For a breach, a VIP type is invited so they are aware. 

<kbd>
  <img src="/media/example_usage.png">
</kbd>
  
# xMatters Configuration

## Import the xMatters Workflow

1. Download the [SlackSteps.zip](SlackSteps.zip) file
2. Follow instructions for [Importing a workflow](https://help.xmatters.com/ondemand/xmodwelcome/workflows/manage-workflows.htm#ImportExport)

## Usage

### Archive Channel
The **Archive Channel** step is used for archiving channels that have been created. Handy for cleaning up all those channels that get created. 

<kbd>
  <img src="/media/archive.png">
</kbd>

The inputs are:
* **Channel Name** - The name or ID of the channel to archive
* **Throw error if not found?** - If the channel is not found, should we throw an error or ignore. This is helpful if there are flows that may not have created a channel as expected. So instead of building another step to see if the channel exists and then archiving, this will just continue happily if the channel is not found rather than throwing an error. 


### Invite Users
The **Invite Users** step is handy for inviting one or more users to a channel. 

<kbd>
  <img src="/media/invite.png">
</kbd>

The inputs are:
* **Channel Name** - The channel or ID to invite users to
* **Username** - The username, or a comma separated list of usernames to invite to the channel.

## Profit
Add the steps to your desired workflow. 


# Troubleshooting

[Get help using Flow designer](https://help.xmatters.com/ondemand/xmodwelcome/flowdesigner/flow-designer.htm)


