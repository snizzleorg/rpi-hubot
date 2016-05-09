# rpi-hubot

[Raspberry Pi][raspberrypi] compatible [Docker][Docker] Image with a minimal [Hubot][hubot] chat bot. 

rpi-hubot is a chat bot built on the [Hubot][hubot] framework. It was initially generated by [generator-hubot][generator-hubot], and configured to be deployed in a [Docker][docker] container on a [Raspberry Pi][raspberrypi] to get you up and running as quick as possible.

## Building the docker image

    $ docker build -t matthiasg/rpi-hubot .

## Run hubot locally

    $ docker run -i -t matthiasg/rpi-hubot

## Run hubot on Slack

First, set HUBOT_SLACK_TOKEN environment variable. E.g.:

    $ export HUBOT_SLACK_TOKEN="your-hubot-slack-token"
    
For optional use of [hubot-microsoft-translato](https://www.npmjs.com/package/hubot-microsoft-translator) set also these additional environment variables:

    $ export HUBOT_MICROSOFT_TRANSLATOR_CLIENT_ID="your_microsoft_translator_client_id"
    $ export HUBOT_MICROSOFT_TRANSLATOR_CLIENT_SECRET="your_microsoft_translator_client_secret"

Then run hubot on slack:

    $ docker run -d --env HUBOT_SLACK_TOKEN --env HUBOT_MICROSOFT_TRANSLATOR_CLIENT_ID --env HUBOT_MICROSOFT_TRANSLATOR_CLIENT_SECRET matthiasg/rpi-hubot slack

## Credits

- [Kenji Doi (knjcode)'s rpi-hubot-docker-template](https://github.com/knjcode/rpi-hubot-docker-template)
- [Docker Pirates ARMed with explosive stuff (hypriot)](http://blog.hypriot.com/)
- [hypriot/rpi-node](https://hub.docker.com/r/hypriot/rpi-node/)

[hubot]: http://hubot.github.com
[generator-hubot]: https://github.com/github/generator-hubot
[docker]: https://www.docker.com/
[raspberrypi]: https://www.raspberrypi.org/