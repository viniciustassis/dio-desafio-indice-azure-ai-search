# Laboratório para Criar um índice do Azure AI Search (UI)

## Resumo
Projeto que cria um índice do Azure AI Search usando dados extraídos através da mineração de conhecimento para buscar insights sobre as experiências dos clientes, como desafio de projeto da DIO.

Laboratório da Azure [Explore an Azure AI Search index (UI)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)

## Recursos/Ferramentas necessárias
- **Recurso do Azure AI Search** que gerenciará a indexação e a consulta.
- **Recurso de serviços de IA do Azure** que fornece serviços de IA para habilidades que sua solução de pesquisa pode usar para enriquecer os dados na fonte de dados com insights gerados por IA.
- **Uma conta de armazenamento com contêineres de blobs** que armazenará documentos brutos e outras coleções de tabelas, objetos ou arquivos.


Observação: Os recursos do Azure AI Search e dos serviços Azure AI devem estar no mesmo local!

## Processo

1. **Recursos**

- 1.1. **Criação de recurso do Azure AI Search**:
    - Criação de recurso do Azure AI Search no [Portal Azure](https://portal.azure.com)

- 1.2. **Criação de serviços de IA do Azure**:
    - deve estar no mesmo local que seu recurso do Azure AI Search.
    - A solução de pesquisa usará esse recurso para enriquecer os dados no armazenamento de dados com insights gerados por IA.

- 1.3. **Criação de uma conta de armazenamento**:
    - Após a conclusão da implantação, ir para o recurso implantado
    - Alterar a configuração de Permitir acesso anônimo de Blob para **Habilitado** e selecionar **Salvar**

2. **Carregamento de documentos para o armazenamento do Azure**:
- No painel do menu esquerdo, selecionar Containers e criar um container
- O arquivo que será carregado é o exemplo do laboratório [avaliações de café compactadas](https://aka.ms/mslearn-coffee-reviews)
- No portal do Azure, selecione o contêiner de avaliações de café
- No contêiner, selecionar Upload blob e informar o arquivo

3. **Utilização do indexador do Azure no portal do Azure**:
- Acesse o recurso do Azure AI Search criado anteriormente.
- No painel de navegação, selecione **Import data** para iniciar o assistente de indexação.
- Siga as instruções do assistente para conectar sua fonte de dados (conta de armazenamento do Azure).
- Escolha o contêiner onde você carregou os documentos de avaliações de café.
- Configure as habilidades de enriquecimento de IA que deseja aplicar aos dados durante a indexação. Isso pode incluir extração de entidades, análise de sentimentos, etc.
- Nomeie seu índice e revise as configurações antes de criar o indexador.
- Após a criação, o Azure AI Search processará os documentos no contêiner, aplicará as habilidades de IA selecionadas e criará o índice.

4. **Consultar seu índice de pesquisa**:
- Após a indexação ser concluída, você pode começar a consultar seu índice para buscar insights.
- No recurso do Azure AI Search, vá para a seção **Search explorer**.
- Use a interface do Search explorer para executar consultas de texto livre ou consultas mais complexas, utilizando a linguagem de consulta do Azure Search.
- Experimente diferentes tipos de consultas para explorar os dados indexados e os insights gerados pelo enriquecimento de IA.

5. **Revise os resultados salvos em uma Loja de conhecimento**:
- Se você configurou uma Loja de conhecimento como parte do seu processo de indexação, os dados enriquecidos serão salvos automaticamente nela.
- A Loja de conhecimento permite revisar e gerenciar os dados enriquecidos gerados a partir de suas fontes originais.
- Acesse a Loja de conhecimento através do recurso do Azure AI Search ou diretamente via Azure Storage Explorer, se os dados estiverem armazenados em uma conta de armazenamento do Azure.
- Analise os dados enriquecidos para identificar padrões, tendências e insights valiosos que podem ser aplicados para melhorar a experiência do cliente ou informar decisões de negócios.

## Insights Principais

- Automatizar a organização, a busca e a análise de dados reduz a necessidade de intervenção manual.
- Ferramentas de busca enriquecidas por IA podem oferecer recomendações personalizadas nas plataformas de E-commerce para análises de sentimentos em avaliações de produtos e buscas visuais, melhorando a conversão de vendas.
