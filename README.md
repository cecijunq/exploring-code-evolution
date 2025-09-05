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

1. Repositório selecionado: <URL_DO_REPOSITORIO_SELECIONADO_AQUI>
2. Gráfico selecionado: <IMAGEM_DO_GRAFICO_SELECIONADO_AQUI>
3. Explicação: <EXPLICACAO_AQUI>

# RESPOSTA DO EXERCÍCIO
Repositório selecionado: https://github.com/pytorch/pytorch.git
Gráfico selecionado:

Explicação:
PyTorch é um pacote Python amplamente usada para criar, treinar e implantar modelos de aprendizado profundo, sendo uma das bibliotecas mais populares na área de IA. Devido à sua popularidade, há um grande número de pessoas e de esforço aplicado para aprimorar o código da biblioteca e, como os usuários podem entrar em contato com os desenvolvedores desse pacote se eles encontrarem erros (conforme é mencionado da seção "Releases and Contributing" do README do repositório), quanto mais usuários tem, mais pessoas podem encontrar erros e sugerir mudanças, o que leva ao aumento desse esforço. Devido a isso, ao longo dos anos, é natural que o número de arquivos cresça, já que novas funcionalidades e funções podem ter sido adicionadas à biblioteca, ou, devido à refatoração, optou-se por separar códigos que antes num mesmo arquivo, em arquivos distintos.
Isso é evidenciado pela curva azul do gráfico apresentado acima, que indica o número de arquivos de produção presentes no repositório em cada ano, desde 2020. A curva está em constante crescimento, mostrando o trabalho constante dos desenvolvedores em aprimorar o pacote. Notamos, contudo, que entre 2024 e 2025, tal crescimento diminuiu, o que pode nos levar a pensar que o esforço de aprimoração diminuiu, o que fez que não fossem feitos avanços significativos no código. Contudo, não é possível afirmar isso com certeza, já que pode ser que os trabalhos de aprimoração nos anos anteriores criaram um ambiente com um código de qualidade, que não exige manutenções muito impactantes (no que tange ao número de arquivos disponíveis). A segunda curva apresentada se refere ao número de arquivos de teste presentes no repositório em cada ano. Observamos que, de 2020 a 2024, tal número cresceu constantemente, o que indica que os desenvolvedores adotam a boa prática de sempre realizar testes dos códigos antes de lançá-los, para garantir que o comportamento do programa está de acordo com o esperado, evitando a ocorrência de bugs que empobraçam a experiência do usuário. Contudo, de 2024 a 2025, há uma queda significativa no número de arquivos de testes, o que é um ponto de atenção, já que pode indicar que menos testes estão sendo feitos, o que não é o ideal e nem o esperado, já que deixa o programa mais suscetível de ter erros, que exigerão um maior esforço de manutenção e correção, o que aumenta muito os custos de desenvolvimento. Também há a possibilidade de que arquivos de testes de códigos antigos que não são alterados há muito tempo foram deletados (julgamento da aluna!) por questões de gerenciamento de arquivos, para manter apenas aqueles de fato usados. Mesmo que esse seja o caso, isso não é o ideal, pois, no futuro, caso esses códigos tenham que passar por alguma manutenção, erros podem ocorrer e terá que refazer tais arquivos.
