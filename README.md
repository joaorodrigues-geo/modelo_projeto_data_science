# Título do projeto

*One-line English summary: what was analysed and the main result.*

![Gráfico principal](relatorios/imagens/principal.png)

**Resultado principal:** uma frase com o número mais importante.

## Objetivo

Que pergunta o projeto responde e porque interessa (2–3 frases).

## Dados

Resumo dos dados usados. A lista completa, com fonte, data e licença, está em [`referencias/02_fontes.md`](referencias/02_fontes.md); o significado de cada coluna, em [`referencias/01_dicionario_de_dados.md`](referencias/01_dicionario_de_dados.md).

## Método

1. Limpeza e preparação (`notebooks/01-jr-...`)
2. Análise exploratória (`notebooks/02-jr-...`)
3. Modelo e validação (`notebooks/03-jr-...`): como se separaram treino e teste e que métricas se usaram.

## Resultados

Tabela ou gráficos com os números principais.

## Limitações

- O que os dados não permitem concluir.
- Fontes de erro conhecidas.

## Como reproduzir

```bash
conda env create -f ambiente.yml
conda activate nome-do-projeto
jupyter lab
```

Os dados brutos não estão no repositório: descarregar para `dados/brutos/` a partir das fontes indicadas.

## Organização

```
├── ambiente.yml        ambiente conda para reproduzir a análise
├── dados/
│   ├── brutos/         originais, nunca editados (fora do Git)
│   ├── intermedios/    gerados pelos notebooks (fora do Git)
│   └── processados/    tabelas finais (no Git)
├── modelos/            modelos treinados e resumos
├── notebooks/          numerados: 01-jr-descricao.ipynb
│   └── src/            config.py (caminhos), graficos.py (estilo e cores)
├── R/                  versão em R, quando existir
├── referencias/        dicionário de dados e fontes
└── relatorios/
    └── imagens/        gráficos para o README e relatórios
```

## Licença

Código: MIT. Os dados mantêm a licença de cada fonte (ver `referencias/02_fontes.md`).

---

<sub>Estrutura inspirada no [Cookiecutter Data Science](https://cookiecutter-data-science.drivendata.org/) e no [modelo de Francisco Bustamante](https://github.com/chicolucio).</sub>

<!--
COMO USAR ESTE MODELO (apagar este bloco no projeto novo)
1. No GitHub: "Use this template" → nome do projeto → criar.
2. git clone do repositório novo.
3. Em ambiente.yml, mudar "name:"; depois: conda env create -f ambiente.yml
4. Mudar o nome do notebook de exemplo; apagar dados/processados/exemplo.csv.
5. Ajustar caminhos em notebooks/src/config.py.
6. Preencher referencias/01_dicionario_de_dados.md e 02_fontes.md.
7. Preencher este README. Copiar .env.exemplo para .env só se houver chaves (nunca vai para o Git).
-->
