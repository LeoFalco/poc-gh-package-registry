# Monorepo

Poc para demonstrar um projeto usando

- Monorepo (vários pacotes dentro de um único repo git)
- lerna (para gerenciar os pacotes)
- github actions (para CI e CD)
- github package registry (publicação dos pacotes)
- husky (git hooks locais)
- commit-zen (mensagens de commits padronizadas)

## workflow

Ao fazer um commit na master (merge também conta) o github actions se encarrega de:

- instalar as dependências de todos os pacotes
- executar os testes
- incrementar a versão do pacote de acordo com o [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
- criar uma tag para a versão e fazer push
- publicar os pacotes github package registry
