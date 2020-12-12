# homeassistant

## devops

### for chromebook
- install docker
  - https://itnext.io/install-docker-on-pixelbook-chromeos-24fc898451e1
    - `sudo apt-get -y install apt-transport-https ca-certificates software-properties-common gnupg2`
    - ```bash
      curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
      sudo apt-key fingerprint 0EBFCD88
      sudo add-apt-repository “deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable”
      sudo apt-get update
      ```
    - `sudo apt-get -y install docker-ce || exit 1`
- `sudo docker pull homeassistant/home-assistant`
- run the container with auto restart
  - https://www.home-assistant.io/docs/installation/docker/
  - `sudo docker run -d --name="home-assistant" -v
 /home/bradyasheehan/homeassistant:/config -v /etc/localtime:/etc/localtime:ro --net=host homeassistant/home-assistant:stable`
- Naviate to http://localhost:8123/
