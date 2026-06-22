```yaml
name: Meu Primeiro Robo CI/CD

# Quando este robô deve acordar?
on:
  push:
    branches: [ "main" ]

# O que ele deve fazer?
jobs:
  construir_e_testar:
    runs-on: ubuntu-latest # O robô vai usar um computador Linux virtual da Google/Microsoft

    steps:
      - name: Passo 1 - Puxar o código
        uses: actions/checkout@v3

      - name: Passo 2 - Executar Teste de Qualidade
        run: echo "O código está perfeito! Iniciando a preparação para o servidor..."

      - name: Passo 3 - Simular o Deploy (Lançamento)
        run: echo "Código enviado com sucesso para a Internet! 🚀"
