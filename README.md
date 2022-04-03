# rotten-potatoes

## Configuração

MONGODB_DB => Nome do database

MONGODB_HOST => Host do MongoDB

MONGODB_PORT => Posta de acesso ao MongoDB

MONGODB_USERNAME => Usuário do MongoDB

MONGODB_PASSWORD => Senha do MongoDB

---

# Comandos mais utilizados

### Comandos DOCKER:
Criar build da imagem:
- `docker build -t caiuzu/rotten-potatoes:v1.0.0 .`

Subir imagem para dockerhub:
- `docker push caiuzu/rotten-potatoes:v1.0.0`

Criar tag para ultima versão:
- `docker tag caiuzu/rotten-potatoes:v1.0.0 caiuzu/rotten-potatoes:latest`

Subir imagem para dockerhub:
- `docker push caiuzu/rotten-potatoes:latest`

---

###Comandos K8S:
Criar cluster com X servers e agents com port bind em porta 30000:
- `k3d cluster create meucluster --servers 3 --agents 3 -p "8080:30000@loadbalancer"`

Executar o manifesto:
- `kubectl apply -f deployment.yml`

Listar clusters:
- `k3d cluster list`

Listar pods:
- `kubectl get pods`

Deletar cluster:
- `k3d cluster delete meucluster`
