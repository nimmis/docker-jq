# Bundled jq

[![](https://images.microbadger.com/badges/image/nimmis/jq.svg)](https://microbadger.com/images/nimmis/jq "Get your own image badge on microbadger.com")

This container are a minimal container with jq installed. Used för remote script where jq is not avaliable or you can't install it localy

Using this container as the jq command, using the **-rm** throws the container when used

	docker inspect container | docker run -i --rm nimmis/jq .[0]

To make it more convinient you can define an alias

	alias jq='docker run -i --rm nimmis/jq'

Makes commands easy

	docker inspect nimmis/jq | jq .[0].Config.Labels

displays

```
{
  "maintainer": "nimmis <kjell.havneskold@gmail.com>",
  "org.label-schema.build-date": "2017-01-29T20:40:38Z",
  "org.label-schema.docker.dockerfile": "/Dockerfile",
  "org.label-schema.name": "jq bundled in a container",
  "org.label-schema.url": "https://www.nimmis.nu",
  "org.label-schema.vcs-ref": "28dac05",
  "org.label-schema.vcs-url": "https://github.com/nimmis/docker-jq.git"
}
```

