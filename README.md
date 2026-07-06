# Template LaTeX - Artigo Padrão SBC

Este repositório contém um template modular em LaTeX formatado de acordo com as diretrizes da **Sociedade Brasileira de Computação (SBC)**. 

O projeto foi estruturado para facilitar a escrita de artigos científicos e trabalhos acadêmicos, isolando a formatação do conteúdo e organizando seções, figuras e referências em diretórios separados. É ideal para editores como o TeXstudio.

## 🗂️ Estrutura do Projeto

O projeto utiliza uma arquitetura de múltiplos arquivos para manter o código limpo e organizado:

```text
📂 template-artigo-abnt
├── 📁 figuras/               # Diretório para imagens e gráficos (ex: .png, .jpg, .pdf)
├── 📁 secoes/                # Arquivos .tex individuais para cada parte do artigo
│   ├── 1-introducao.tex
│   ├── 2-referencial.tex
│   ├── 3-metodologia.tex
│   ├── 4-resultados.tex
│   └── 5-conclusao.tex
├── 📄 main.tex               # Arquivo mestre que orquestra o documento
├── 📄 referencias.bib        # Banco de dados de referências no formato BibTeX
├── 📄 sbc-template.sty       # Arquivo de estilo visual (obrigatório da SBC)
└── 📄 sbc.bst                # Estilo de formatação da bibliografia (obrigatório da SBC)
```

## 🚀 Como Utilizar

### Pré-requisitos

- Uma distribuição LaTeX instalada (como TeX Live ou MiKTeX).
- Editor de LaTeX de sua preferência (recomendado: TeXstudio).

### Compilação no TeXstudio

Para garantir que o sumário, as referências cruzadas e as citações bibliográficas sejam geradas corretamente, certifique-se de que o arquivo main.tex esteja definido como o Documento Mestre e siga o ciclo de compilação:

1. F5 (Build & View) - Processa o texto base.
2. F8 (Bibliography) - Extrai e formata os dados do arquivo .bib.
3. F5 (Build & View) - Insere as referências no documento.
4. F5 (Build & View) - Alinha paginação e links cruzados.

***Aviso: Nunca remova os arquivos sbc-template.sty e sbc.bst da raiz do projeto, pois o compilador depende deles para aplicar as normas da SBC.***

## ✍️ Inserindo Figuras e Citações

### Para imagens: 

O projeto utiliza o pacote graphicx. Coloque suas imagens na pasta /figuras e referencie o caminho relativo de forma simples:

```latex
\includegraphics[width=0.8\textwidth]{./figuras/nome-da-imagem.jpg}
```

### Para citações: 

Utilize as chaves cadastradas no seu arquivo *referencias.bib* através do comando padrão 

```latex
Bala bla bla \cite{chave_do_autor}.
```
