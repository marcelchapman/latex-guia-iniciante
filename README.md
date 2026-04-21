# latex-guia-iniciante
Guia prático de LaTeX para iniciantes (PT-BR)
# LaTeX para Iniciantes: Como Criar Documentos Acadêmicos do Zero

Este guia foi criado para ajudar iniciantes a sair do zero e produzir seu primeiro documento acadêmico em LaTeX de forma rápida e prática.

## Contexto
Muitos iniciantes encontram dificuldade ao começar com LaTeX por se tratar de uma linguagem técnica baseada em comandos, diferente de editores visuais tradicionais. Além disso, a maior parte dos materiais disponíveis em português é extensa e voltada a um uso acadêmico mais avançado, o que dificulta um início rápido e prático. Este guia propõe uma abordagem direta, com foco em quem precisa criar um documento acadêmico simples em pouco tempo, sem se aprofundar em recursos avançados.

## NotebookLM

Este projeto utilizou o NotebookLM como ferramenta de apoio para organização das fontes, testes de prompts e geração de materiais complementares, como infográficos, mapas mentais e flashcards.

Acesse o caderno completo: [https://notebooklm.google.com/notebook/675ab74c-4e14-4ece-90a9-a6773367350a]


## Objetivos

- Compreender a estrutura básica de um documento em LaTeX.
- Criar um documento básico em LaTeX a partir do zero.
- Aplicar comandos essenciais para a formatação do teto e a organização do documento.


## Curadoria de Fontes

1.	LaTeX – Leslie Lamport
Livro fundamental escrito pelo criador do LaTeX. Foi utilizado como referência principal para compreender a estrutura do sistema e os comandos básicos. Apesar de ser técnico em alguns pontos, oferece uma base sólida e confiável.
2.	Text and Math into LaTeX — Gratzer
Obra voltada a um público mais avançado, com forte foco em aplicações matemáticas. Foi utilizada como complemento para entender como o LaTeX é aplicado em contextos acadêmicos mais exigentes, embora não seja indicada para iniciantes.
3.	FreeCodeCamp (video)
Recurso prático utilizado para visualizar a aplicação real do LaTeX. Apresenta um passo a passo desde a criação de um documento até exemplos mais completos, sendo útil para reforçar o aprendizado inicial. 
4.	LaTeX in 24 Hours – Dilip Datta
Livro com proposta de aprendizado progressivo. Foi utilizado para compreender uma sequência estruturada de evolução no uso do LaTeX, do básico aos níveis intermediários.
5.	LaTeX Notes for Professionals – GoalKicker
Material direto e conciso, focado nos comandos essenciais. Ideal como referência rápida para iniciantes que precisam produzir um documento funcional sem aprofundamento teórico.


## Engenharia de Prompts e Aprendizados

Prompt 1:  
“Para quem o LaTeX é indicado?”
- Resultado:  
A resposta foi conceitual, focada no público-alvo da ferramenta.
- Problema:  
Apesar de correta, não contribuiu para o objetivo prático de construir um documento.
 
Prompt 2:  
“Como construir um documento básico em LaTeX?”
- Resultado:
A resposta apresentou orientações úteis e um exemplo simples de código.
- Problema:
O conteúdo ainda era genérico e não oferecia um modelo completo e diretamente utilizável.
 
Prompt 3:  
“Faça um documento modelo em LaTeX que contenha capa, índice, apresentação, seções, um parágrafo de texto e uma lista aninhada. Explique brevemente a função de cada parte.”
- Resultado:
A resposta gerou um modelo estruturado de documento, incluindo os principais elementos de um trabalho acadêmico.
- Melhoria:
O prompt passou a produzir um resultado prático e reutilizável, alinhado com o objetivo de criar um documento desde o início.


## Miniguia de Estudo

1.	O que é LaTeX?  
- LaTeX é um sistema de preparação de documentos voltado para textos acadêmicos e profissionais, amplamente utilizado por estudantes, professores e pesquisadores.
- Diferente de editores visuais, você escreve o conteúdo usando comandos e o sistema cuida da formatação.
- É especialmente útil para lidar com fórmulas matemáticas e para organizar referências e numerações de forma totalmente automática.

2.	Estrutura básica de um documento.  
- Um documento em LaTeX é dividido em duas partes principais: preâmbulo e corpo do documento.
- Preâmbulo: define configurações como tipo de documento, pacotes e metadados (título, autor).
- Corpo do documento: onde o conteúdo é escrito. 

Exemplo mínimo:

```latex
% --- PREÂMBULO ---
\documentclass{article}                  % Define o tipo de documento
\usepackage[utf8]{inputenc}              % Codificação de caracteres
\title{Título do Trabalho}
\author{Nome do Autor}

% --- CORPO DO DOCUMENTO ---
\begin{document}
\maketitle

Olá, mundo!

\end{document}
```

### 1. Elementos essenciais

Esses são os elementos mínimos para estruturar um documento simples:  
- Título e metadados  
Definidos no preâmbulo e exibidos com `\maketitle`. 

```latex
\title{Meu Documento}
\author{Autor}
\date{\today}
```
- Seções  
Utilizadas para organizar o conteúdo do documento. 

```latex
\section{Introdução}
Este é um parágrafo de exemplo.
```
- Texto simples  
Basta escrever diretamente no corpo do documento. 

```latex
Este é um texto simples em LaTeX.
```

### 2. Listas

No LaTeX, listas são criadas com os ambientes itemize (marcadores) e enumerate (numeração).  
- Use `\begin{...}` e `\end{...}` para definir o início e o fim da lista 
- Utilize `\item` para cada elemento 
- Para criar subníveis, basta inserir uma lista dentro de outra

Exemplo:

```latex
\begin{itemize}
    \item Frutas Tropicais:
    \begin{enumerate}
        \item Manga
        \item Abacaxi
    \end{enumerate}
    \item Legumes:
    \begin{enumerate}
        \item Cenoura
        \item Batata
    \end{enumerate}
\end{itemize}
```

- O LaTeX ajusta automaticamente o estilo e o recuo conforme o nível da lista


### 3. Compilação e erros comuns

A compilação de um arquivo .tex transforma o código em um documento final (geralmente PDF), utilizando compiladores como pdflatex.
- Em editores online, como o Overleaf, basta clicar no botão de compilação
- Em editores locais, é possível usar atalhos ou comandos no terminal, como: 

`pdflatex exemplo.tex`
	
Erros comuns:
  
- `Undefined control sequence`   
  - O que é: ocorre quando o LaTeX não reconhece um comando (erro de digitação ou pacote ausente) 
  - Como resolver: corrigir o comando ou incluir o pacote necessário com `\usepackage{...}` 
- `Missing $ inserted`
  - O que é: ocorre ao usar elementos matemáticos fora do modo matemático
  - Como resolver: envolver a expressão com `$...$`
  - Dica: compile o documento com frequência para identificar erros rapidamente 


## Glossário

- LaTeX: Sistema de composição de documentos baseado em comandos, que permite focar no conteúdo enquanto a formatação é automatizada.
- Preâmbulo: Parte inicial do arquivo (antes de `\begin{document}`), onde são definidas configurações, classe e pacotes.
- Corpo do documento: Conteúdo principal entre `\begin{document}` e `\end{document}`.
- Comando: Instrução iniciada por `\`, usada para formatar texto ou executar funções específicas.
- Ambiente: Estrutura definida por `\begin{}` e `\end{}`, usada para organizar elementos como listas e tabelas.
- Classe de documento: Definida por `\documentclass`, determina o tipo e o layout do documento.
- Pacote: Extensão carregada com `\usepackage{}`, que adiciona funcionalidades ao LaTeX.
- Modo matemático: Formato usado para escrever expressões matemáticas, geralmente entre `$...$`. 



## Prompts Reutilizáveis

- Gerar um modelo de documento acadêmico em LaTeX com capa, índice, seções, lista e conclusão
- Criar uma tabela simples em LaTeX
- Inserir uma imagem com legenda em LaTeX
- Escrever uma fórmula matemática em LaTeX (modo inline ou destacado)
- Adicionar uma seção de referências ou bibliografia em um documento LaTeX 

## Materiais Gerados

- Infográfico: [https://notebooklm.google.com/notebook/675ab74c-4e14-4ece-90a9-a6773367350a?artifactId=cdd69f27-6d60-45a1-a93f-6a865300ed34]
- Vídeo: [https://notebooklm.google.com/notebook/675ab74c-4e14-4ece-90a9-a6773367350a?artifactId=dc09735c-162f-4d01-a629-99149b923f1b]
- Flashcards: [https://notebooklm.google.com/notebook/675ab74c-4e14-4ece-90a9-a6773367350a?artifactId=27f0dd97-edbe-499a-8401-62dbc7f34cf8]


## Conclusão

Este projeto demonstrou a aplicação de IA como ferramenta de aprendizagem ativa, combinando curadoria de fontes, engenharia de prompts e organização do conhecimento para construir um guia prático de LaTeX.
