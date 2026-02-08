# Database Choice

## Your Choice
I chose Azure Cosmos DB (Core SQL API, Serverless/Free Tier).

## Justification
Azure Cosmos DB stores JSON documents natively, which fits the output of the Text Analyzer function. It works well with serverless applications and does not require a fixed schema. The serverless and free tier options make it affordable for students. It also provides strong Python SDK support for Azure Functions.

## Alternatives Considered
Azure Table Storage was considered but has limited query capabilities. Azure SQL Database was rejected because it requires predefined schemas and is less flexible for JSON data. Azure Blob Storage was not chosen because it is not designed for structured querying.

## Cost Considerations
Azure Cosmos DB offers a free tier with limited RU/s and storage. The serverless tier charges based on usage, making it suitable for low-traffic student projects.
