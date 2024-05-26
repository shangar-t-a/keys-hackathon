# Azure Cosmos DB Developer Cloud Skills Challenge Part 1

URL: <https://learn.microsoft.com/en-us/collections/gm3rb7kwqzn8?WT.mc_id=cloudskillschallenge_a67d6970-52a8-4050-b6f0-d9c51324ed40>

- [Azure Cosmos DB Developer Cloud Skills Challenge Part 1](#azure-cosmos-db-developer-cloud-skills-challenge-part-1)
  - [Azure OpenAI Services](#azure-openai-services)
    - [Access Azure OpenAI Service](#access-azure-openai-service)
    - [Use Azure OpenAI Studio](#use-azure-openai-studio)
    - [Explore types of generative AI models](#explore-types-of-generative-ai-models)
    - [Deploy generative AI models](#deploy-generative-ai-models)
    - [Use prompts to get completions from models](#use-prompts-to-get-completions-from-models)
    - [Test models in Azure OpenAI Studio's playgrounds](#test-models-in-azure-openai-studios-playgrounds)
    - [Exercise - Get started with Azure OpenAI Service](#exercise---get-started-with-azure-openai-service)
  - [Explore fundamentals of Azure Cosmos DB](#explore-fundamentals-of-azure-cosmos-db)
    - [Identify Azure Cosmos DB APIs](#identify-azure-cosmos-db-apis)
      - [Azure Cosmos DB for MongoDB](#azure-cosmos-db-for-mongodb)
      - [Azure Cosmos DB for PostgreSQL](#azure-cosmos-db-for-postgresql)
      - [Azure Cosmos DB for Table](#azure-cosmos-db-for-table)
      - [Azure Cosmos DB for Apache Cassandra](#azure-cosmos-db-for-apache-cassandra)
      - [Azure Cosmos DB for Apache Gremlin (Graph)](#azure-cosmos-db-for-apache-gremlin-graph)
    - [Exercise: Explore Azure Cosmos DB](#exercise-explore-azure-cosmos-db)
    - [Summary](#summary)
  - [Introduction to building copilots for startups](#introduction-to-building-copilots-for-startups)
    - [Overview of copilots for startups](#overview-of-copilots-for-startups)
    - [What is Azure Copilot Stack?](#what-is-azure-copilot-stack)
    - [Examine Microsoft Copilot Stack use cases](#examine-microsoft-copilot-stack-use-cases)
    - [Apply best practices to build your future copilot](#apply-best-practices-to-build-your-future-copilot)
  - [Build natural language solutions with Azure OpenAI Service](#build-natural-language-solutions-with-azure-openai-service)
    - [Integrate Azure OpenAI into your app](#integrate-azure-openai-into-your-app)
    - [Use Azure OpenAI REST API](#use-azure-openai-rest-api)
      - [Chat Completions](#chat-completions)
      - [Embeddings](#embeddings)
    - [Use Azure OpenAI SDK](#use-azure-openai-sdk)
      - [Install Libraries](#install-libraries)
      - [Configure app to access Azure OpenAI resource](#configure-app-to-access-azure-openai-resource)
      - [Call Azure OpenAI resource](#call-azure-openai-resource)
      - [Exercise - Integrate Azure OpenAI into your app](#exercise---integrate-azure-openai-into-your-app)

## Azure OpenAI Services

### Access Azure OpenAI Service

- Creating account in Azure Portal - <https://portal.azure.com/>.
- Azure OpenAI Services has to be requested for access - <https://aka.ms/oai/access>.
  - Is expecting work email address.
- Creating an Azure OpenAI Services resource in Azure Portal.

### Use Azure OpenAI Studio

- Azure OpenAI Studio - <https://oai.azure.com/portal/>.
  - Model management, deployment, experimentation, customization, and learning resources.
  - Deploy base models.

### Explore types of generative AI models
  
- Types of GenAI models. Models available during the challenge (12-May-2024):
  - GPT-4 (Latest of generative AI models).
  - GPT-3.5 (GPT-35-turbo can be suitable for most cases).
  - Embedding models (Text to numeric vectors).
  - DALL-E (Text to image). In Preview stage.
  - Models vary in size, performance, and cost.

### Deploy generative AI models
  
Deploy GenAI models.

- Deploy using Azure OpenAI Studio. Select model, create deployment, and deploy.
- Other deployment options: Azure CLI, Azure REST API.

### Use prompts to get completions from models

- Use Prompts to get completions.
  - Prompt Types:
    - Classification content. E.g. "Sentiment analysis: I enjoyed the movie" "Positive"
    - Generating new content. E.g. "List of fruits" "Apple, Banana, Orange"
    - Holding a conversation. E.g. "You are a friendly assistant"
    - Transformations. E.g. "Translate 'Hello' to French" "Bonjour"
    - Summarizing content. E.g. "Summarize this article" "The article is about..."
    - Picking up where you left off. E.g. "One way to grow tomatoes" "is to plant seeds"
    - Giving factual responses. E.g. "What is the capital of France?" "Paris"
  - Completion quality (Factors):
    - Prompt engineering. <https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/prompt-engineering?portal=true>
    - Model Parameters.
    - Data used to train the model. (Fine tuning: <https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/fine-tuning?pivots=programming-language-studio&tabs=turbo%2Cpython-new>)
  - Chat Completions: <https://learn.microsoft.com/en-us/azure/ai-services/openai/reference#chat-completions?azure-portal=true>

### Test models in Azure OpenAI Studio's playgrounds

Test Models in Azure OpenAI Studio's Playgrounds.

- Completion Playground Parameters:
  - Temperature: 0.0 to 1.0 (0.0: Conservative, 1.0: Creative).
  - Max length (Tokens): API supports max of 4000 tokens. Tokens include prompt (system message, examples, message
    history, and user query) and response. One token is approximately 4 english characters.
  - Stop sequence: Stop completion at a specific token.
  - Top P: Probability threshold for sampling. Choose from top P tokens, increasing randomness.
  - Frequency penalty: Penalize tokens that have been generated recently.
  - Presence penalty: Penalize tokens that have been generated previously.
  - Pre Response Text: Text to include before the response. Prepare model for the response.
  - Post Response Text: Text to include after the response. Encourage further conversation.
- No Shot & Few Shot
  - No Shot: No examples provided. Model uses pre-trained knowledge.
  - Few Shot: Provide examples to guide the model.

### Exercise - Get started with Azure OpenAI Service

- Exercise: Azure OpenAI Services
  - Get Azure OpenAI Subscription. <https://aka.ms/oaiapply>
  - Create a resource in Azure Portal.
  - Azure Portal -> Azure OpenAI Studio -> Deploy a model.
  - Use Azure OpenAI Studio's Playgrounds to test the model.
    - Setup, Chat Session and Configuration.
  - Chat response with and without history.
  - Experimenting with System Message and Few Shots.
  - Experiment with Parameters.
  - Deploy model to web app.
  - Clean up resources.
  
> [!NOTE]
> The exercise is done read only due to unavailability of subscription and existing hands-on experience with
> Open AI models / services.

## Explore fundamentals of Azure Cosmos DB

1. Azure Cosmos DB is a cloud database service for NoSQL data.
2. Azure Cosmos DB:
   - Multiple API support.
   - Highly scalable (Automatically allocate space in containers for each partitions, each partition can grow to 10GB).
   - Indexes are created and maintained automatically.
3. Azure Cosmos DB can be used in: (Large scale data, quick response)
   - IoT and telematics.
   - Retail and marketing.
   - Gaming.
   - Web and mobile apps.

### Identify Azure Cosmos DB APIs

- Azure Cosmos DB is serverless.
- Manages data in JSON (NoSQL) and still uses SQL syntax.
- Sample SQL query and result could be:

  ```sql
  SELECT *
  FROM customer c
  WHERE c.id = "joe@Litware.com"
  ```

  ```json
  {
    "id": "joe@Litware.com",
    "name": "Joe Jones",
    "address": {
      "street": "123 Main St",
      "city": "Seattle"
  }
  ```

#### Azure Cosmos DB for MongoDB

- Enables developers to use MongoDB client to work with data in Azure Cosmos DB.
- MongoDB (MongoDB Query Language) uses object-oriented syntax.
- Sample MongoDB query and result could be:

  ```python
  db.people.find({"id": 123})
  ```

  ```json
  {
    "id": 123,
    "name": "Hammer",
    "price": 9.99
  }
  ```

#### Azure Cosmos DB for PostgreSQL

- Azure Cosmos DB for PostgreSQL is a native PostgreSQL.
- Can start building on single node server group and scale to multiple nodes.
- Sample PostgreSQL query and result could be:

  ```table
  | ProductID | ProductName | Price |
  |-----------|-------------|-------|
  | 123       | Hammer      | 9.99  |
  | 124       | Saw         | 19.99 |
  ```

  ```sql
  SELECT ProductName, Price
  FROM Products
  WHERE ProductID = 123
  ```

  ```table
  | ProductName | Price |
  |-------------|-------|
  | Hammer      | 9.99  |
  ```

#### Azure Cosmos DB for Table

- Azure Cosmos DB for Table is a key-value store.
- Offers greater scalability and performance than Azure Table Storage.
- Sample Table query and result could be: (use Table API through language specific SDKs)

  ```table
  | PartitionKey | RowKey | Name     | Price |
  |--------------|--------|----------|-------|
  | 1            | 123    | Hammer   | 9.99  |
  | 2            | 124    | Saw      | 19.99 |
  ```

  ```url
  <https://endpoint/Products(PartitionKey='1',RowKey='124')>
  ```

#### Azure Cosmos DB for Apache Cassandra

- Azure Cosmos DB for Apache Cassandra is compatible with Apache Cassandra.
- Column-family storage structure.
- Column-families are tables, except that they can have different columns.
- Sample Cassandra query and result could be:

  ```table
  | ID | Name      | Manager   |
  |----|-----------|-----------|
  | 1  | Sue Smith |           |
  | 2  | Joe Jones | Sue Smith |
  ```

  ```sql
  SELECT * FROM employees WHERE ID = 2
  ```

  Retrieve record for Joe Jones.

#### Azure Cosmos DB for Apache Gremlin (Graph)

- Azure Cosmos DB for Apache Gremlin is used with data in a graph structure.
- Entities are defined as vertices that form nodes in connected graphs.
- Nodes are connected by edges.<br>
  ![Azure Cosmos DB for Apache Gremlin](images/azure_cosmos_db_for_apache_gremlin.png)<br>
  Vertex ("employee" and "department") and edge ("reports to" and "works in").
- Sample Gremlin query and result could be:

  ```python
  # Add new employee vertex with ID 3 and name Alice that reports to employee with ID 1.
  g.addV('employee').property('id', '3').property('firstName', 'Alice')
  g.V('3').addE('reports to').to(g.V('1'))
  ```

- Query to return all of the employee vertices, in order of their ID.

  ```python
  g.V().hasLabel('employee').order().by('id')
  ```

### Exercise: Explore Azure Cosmos DB

1. Create an Azure Cosmos DB account.
2. Create a database and container.
3. View and Create items in the database.
4. Query items in the database.
5. Clean up resources.

> [!NOTE]
> The exercise is done read only due to unavailability of subscription

### Summary

- Global scale database for non-relational data.
- Key features and capabilities of Azure Cosmos DB.
- Different APIs for different data models.

## Introduction to building copilots for startups

- Concept of Copilots and the Azure Copilot Stack.
- How copilots are used and deployed?
- Best practices for building copilots.

### Overview of copilots for startups

- Copilots are AI assistants built using Azure Copilot Stack (AI Development Framework).
- Plugins for Copilot (Help access and use data from various sources).
  - Simplify integration with data sources via unified APIs.
  - Enhance customizations by allowing to fine-tune models.
  - Improve scalability and reliability by using Azure infrastructure.
  - Support responsible AI by providing content filtering, governance, and diversity and inclusion features.
- Copilot App Patterns: Beside (helper in app), Center (app foundation) and Outside (orchestrate across app and tasks).
- Benefits:
  - Product without Copilot could become rare!
  - Incorporate Copilot in apps / products will be a game changer.
  - Boost productivity and increase customer satisfaction.

### What is Azure Copilot Stack?

- AI Development Framework.
- Uses generative AI technologies like GPT-4 available in Azure OpenAI Services.
- Provides various tools and services to build and deploy AI models. (Azure OpenAI Studio)
- Differentiate Azure OpenAI and OpenAI Service
  - OpenAI Service: Access to OpenAI models directly from OpenAI.
  - Azure OpenAI: Access to OpenAI models through Azure services. With additional features and services. Mainly
    security, performance, scalability, reliability, and support. Co-develops API with OpenAI.
- Explore the benefits of copilots for startups
  - Save time and reduce costs by automating tasks.
  - Improve quality and accuracy of outputs by applying state-of-the-art AI models.
  - Customize and fine-tune models with own data and hyperparameter.
  - Use AI responsibly by filtering and moderating content.
  - Secure data with Azure's enterprise-grade security and compliance features.
- Not a one-size-fits-all solution. Customizable and scalable.

### Examine Microsoft Copilot Stack use cases

- Microsoft integrates Copilot in various products. (GitHub, MS Edge, MS365, etc.)
- Microsoft uses Copilot Stack.
- Case Study: GitHub Copilot, Microsoft Security Copilot, Microsoft 365 Copilot.

### Apply best practices to build your future copilot

- Work alongside not a replacement.
- Copilot architecture guidance as model for building products.
- NLP can enable users to interact with product and provide feedback and guidance.
- Integrating AI can enrich existing features and create new features that solve real problems.
- Combining AI capabilities (Image + NLU) could unlock even more powerful and creative solution.

## Build natural language solutions with Azure OpenAI Service

- Add AI capabilities to apps with help of Python and C# SDKs and REST APIs.
- Azure OpenAI has various AI models, each specialized for different tasks.

### Integrate Azure OpenAI into your app

1. Create an Azure OpenAI resource.
   - Azure Portal -> Azure OpenAI -> Create resource.
   - Key and endpoint are provided.

2. Choose and deploy a model.
   - Model Families:
     - GPT (Generative Pre-trained Transformer).
     - Code (gpt-3, gpt-35-turbo).
     - Embeddings

   - Details on models, capability levels and naming conventions: <https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/models>

3. Authentication and specification of deployed model
   - When deploying model, deployment name is provided. When configuring the app resource endpoint, key and deployment
   name are used enabling to deploy multiple models with the same resource.

4. Prompt Engineering
   - Simple input -> Simple output (like a search engine).
   - Customized input (prompt) -> Customized output (like a chatbot).
   - Output of the model should be measured and evaluated.

5. Available Endpoints
   - Completion
   - ChatCompletion
     - Example:

     ```json
     {"role": "system", "content": "You are a helpful assistant, teaching people about AI."},
     {"role": "user", "content": "Does Azure OpenAI support multiple languages?"},
     {"role": "assistant", "content": "Yes, Azure OpenAI supports several languages, and can translate between them."},
     {"role": "user", "content": "Do other Azure AI Services support translation too?"}
     ```

     - Chat history can be fed as input to the model to provide context.
     - Can also be used for summarization or entity extraction.
   - Embeddings

### Use Azure OpenAI REST API

- All REST API require endpoint and key.
- ENDPOINT_NAME, API_KEY and DEPLOYMENT_NAME.

#### Chat Completions

- `POST` request for the model.

  ```rest
  curl <https://YOUR_ENDPOINT_NAME.openai.azure.com/openai/deployments/YOUR_DEPLOYMENT_NAME/chat/completions?
  api-version=2023-03-15-preview \>
    -H "Content-Type: application/json" \
    -H "api-key: YOUR_API_KEY" \
    -d '{"messages":[{"role": "system", "content": "You are a helpful assistant, teaching people about AI."},
  {"role": "user", "content": "Does Azure OpenAI support multiple languages?"},
  {"role": "assistant", "content": "Yes, Azure OpenAI supports several languages, and can translate between them."},
  {"role": "user", "content": "Do other Azure AI Services support translation too?"}]}'
  ```

  Possible response could be:

  ```json
  {
    "id": "chatcmpl-6v7mkQj980V1yBec6ETrKPRqFjNw9",
    "object": "chat.completion",
    "created": 1679001781,
    "model": "gpt-35-turbo",
    "usage": {
        "prompt_tokens": 95,
        "completion_tokens": 84,
        "total_tokens": 179
    },
    "choices": [
        {
            "message":
                {
                    "role": "assistant",
                    "content": "Yes, other Azure AI Services also support translation. Azure AI Services offer
                    translation between multiple languages for text, documents, or custom translation through Azure
                    AI Services Translator."
                },
            "finish_reason": "stop",
            "index": 0
        }
    ]
  }
  ```

- REST endpoints also allow for specifying optional parameters like `temperature`, `max_tokens`, and more.

#### Embeddings

- Embeddings API can be used to convert text to numeric vectors (easily consumed by ML models).
- `POST` request for the embeddings model.

  ```rest
  curl <https://YOUR_ENDPOINT_NAME.openai.azure.com/openai/deployments/YOUR_DEPLOYMENT_NAME/embeddings?
  api-version=2022-12-01 \>
  -H "Content-Type: application/json" \
  -H "api-key: YOUR_API_KEY" \
  -d "{\"input\": \"The food was delicious and the waiter...\"}"
  ```

  Make sure to use embeddings model for embeddings APIs. They typically start with `text-embeddings` or
  `test-similarity`.

  Possible response could be:

  ```json
  {
    "object": "list",
    "data": [
      {
        "object": "embedding",
        "embedding": [
          0.0172990688066482523,
          -0.0291879814639389515,
          ....
          0.0134544348834753042,
        ],
        "index": 0
      }
    ],
    "model": "text-embedding-ada:002"
  }
  ```

### Use Azure OpenAI SDK

- Azure OpenAI SDKs are available for Python and C#. Functions are similar to REST API.
- Requires: ENDPOINT_NAME, API_KEY and DEPLOYMENT_NAME.

#### Install Libraries

- Python SDK:

  > `pip install azure-openai`

#### Configure app to access Azure OpenAI resource

- Necessary parameters are `endpoint`, `key`, and name of the deployment, which is called `engine`.

```python
# Add OpenAI library
from openai import AzureOpenAI

deployment_name = '<YOUR_DEPLOYMENT_NAME>' 

# Initialize the Azure OpenAI client
client = AzureOpenAI(
        azure_endpoint = '<YOUR_ENDPOINT_NAME>', 
        api_key='<YOUR_API_KEY>',  
        api_version="20xx-xx-xx" #  Target version of the API, such as 2024-02-15-preview
        )
```

#### Call Azure OpenAI resource

- Once configured connection to Azure OpenAI, send prompt to the model.

```python
response = client.chat.completions.create(
    model=deployment_name,
    messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "What is Azure OpenAI?"}
    ]
)
generated_text = response.choices[0].message.content

# Print the response
print("Response: " + generated_text + "\n")
```

- Response object contains `total_tokens` and `finish_reason`.
- Optional parameters like `temperature` and `max_tokens` can be passed to the model.

#### Exercise - Integrate Azure OpenAI into your app

1. Provision an Azure OpenAI resource.

   - Sign in to Azure Portal: <https://portal.azure.com/>.
   - Create a new resource.
     - Subscription
     - Resource Group
     - Region
     - Name
     - Pricing tier (Standard S0)
   - Deploy the resource.

2. Deploy a model.

   - Azure OpenAI Studio -> Deploy a model.
   - Deployments -> gpt-35-turbo-16k
     - Model: gpt-35-turbo-16k
     - Model Version: Auto-update to default
     - Deployment Name
     - Advanced Options
       - Content filter: Default
       - Deployment type: Standard
       - Tokens per minute rate limit: 5K*
       - Enable dynamic quota: Enabled

3. Develop an app in VS Code.
  
   - Start Visual Studio Code.
   - Clone: <https://github.com/MicrosoftLearning/mslearn-openai>

4. Configure the application

   - Update code and verify.
   - Install openai (SDK), Update .env file with endpoint, key and deployment name.

5. Add code to use Azure OpenAI service.

   - Import SDK.
   - Initialize client and System messages.
   - Call chat completions and print response.
   - Test the app.
   - Include chat history and system messages.
   - Experiment with parameters (temperature).
   - Clean up resources.
