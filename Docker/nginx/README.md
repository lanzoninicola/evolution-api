O Portainer web não permite bind de arquivos locais (nginx.conf)

**Solução**: crie uma imagem customizada com o nginx.conf embutido

 # dockerfile

FROM nginx:latest
COPY nginx.conf /etc/nginx/nginx.conf

# bash to build the image and upload to the Docker Hub

docker build -t lanzoninicola/nginx-evolution:latest .
docker push lanzoninicola/nginx-evolution:latest

# public address

http://191.101.234.115:8088/

# REST API

https://doc.evolution-api.com/v2/api-reference/get-information