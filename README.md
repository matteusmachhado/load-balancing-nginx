# Load Balancing com Nginx

Este projeto implementa um balanceamento de carga utilizando Nginx para distribuir tráfego entre três réplicas de uma WebAPI .NET 8, utilizando o algoritmo de Round Robin para garantir a distribuição equilibrada das requisições.

## 🚀 Tecnologias

- .NET 8: Utilizado para desenvolver a WebAPI.
- Nginx: Servidor web e balanceador de carga.
- Docker & Docker Compose: Utilizados para orquestração de containers.
- Docker Desktop ou Rancher Desktop.

## 📋 Pré-requisitos

- Git
- Visual Studio 2022
- Docker

## 🛠️ Instalação

1. Clone este repositório:

   git clone [https://github.com/matteusmachhado/load-balancing-nginx.git](https://github.com/matteusmachhado/load-balancing-nginx.git)

2. Navegue até o diretório do projeto:

```
   cd [diretorio]\load-balancing-nginx\docker
```

3. Suba os serviços com o Docker Compose:

```
   docker-compose up -d --build
```

 ✔ Network docker_load-balancing  Created                                                                                                                                         
 ✔ Container docker-web-api-3     Started                                                                                                                                          
 ✔ Container docker-web-api-2     Started                                                                                                                                          
 ✔ Container docker-web-api-1     Started                                                                                                                                          
 ✔ Container load-balancing       Started 

   Isso criará três réplicas da WebAPI e configurará o Nginx como balanceador de carga.

   ![image](https://github.com/user-attachments/assets/a8748eee-6359-434c-8661-374131c7b7cf)


5. Acesse a API através do Nginx:

   Abra seu navegador e vá para http://localhost:5001/swagger/index.html

  ![image](https://github.com/user-attachments/assets/dc6b4063-23bc-47b2-9942-62ebd1c7d352)

 O Nginx estará distribuindo as requisições entre as três réplicas.

 ![test-load-balancing-nginx](https://github.com/user-attachments/assets/1b91831a-4f53-458f-9561-78e576f0dd4c)

## Colaboradores

- Mateus Machado - Criador e Mantenedor
