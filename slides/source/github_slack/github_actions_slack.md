
# Github Actions Release Automation

---
## 

<grid  drag="100 100" drop="center"  flow="col">
Why

<p style="font-size:24px">
Focus Friday - no standup meeting and friendly reminder from the team to update cross team slack channel when we release the kraken.
</p>

<p style="font-size:12px">
2 Espresso shots in and 15 tabs later we had the minor inconvenience of manually updating the slack channel topic automated.
</p>

![[source/github_slack/assets/Screenshot 2024-02-16 at 12.02.37 PM.png]]

</grid>

---

## Development

<p style="font-size:24px">
Very important to check out things to try and workout the problems
</p>

![[source/github_slack/assets/Screenshot 2024-02-16 at 1.01.47 PM.png]]


---

## 



<grid drag="90 20" drop="5 10">
Testing
<p style="font-size:32px">
CURL commands, Postman visualizer, Visual Studio Code + YAML linter + Github Actions extensions.
</p>

</grid>

<grid drag="25 55" drop="5 -10">
<p style="font-size:18px">
Parsing too much information from Github API using a CLI tool JQ. JQ online JSON parser playground
</p>

</grid>

<grid drag="25 20" drop="5 70" style="font-size:18px">

- [Github API docs](https://docs.github.com/en/rest/releases/releases?apiVersion=2022-11-28#get-the-latest-release)

- [JQ online JSON parser playground](https://github.com/jqlang/jq)
</grid>

<grid drag="60 55" drop="-5 -10">

![[source/github_slack/assets/Screenshot 2024-02-16 at 12.42.56 PM.png]]
</grid>

---


## Workflows





<grid drag="50 20" drop="5 70" style="font-size:24px">

### Slack Workflows

[Builder Automation (WebHook)](https://slack.com/shortcuts/Ft06KXCD5S72/bbaba72122c80e8f345cd0eaf003071d)


</grid>

<grid drag="50 20" drop="55 70" style="font-size:24px">

### Github Workflows

[GA slack-send](https://github.com/marketplace/actions/slack-send)

</grid>





---

## Releases

<p style="font-size:32px">
So whenever there's a new `Release` published by any team member it will trigger this automation to update the stakeholders (slack cross-team) channel with appropriate information.
</p>

![[source/github_slack/assets/Screenshot 2024-02-16 at 11.54.50 AM.png]]