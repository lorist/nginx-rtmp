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

