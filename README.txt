# Repositório Compartilhado — Simulação de Fluxo de Equipe Real

## Sobre o projeto
Este repositório dá continuidade à Atividade Básica da disciplina de Design Profissional, aplicando o fluxo de trabalho colaborativo usado por times profissionais: branches individuais, Pull Requests com revisão entre colegas, resolução de conflitos de merge, Issues e versionamento com tags.

## Integrantes
- Pedro Henrique Sigismundo (@pedrohs-cdc)
- Luis Otavio Ferreira da Silva (@LuisFCyber)
- Edney Araujo da Silva (@UniEdney)
- Iago Matos Vieira (@yatokkj)
- Marcelo Teixeira de Almeida (@MarceloTeixeira0836)

## Fluxo de trabalho adotado

### 1. Branches individuais
Cada integrante criou seu próprio branch a partir do `main`, seguindo o padrão:

```
feature/nome-da-pessoa
```

### 2. Commits e Pull Requests
Cada integrante:
- Fez ao menos 1 alteração no projeto dentro do próprio branch.
- Enviou o branch ao GitHub (`git push`).
- Abriu um Pull Request do seu branch para o `main`.

**Pull Requests abertos e mesclados:**

| PR | Título | Autor |
|----|--------|-------|
| #9  | Feature/pedrosigismundo | Pedro |
| #10 | Pull do marcelo | Marcelo |
| #11 | Alteração redme Luis | Luis |
| #12 | Redmi Iago | Iago |
| #13 | Deixando apenas meus dados | Edney |

Todos os Pull Requests foram revisados e comentados por outro integrante do grupo (não pelo próprio autor) antes de serem mesclados ao `main`.

### 3. Conflito de merge
Durante o desenvolvimento, o branch `feature/pedrosigismundo` divergiu do repositório remoto por alterações simultâneas no arquivo `README.txt`. Ao tentar enviar o branch com `git push`, o Git identificou que o histórico remoto continha mudanças que não existiam localmente, gerando um conflito.

**Como foi resolvido:**
1. Execução de `git pull origin feature/pedrosigismundo`, que trouxe as alterações remotas e sinalizou o conflito diretamente no arquivo `README.txt`.
2. Edição manual do arquivo, mantendo o conteúdo relevante de ambas as versões e removendo as marcações de conflito (`<<<<<<<`, `=======`, `>>>>>>>`).
3. Commit da resolução: `git commit -m "resolve conflito no README"`.
4. Envio do branch atualizado com `git push --set-upstream origin feature/pedrosigismundo`.

O Pull Request correspondente foi então revisado por outro integrante e mesclado normalmente ao `main`.

### 4. Issues
Foram abertas Issues no repositório, descrevendo melhorias futuras para o projeto:

- **#7** — Adicionar seção de instruções de instalação no README
- **#8** — Criar página de perfil dos integrantes

### 5. Versionamento
Após todos os Pull Requests serem mesclados ao `main`, foi criada a tag `v1.0` no commit final e publicada no GitHub, marcando a primeira versão estável do projeto.

### 6. Organização
Todos os branches já mesclados (`feature/pedrosigismundo`, `feature/Marcelo`, `feature/luis`, `feature/Iago`, `feature/edney`) foram deletados, tanto localmente quanto no repositório remoto, mantendo o repositório limpo.

## Comandos utilizados

```bash
# Criar e mudar para o branch individual
git checkout -b feature/nome-da-pessoa

# Enviar o branch ao GitHub pela primeira vez
git push -u origin feature/nome-da-pessoa

# Após o Pull Request ser mesclado, atualizar o main local
git checkout main
git pull origin main

# Criar e enviar a tag de versão
git tag v1.0
git push origin v1.0

# Deletar branch local e remoto já mesclado
git branch -d feature/nome-da-pessoa
git push origin --delete feature/nome-da-pessoa
```

## Resumo da entrega

| Critério | Status |
|---|---|
| Branch individual por integrante | Concluído |
| Commits mínimos (2 por pessoa, 6 no total) | Concluído |
| Push e Pull Request aberto por todos | Concluído |
| PRs revisados por outro integrante | Concluído |
| Conflito de merge provocado e resolvido | Concluído |
| Issues com descrições claras (mín. 2) | Concluído |
| Tag v1.0 criada após todos os merges | Concluído |
| Branches mesclados deletados | Concluído |