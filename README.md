# Projeto Desafio2
## Pipeline + Data Warehouse - Modelagem Dimensional
Este Projeto tem como objetivo construir um pipeline de dados completo de 3 bases operacionais vendas, estoque, devoluções para uma empresa 
fictícia de e-commerce de eletrônicos, permitindo a consolidação, tratamento e análise de dados de vendas, clientes e produtos. A solução para
projeto segue boas práticas de engenharia de dados, incluindo ingestão, transformação e modelagem em um Data Warehouse.

# Contexto do Projeto 
A empresa dw_eletronicos de e-commerce especializada na venda de eletrônicos como Notebooks, Tablet, Smartphone, Webcam, Mouse, Teclado Mecânico,
Caixa de Som Mini, Headset Gamer, Monitor. As operações são distribuídas nas cidades Belo Horizonte, Campinas, Curitiba, Florianópolis,
Goiânia, Porto Alegre, Recife, Rio de Janeiro, Salvador e São Paulo. Os dados operacionais são gerados em múltiplos sistemas e disponibilizado em arquivos externo no formato CSV, incluindo informações de clientes, pedidos, itens vendidos, movimentações de estoque e registros de devoluções. Esses arquivos são extraidos e armazenados em uma camada RAW onde e preservado os dados brutos para o tratamento e limpeza.

# Sistemas utilizadas:
 - VS Code
 - Linguagem Python (Pandas)
 - dbdiagram.io
 - Postgres (pgAdmim4)

# Arquitetura do Projeto
     Arquivos CSV(Vendas, Estoque, Devoluções)
                           │
                           ▼
           Camada RAW (Dados Bruto)
                           │
                           ▼
           Camada STAGING (Dados tratados, limpo, organizado)
                           │
                           ▼
           Data Warehouse (DW - Modelo Dimensional)
                	├──  Dimensões
                	└──  Fatos
                           │
                           ▼
            Métricas de Negócio (SQL)

# Estrutura do Projeto
        DESAFIO_DW_ELETRONICOS/
        |dados/
        │   ├── desafio2_devolucoes.csv
        │   ├── desafio2_estoque.csv
        │   └── desafio2_vendas.csv
        |Diagrama Dimensional/
        │   └── Diagrama Modelo Dimensional.png
        |documentos/
        │   └── desafio2.docx
        |Ingestao/
        │   ├── criacao_schema.ipynb
        │   ├── extracao_devolucao.ipynb
        │   ├── extracao_estoque.ipynb
        │   └── extracao_vendas.ipynb
        |Metricas de Negocio/
        │   ├── Faturamento_canal.ipynb
        │   ├── Faturamento_categoria.ipynb
        │   ├── Faturamento_estado.ipynb
        │   ├── Faturamento_forma_pagamento.ipynb
        │   ├── Faturamento_liquido.ipynb
        │   ├── Faturamento_mes.ipynb
        │   ├── Faturamento_produto.ipynb
        │   ├── Percentual_devolucao.ipynb
        │   ├── Produtos_abaixo_estoque_minimo.ipynb
        │   └── Valor_perdido_devolucoes.ipynb
        |tabelasDimensional/
        │   ├── dimensoes.ipynb
        │   └── fato.ipynb
        └── requirements.txt
 - acesse os arquivos nessa plataforma para acompanhar o desenvolvimento do projeto

# Sequencia de aplicação do projeto
 1. Dados de arquivos externos (desafio_devolucoes.csv, desafio_estoque.csv, desafio_vendas.csv)
 2. Diagrama Dimensional (projetado na plataforma https://dbdiagram.io/
 3. Documentos desafio2.docx
 4. Criação do Banco de Dados no Postgres (dw_eletronicos)
 5. Arquivo (Ingestão):
    - Criação dos schemas
    - Extração dos arquivos (devolucoes, estoque, vendas)
    - Subindo para o Banco de Dados dw_eletronicos
 6. Arquivo (Tabelas Dimensionais):
    - Criação de Tabelas Dimensionais e insersão(população) dos dados (dim_canal_venda, dim_cliente, dim_localidade, dim_pagamento, dim_produto, dim_tempo)
    - Criação de Tabelas Fato e insersão(população) dos dados (fato_vendas, fato_estoque, fato_devolucoes)
 7. requirements.txt (Bibliotecas instaladas no VS Code)
 8. Arquivo (Metricas de Negocio):
    - Faturamento_canal
    - Faturamento_categoria
    - Faturamento_estado
    - Faturamento_forma_pagamento
    - Faturamento_liquido
    - Faturamento_mes
    - Faturamento_produto
    - Percentual_devolucao
    - Produtos_abaixo_estoque_minimo
    - Valor_perdido_devolucoes

# Dependência para rodar a metrica de negocio para Consulta de Dados(query)
  - PostgreSQL (pgAdmim 4)

# Importancia do Projeto Desafio2 para o Aprendizado e Profissionalização
Executar o Projeto Desafio2 vai muito além de apenas desenvolver um pipeline de dados, representa uma experiência prática completa que simula desafios reais enfrentados no dia a dia de profissionais de dados. Ao trabalhar com múltiplas fontes em CSV (vendas, estoque e devoluções), e desenvolvida uma visão integrada do ciclo de vida dos dados, desde a ingestão até a geração de métricas estratégicas.
Do ponto de vista de aprendizado, o projeto consolida fundamentos essenciais de Data Warehouse, permitindo aplicar conceitos como organização em camadas (RAW, STAGING e DW), tratamento e padronização de dados, além da construção de um modelo analítico eficiente baseado em Star Schema. Essa abordagem ajuda a entender, na prática, como transformar dados brutos em informações confiáveis e úteis para o negócio.
Outro ponto importante é o desenvolvimento de habilidades técnicas amplamente exigidas no mercado. O uso de ferramentas como PostgreSQL, manipulação de dados com Pandas e construção de queries SQL para métricas fortalece uma base técnica e aumenta a autonomia na resolução de problemas. Além disso, a organização do projeto em uma estrutura clara e documentada demonstra maturidade profissional e boas práticas de engenharia.
No contexto profissional, esse tipo de projeto funciona como um forte item de portfólio. Ele evidencia uma capacidade de:
Trabalhar com dados reais e imperfeitos
Estruturar pipelines de dados ponta a ponta
Modelar um Data Warehouse orientado a análise
Gerar insights de negócio a partir de dados
Entretanto, o Desafio2 da Comunidados contribui diretamente para a transição de um conhecimento teórico para uma atuação prática, aproximando você do que é esperado em posições como Analista de Dados, Engenhearia de Dados. Ele mostra não apenas que você entende conceitos, mas que consegue aplicá-los de forma estruturada, escalável e orientada a resultados, o Desafio traz um diferencial importante no processo de profissionalização.



    
