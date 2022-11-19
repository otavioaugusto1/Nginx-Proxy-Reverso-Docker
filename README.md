# Nginx-Proxy-Reverso-Docker
Exemplo de Proxy Reverso utilizando Nginx + Docker + PHP APP.

Passo a passo para buildar e rodar as imagens:
# Na raiz do projeto, faça:
  ## Build da imagem Laravel: docker build -t otavioaugusto1/laravel:prod laravel/ -f laravel/Dockerfile.prod
  ## Build da imagem Nginx: docker build -t otavioaugusto1/nginx:prod nginx/ -f Dockerfile.prod
  
# Rodando as imagens:
 ## Imagem Laravel: docker run -d --name nginx --network laranet -p 8080:80 otavioaugusto1/nginx:prod
 ## Imagem Nginx: docker run -d --name nginxProxyReverso --network laranet -p 8080:80 otavioaugusto1/nginx:prod
 
# Navegador:
 ## Basta abrir o navegador de sua preferência e executar: localhost:8080 ou 0.0.0.0:8080
