# homeassistant

## devops

### for chromebook
- install docker
  - https://itnext.io/install-docker-on-pixelbook-chromeos-24fc898451e1
- `sudo docker pull homeassistant/home-assistant`
- run the container with auto restart
  - https://www.home-assistant.io/docs/installation/docker/
  - `sudo docker run -d --name="home-assistant" -v
 /home/bradyasheehan/homeassistant:/config -v /etc/localtime:/etc/localtime:ro --net=host homeassistant/home-assistant:stable`
- Naviate to http://localhost:8123/
