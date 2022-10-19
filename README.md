[![Docker Pulls](https://badgen.net/docker/pulls/cauachagas/conversao-temperatura?icon=docker&label=pulls)](https://hub.docker.com/r/cauachagas/conversao-temperatura/)
[![Docker Image Size](https://badgen.net/docker/size/cauachagas/conversao-temperatura?icon=docker&label=image%20size)](https://hub.docker.com/r/cauachagas/conversao-temperatura/)

# Projeto conversão de temperatura

### Sobre o projeto
O projeto conversão de temperatura é um projeto desenvolvido em NodeJS. O projeto tem como objetivo ser um exemplo para a criação de ambiente com containers usando NodeJS.

### Observações do projeto
A aplicação é exposta usando a porta 8080


### Rodar a aplicação com a imagem gerada neste repositório
Para rodar esta aplicação você pode utilizar

```bash
docker container run -d -p 8080:8080 cauachagas/conversao-temperatura
```

Desta forma ao acessar [localhost:8080](localhost:8080) você pode utilizar a aplicação.

![](https://drive.google.com/uc?export=view&id=1wmF_Fk-ShMIWrea5BBzz6w-5lDPF6r_J)


### Rodando com Kubernetes

Primeiro é preciso criar um cluster Kubernetes

```k3d cluster create meucluster -p "82:30001@loadbalancer"```

onde `meucluster` é o nome do cluster, onde a porta 82 da nossa máquina escuta a porta 30001 do cluster.

Depois é preciso navegar para src. Com o comando

`kubectl apply -f k8s/`

é criado a menor unidade Kubernetes, chamado de pod.

![](https://drive.google.com/uc?export=view&id=18pysr0_ZagrhKnB8mAxBdDMg-kHX8fff)