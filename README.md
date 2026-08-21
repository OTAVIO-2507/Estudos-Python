<div align="center">

# Estudos Python — Menu Interativo de Exercícios

Programa de console em Python com um menu interativo de 8 opções que reúne exercícios de fundamentos: manipulação de listas, cálculos de soma e média, tabuada, ordenação e tratamento de entradas do usuário.

![Python](https://img.shields.io/badge/Python_3-3776AB?style=flat-square&logo=python&logoColor=white)

</div>

## Visão geral

O programa roda em loop contínuo: a cada operação concluída, a tela é limpa e o menu principal é reexibido. Cada opção exercita um fundamento diferente da linguagem — funções, estruturas condicionais, laços, formatação de saída e validação de entradas — servindo como registro prático da evolução nos estudos de Python.

## Funcionalidades

- Exibição de listas de números e nomes pré-definidas
- Cálculo de idade a partir do ano de nascimento
- Geração de tabuada para qualquer número, inteiro ou decimal
- Ordenação da lista de números em ordem decrescente
- Cálculo de soma e média dos números da lista
- Tratamento de erros para opções e valores inválidos
- Limpeza de tela entre as operações

## Decisões de projeto

Algumas escolhas que não são óbvias pelo código:

**O retorno ao menu é recursivo, e isso tem custo.** `voltar_ao_menu_principal` chama `main()` outra vez em vez de devolver o controle a um laço. Funciona para uso interativo, porque ninguém navega fundo o suficiente para estourar a pilha, mas cada volta ao menu empilha mais uma chamada sem encerrar a anterior. Um `while True` dentro de `main` seria a forma que não acumula.

**Cada opção é uma função com nome próprio.** O menu não executa lógica: ele só despacha. Isso mantém cada exercício isolado e legível sozinho, que é o objetivo de um repositório de estudo — o arquivo serve para ser lido, não só executado.

## Tecnologias

| Tecnologia | Aplicação no projeto |
| --- | --- |
| Python 3 | Linguagem principal do programa |
| Funções e laços | Organização das opções do menu |
| Módulo `os` | Limpeza da tela do terminal |
| `try`/`except` | Validação de entradas do usuário |

## Como executar

Pré-requisito: Python 3 instalado.

```bash
git clone https://github.com/OTAVIO-2507/Estudos-Python.git
cd Estudos-Python
python exercicios.py
```

O menu interativo será exibido no terminal; escolha uma opção de 1 a 8.

## Estrutura do projeto

```
Estudos-Python/
├── exercicios.py   Programa completo (menu e exercícios)
└── README.md
```

