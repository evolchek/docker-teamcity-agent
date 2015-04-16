[JetBrains TeamCity](https://www.jetbrains.com/teamcity/) build agent. No build tools included. See [teamcity-agent](https://registry.hub.docker.com/u/klikatech/teamcity-agent/) image for a real-life usage example.

## How to use the image

You should already have a TeamCity server running. See [teamcity](https://registry.hub.docker.com/u/klikatech/teamcity/) image description for details.

Run a build agent container:

```
docker run -d --name teamcity-agent --link teamcity:teamcity -e TEAMCITY_URL=http://teamcity:8111 -e AGENT_NAME=Default klikatech/teamcity-agent
```

The bootstrap script will automatically download and start a build agent.
