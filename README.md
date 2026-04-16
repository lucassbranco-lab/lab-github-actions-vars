# Desafio GitHub Actions - Variáveis e Escopos

Este projeto demonstra o uso de variáveis em diferentes escopos no GitHub Actions, incluindo:

- Variáveis globais (env)
- Variáveis por job
- Variáveis por step
- Variáveis dinâmicas com GITHUB_ENV
- Variáveis padrão do GitHub
- Secrets e Variables do repositório

## Execução do Workflow

O workflow foi executado manualmente através da aba **Actions** do GitHub.

## Respostas

### Por que a Secret aparece como ***?
Porque o GitHub mascara automaticamente valores sensíveis nos logs por segurança, evitando vazamento de dados.

### O Job deploy_app consegue ler a variável BUILD_VERSION do build_app?
Não. Cada job roda em um ambiente isolado (runner diferente), então as variáveis não são compartilhadas automaticamente entre eles.
