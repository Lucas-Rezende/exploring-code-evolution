# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas linguagens Python, JavaScript, TypeScript e Java, e gera relatórios `HTML` como [este](https://andrehora.github.io/gitevo-examples/python/pandas.html).

Mais exemplos de relatórios podem ser podem ser encontrados em https://github.com/andrehora/gitevo-examples.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

> [!NOTE]
> Antes de instalar a ferramenta, é recomendado criar e ativar um [ambiente virtual Python](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#create-and-use-virtual-environments).

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
$ pip install gitevo
```

Execute a ferramenta no repositório selecionado utilizando o comando abaixo (ajuste conforme a linguagem do repositório).
Substitua `<git_url>` pela URL do repositório que será analisado:

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r javascript <git_url>

# TypeScript
$ gitevo -r typescript <git_url>

# Java
$ gitevo -r java <git_url>
```

Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

> [!NOTE]
> Essa etapa pode demorar alguns minutos pois o projeto será clonado e analisado localmente.

# Passo 3: Explorar o relatório de evolução de código

Após executar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), é gerado um relatório `HTML` contendo diversos gráficos sobre a evolução do código.

Abra o relatório `HTML` e observe com atenção os gráficos.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo
- Detalhar se as curvas estão de acordo com boas práticas
- Explicar grandes alterações nas curvas
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- etc.

Seja criativo!

# Instruções para o exercício

1. Crie um `fork` deste repositório (mais informações sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Adicione o relatório `HTML` no seu fork.
3. No Moodle, submeta apenas a URL do seu `fork`.

Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork:

**1. Repositório selecionado:** [https://github.com/zxing/zxing](https://github.com/zxing/zxing)

**2. Gráfico selecionado:**<br>
<img width="812" height="406" alt="lines_of_code" src="https://github.com/user-attachments/assets/c8ba2ba1-7e93-4cf2-ac31-49b2086146f8" />

---

### 3. Explicação

Apesar de parecer simples, o gráfico de linhas de código apresenta detalhes importantes sobre a história do projeto. Ele revela que houve um grande aumento de linhas nos primeiros anos de desenvolvimento e, nos últimos anos, o crescimento diminuiu e estagnou. Isso demonstra visualmente o estado atual do software: 

> *"The project is in maintenance mode, meaning, changes are driven by contributed patches."*

Essa característica é visível na grande inclinação que a curva possui nos primeiros 4 anos de projeto. Ademais, os *commits* mais recentes corroboram com essa informação, pois seus títulos são, majoritariamente, associados a atualizações de *plugins* e dependências, correções de erro, entre outros ajustes pontuais.

Dada a curva de crescimento, o código provavelmente seguiu boas práticas. O repositório chegou a um ponto em que poucas linhas de código são necessárias anualmente para manter o projeto não somente funcionando, mas continuando atrativo para os usuários.

Outro fator interessante é que a curva de evolução de outros parâmetros do projeto (files, production, classes declaration, methods) possui um comportamento semelhante à curva de evolução de linhas de código.
