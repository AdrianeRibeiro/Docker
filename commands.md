# exercicio-volume
`sudo docker container run -p 8080:80 -v ${pwd}/not-found:/usr/share/nginx/html nginx`

`sudo docker container run -p 8080:80 -v ${pwd}/html:/usr/share/nginx/html nginx`

`sudo docker container run -d --name ex-daemon-basic -p 8080:80 -v ${pwd}/html:/usr/share/nginx/html nginx`

# first-build
`sudo docker image build -t ex-simple-build .`

`sudo docker container run -p 8080:80 ex-simple-build`

# build-args
// NO DIRETÓRIO DA PASTA EXECUTAR

`sudo docker image build -t ex-build-arg .`

`sudo docker container run ex-build-arg bash -c 'echo $S3_BUCKET'`

`sudo docker image build --build-arg S3_BUCKET=myapp -t ex-build-arg .`

`sudo docker container run ex-build-arg bash -c 'echo $S3_BUCKET'`

# build-copy
`sudo docker image build -t ex-build-copy .`

`sudo docker container run -p 8080:80 ex-build-copy`

# build-dev
`sudo docker image build -t ex-build-dev .`

`sudo docker container run -it -v $(pwd):/app -p 80:8000 --name my-python-server ex-build-dev`

# node-mongo-compose
`sudo docker-compose up`