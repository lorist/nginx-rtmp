# nginx-rtmp

This is a standard nginx-rtmp docker deployment.

It takes an RTMP stream and writes it to a volume.. The use case here is to use this as a target for Pexip Infinity VMRs. When used in conjunction with this docker container: https://github.com/lorist/watchdog recorded files can be automatically uploaded to a MediaCMS deployment.

## Instructions

```
git clone https://github.com/lorist/nginx-rtmp.git && cd nginx-rtmp
mkdir videos
chmod 777 videos
docker compose up -d
```

## MediaCMS notes

Setup dns to point to your docker host IP

git clone https://github.com/mediacms-io/mediacms && cd mediacms

chmod -R 777 mediacms/media_files

https://github.com/mediacms-io/mediacms/blob/main/docs/admins_docs.md#3-docker-installation

Edit localsettings.py and docker-comopse-letsencrypt.yaml to suit
docker compose -f docker-compose-letsencrypt.yaml up --detach


<img width="2048" alt="image" src="https://github.com/lorist/nginx-rtmp/assets/5859812/000a8632-15d7-426d-ad42-2963d6f95761">


