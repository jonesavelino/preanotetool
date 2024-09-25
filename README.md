# PREAnoTeTool
PREAnoTeTool é um protótipo de software baseado na abordagem PREAnoTe e tem o objetivo de pré-anotar um corpus baseado em glossários, utilizando o metamodelo Command and Control Relations Metamodel (C2RM) da abordagem IDEA-C2 (https://github.com/jonesavelino/idea-c2-tool).

# Descrição do Projeto
Projeto de pesquisa acadêmica para pré-anotar corpora com o intuito de realizar o ajuste fino de modelo de linguagem pré-treinado. No final, é estruturado o conteúdo utilizado no ajuste fino do modelo através de um Knowledge Graph, representado por um grafo Resource Description Framework (RDF). 

# Fonte da Base de dados Textuais para Treinamento
- Glossário de Termos do EB (link: https://bdex.eb.mil.br/jspui/bitstream/123456789/298/1/C-20-1.pdf)
- Doutrinas militares (link: https://bdex.eb.mil.br/jspui/)

# Pré-requisito
Este projeto possui as seguintes dependências:

- [Python 3.10.12] (https://www.python.org/downloads/release/python-31012/) linguagem de programação para rodar as bibliotecas e desenvolvimento.
- [Google Colab Pro] é um ambiente que oferece  Notebooks cujo objetivo é rodar códigos escritos em Python.

# Bibliotecas: 
- [SpaCy 3.5] é uma biblioteca de aprendizado de máquina.  
- [Pipeline] pt_core_news_sm (https://spacy.io/models/pt)
- [Arquitetura] spacy-transformers.TransformerModel.v3 (https://spacy.io/universe/project/spacy-transformers)
- [Modelo de linguagem] neuralmind/bert-base-portuguese-cased (https://github.com/neuralmind-ai/portuguese-bert)
- [RDFLib] - Biblioteca em Python puro para trabalhar com RDF (extensões RDF, N3 e TTL)
- [Graphviz] - Biblioteca que permite visualizar os grafos RDF visualmente. (https://pypi.org/project/graphviz/)
- [PyPDF2] - Biblioteca PDF capaz de dividir, mesclar, cortar e transformar as páginas de arquivos PDF. (https://pypi.org/project/PyPDF2/)
- [PyDotPlus] - Biblioteca em Python com a evolução do pydot que fornece uma interface Python para a linguagem Dot do Graphviz. (https://pypi.org/project/pydotplus/)

# Experimento
- Para executar o experimento é importante seguir o passo a passo das ações do caderno do projeto.
- 1) Recuperar o Glossário de Termos do EB (link: https://bdex.eb.mil.br/jspui/bitstream/123456789/298/1/C-20-1.pdf)
- 2) Rodar as operações de:
- 2.1) Etapa 1: Pré-anotação - Recuperar o arquivo do Glossário e gerar arquivos JSONL para curadoria no Doccano; (Etapa_1_Pre-Anotacao.ipynb)
- 2.2) Etapa 2: Recuperar documentos curados no Doccano (JSONL) para gerar arquivo .SpaCy; (Etapa_2_Converter.ipynb)
- 2.3) Etapa 3: Avaliar a acurácia da pré-anotação, comparando uma fatia do corpus anotado manualmente com o pré-anotado; (Etapa_3_Accuracy.ipynb)
- 2.4) Etapa 4: Gerar os dados de JSONL para grafo RDF Turtle (.ttl) e realizar consultas por meio da linguagem SPARQL; (Etapa_4_Graph.ipynb)

# Agradecimentos
- Agradecemos ao CNPq - Conselho Nacional de Desenvolvimento Científico e Te\-cnológico, e ao IME - Instituto Militar de Engenharia, pelo apoio através de bolsa de iniciação científica (PIBIC Edital 2023/2024), e à FINEP/DCT/FAPEB (nº 2904/20-01.20.0272.00), pelo apoio ao Projeto "Sistemas de Sistemas de Comando e Controle".

# Trabalhos e publicações
- AVELINO, Jones O.; ROSA, Giselle F.; DANON, Gustavo R.; CORDEIRO, Kelli F.; C. CAVALCANTI, Maria. PREAnoTe: Uma abordagem de anotação de corpus para o ajuste fino de Large Language Model pré-treinado. In: SIMPÓSIO BRASILEIRO DE BANCO DE DADOS (SBBD), 39. , 2024, Florinópolis. (Artigo aceito e ainda não publicado).
- Página do simpósio: https://sbbd.org.br/2024/artigos-curtos/
