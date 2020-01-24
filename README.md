# Phish-Composer
Phish-Composer is a docker-compose project inteded to spin up three docker images often used together for phishing. The individual components of this infra are GoPhish, Evilginx2, and Postfix, as are [detailed in this blog post](http://lockboxx.blogspot.com/2018/12/gophish-evilginx2-for-phishing.html). The following are the docker containers used to wrap each of the individual projects:

  - [scottg88/gophish](https://hub.docker.com/r/scottg88/gophish/dockerfile/)
  - [warhorse/evilginx2](https://hub.docker.com/r/warhorse/evilginx2/dockerfile)
  - [mwader/postfix-relay](https://hub.docker.com/r/mwader/postfix-relay/dockerfile)
 

Read more about this project here, which explains some more of the theory behind this deployment as well as some key configuration files in the deployment.


Execution example:
```sh
sudo docker-compose up -d
sudo docker ps
# Attach to evilginx2
sudo docker attach `docker ps | grep evilginx2 | cut -d ' ' -f1`

```
