# jekyll로 build된 _site 폴더를 가져와서 docker nginx로 돌리는 예제

## 방법
1. `cd C:\wducko\wducko.github.io`([https://github.com/wducko/wducko.github.io](https://github.com/wducko/wducko.github.io)) 를 `bundle exec jekyll serve` 해서 `_site` 폴더를 생성한다.

2. `_site` 폴더를 이 `cd C:\wducko\docker-blog` 폴더 안에 넣는다.

3. `docker-compose up -d` 하고 localhost 나 ip로 접속하면 된다.

## linux에 docker 설치 안 되어있는 경우

```
curl -s https://get.docker.com | sudo sh

apt-get -y install python-pip

sudo -H pip install --upgrade --ignore-installed pip setuptools

pip install docker-compose

docker -v

docker-compose -v
```

## 기존 nginx 삭제

```
sudo apt-get --purge remove nginx-*
```

## linux에 docker-compose 실행

```
git clone https://github.com/wducko/docker-blog.git

cd docker-blog

docker-compose up -d
```