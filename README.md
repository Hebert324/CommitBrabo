# Guia do Commit Brabo

```
- Mano, o que este commit "anything" faz?
- Sei não, abre ai pra ver.
- Pô cara assim não da...
```

E ruim quando isso acontece né? então fiz um guia top para deixar os commit melhores e mais padronizados

Sem um padrão seu `git log` vira uma Bagunça.

Vamos melhorar isso, veja os principais pontos:

- Manter um padrão dos commits entre a equipe.
- Colocar o contexto da mudança que foi feita.
- Deixa a navegação mais fácil e simplificada pelo histórico de commits.
- Este padrão vai ajudar a manutenção de um projeto em longo prazo.
- Facilitar a geração de `changelog`

## Como fazer este `log` brabo?

O time tem que concordar e alinhar estes seguintes parâmetros:

**Estilo**: Sintaxe, Gramática, Capitalização, Pontuação, Espaços. Ajuste qual vai ser o padrão de estilo do commit e deixe tudo o mais simples possível.

**Conteúdo**: Qual tipo de mensagem deve conter no corpo do commit? em quais situações tem que ter mensagem ou não?

**Metadata**: Como devemos rastrear as referencias das issues, por IDs, pull request ou algum outro jeito...

Depois de tudo que falei acima, você gostaria de ver um log assim:

<p align="center">
  <img src="https://github.com/Hebert324/CommitBrabo/blob/main/docs/commit_bom.png" alt="Um log de commit top">
</p>

ao invés de um log assim:

<p align="center">
  <img src="https://github.com/Hebert324/CommitBrabo/blob/main/docs/commit_ruim.png" alt="Um log de commit RUIM Demais">
</p>

## Estrutura do Commit Brabo

Vou te passar um modelo que estou começando a utilizar e vejo que ele e muito bom:

_Formato Brabo_

```
<tipo>(escopo): assunto

<corpo>

<rodapé>
```

## Tipo

Os valores permitidos para o `tipo` são, obs: utilizo emojis para deixar mais estilizado o commit:

- ✨feat _(Implementação de uma nova funcionalidade, feature, tela, opção de ação...)_
- 📝style _(Refatoração de indentação, vírgulas ausentes, otimização de imports, não confundir com CSS.)_
- ⚙️refactor _(Refatoração/melhoria de código sem alterar as funcionalidades, exemplo: renomear uma variável ou função...)_
- 🛠️test _(Adicionar/refatorar testes. Apenas testes.)_
- 🛡️fix _(Correção de algum bug do projeto.)_
- 📂docs _(Mudanças na documentação do projeto.)_
- 📘chore _(Alterações em arquivos de configuração do projeto ou do ambiente. Logs, pacotes, dependências e etc.)_

### Assunto

- Deve conter no Máximo de 50 caracteres.
- Os Tipos e o escopo devem estar em letra minúscula: `<test>(sum)`.
- Não deve conter ponto final.
- Assunto deve estar no _imperativo_, ou seja descreva o que um commit faz, ao invés de o que ele fez.

Exemplo:

`✨feat(userInfo): adiciona Modal para editar informações do usuário`.

## Corpo

Nem todo commit precisa de um corpo, se o título do seu commit já explica e deixa claro a intenção dele então pode descartar o corpo.

- Quando necessário utilizar o corpo tente colocar nele `o que` e o `por que` ao invés de `como` foi feito.
- Tente utilizar no máximo de 80 caracteres.
- Tente ser objetivo ao explicar o que e o por que das mudanças.

Exemplo:

```
refactor(userInfo): modifica a chamada do Modal.

A chamada anterior sofreu alterações de contrato, logo, foi necessário refatorá-la.

```

### Rodapé

Basicamente, um indicador de metadados. Aqui você referencia quais issues estão relacionadas, qual issue este commit encerra, ou caso utilize algum outro tipo de tarefa pode colocar aqui.

```
refactor(userInfo): modifica a chamada do Modal.

A chamada anterior sofreu alterações de contrato, logo, foi necessário refatorá-la.

Tarefa Finalizada: #123
Ver também: #456, #789
```

## Links

Sobre este conteúdo acima, retirei algumas informações destes links, fiz algumas mudanças obviamente, mas a inspiração para criar este guia veio daqui:

- [Karma Commit Messages](http://karma-runner.github.io/1.0/dev/git-commit-msg.html)
- [Guia do Commit Amigão](https://github.com/Hebert324/frontend-vaga-teste/tree/main/docs/commits)
