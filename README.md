# 📦 Docker - Apache HTTP Server (Website Simples)  

Este repositório contém uma configuração básica do Docker Compose para executar um servidor Apache com um website simples (arquivo `index.html`).

## 🚀 Como Usar

### Pré-requisitos
- Docker instalado ([Download Docker](https://www.docker.com/get-started))
- Docker Compose (normalmente incluso no Docker Desktop)

### Passos para Execução

1. **Inicie o container:**
   ```bash
   docker-compose up -d
   ```

2. **Acesse o site:**
   Abra no navegador:
   ```
   http://localhost
   ```

3. **Para parar o container:**
   ```bash
   docker-compose down
   ```

## 📂 Estrutura do Projeto
```
.
├── docker-compose.yml    # Arquivo de configuração do Docker Compose
└── website/
    └── index.html        # Arquivo HTML do site (pode ser personalizado)
```

## 🔧 Personalização
- Edite o arquivo `website/index.html` para alterar o conteúdo do site
- Adicione mais arquivos na pasta `website/` (eles serão servidos pelo Apache)

## ⚙️ Configuração do Docker Compose
O arquivo `docker-compose.yml` configura:
- Imagem oficial do Apache HTTP Server
- Mapeamento da porta 80 do host para a porta 80 do container
- Volume vinculado para o diretório `website` (permite edição em tempo real)

## 💡 Dicas
- Para ver os logs do Apache: `docker logs my-apache-app`
- Para acessar o container: `docker exec -it my-apache-app bash`
