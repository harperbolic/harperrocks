---
title: "Como sh pode salvar a sua pele"
description: Durante a correria do dia a dia acabamos nos estressando, porém existem maneiras de aliviar essa sobrecarga.
slug: como-sh-pode-salvar-a-sua-pele 
date: 2024-11-25T14:35:28-03:00
image: banner.jpg
categories:
   - Linux
hidden: true
comments: false
draft: true
license: false
---

## Introdução

Shell script é um tipo de arquivo de sistemas unix-like, que tem o objetivo de ser interpretado por um shell. Além de ter todas as utilidades tradicionais de uma linguagem de script, ele se destaca por estar integrado com o sistema operacional, o que permite que automações sejam feitas de maneira muito mais rápida e eficiente.

## Bash (Bourne-Again SHell)

O Bash se destaca por ser o shell padrão na maior parte das distribuições GNU/Linux, concebido como uma evolução retro-compatível do clássico Bourne Shell (sh).

### Características de um arquivo .sh

A primeira etapa para um arquivo de shell scripting, é indicar ao sistema o local do interpretador desejado, no nosso caso o Bash. Isso é indicado pelo símbolo chamado de shebang (#!)

```#!/bin/bash```

Após isso, tudo que funcionaria no seu terminal funciona dentro do shell script. Desde comandos famosos do sistema como grep e ls, até comandos próprios ou baixados de repositórios.

### Palavras reservadas

#### Variáveis

Como diversas linguagens de script, Bash não é uma linguagem tipada. Uma variável pode ser declarada simplesmente com um nome e o valor a ser recebido, sem a necessidade de ponto e vírgula.

```
name = "puppyslut"

bitches = 1

isEstrogenized = true
```

Preste atenção que, por mais que variáveis sejam declaras dessa maneira, ao utiliza-las em outros comandos devemos colocar o símbolo $ antes delas para indicar a variável.

#### Estrutura condicional

A estrutura condicional é um dos aspectos mais quirkies do Bash, uma estrutura condicional pode ser indicada da seguinte forma:

```
if [[ "$name" == "puppyslut" && "$isEstrogenized" == true]]
   bitches = 0
fi
```

Existem diversos tipos de flags e operadores, alguns incomuns em outras linguagens, que podem ser encontrados no final da página.

#### Estrutura condicional composta

A estrutura condicional composta permite com que caso uma condição não seja satisfeita, uma segunda seja testada.

```
if [[ "$name" == "puppyslut" && "$isEstrogenized" == true]]
   bitches = 0
elif [[ -z "$name" ]]
   bitches = 1
```

## 

## Extra

### Condições

```
[[ -z STRING ]]			Checa se uma string está vazia
[[ -n STRING ]]			Checa se uma string não está vazia
[[ STRING == STRING ]] 		Igual (string)
[[ STRING != STRING ]] 		Diferente (string)

[[ NUM -eq NUM ]]   		Igual (numeral)
[[ NUM -ne NUM ]]		Diferente (numeral)
[[ NUM -lt NUM ]]		Menor que
[[ NUM -le NUM ]]		Menor ou igual que
[[ NUM -gt NUM ]]		Maior que
[[ NUM -ge NUM ]]		Maior ou igual que

[[ STRING =~ STRING ]]		Regex
(( NUM > NUM ))	    		Condição numérica

[[ -o noclobber ]]		Se OPTIONNAME está habilitado
[[ ! EXPR ]]			Negação
[[ X && X ]]			Conjunção
[[ X || Y ]]			Disjunção
```

Condicionais de arquivos:

```
[[ -e FILE ]]			Se arquivo existe
[[ -r FILE ]]			Se tem permissão de leitura
[[ -h FILE ]]			Symlink
[[ -d FILE ]]			Diretório
[[ -w FILE ]]			Se tem permissão de escrita
[[ -s FILE ]]			Tamanho maior que 0 bytes
[[ -f FILE ]]			Arquivo
[[ -x FILE ]]			Executável
[[ FILE1 -nt FILE2 ]]		Se arquivo 1 é mais recente que 2
[[ FILE1 -ot FILE2 ]]		Se arquivo 2 é mais recente que 1
[[ FILE1 -ef FILE2 ]]		Se arquivos iguais
```
