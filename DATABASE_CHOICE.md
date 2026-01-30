## Your Choice: **Azure Cosmos DB serverless**

## Justification: Why is this the best choice for this use case? (3-5 sentences)

I chose this managed database primarily for the convenience it offers when integrating with Azure Functions, using the built-in Output Bindings allowed me to connect my code to the database with just a few lines of configuration rather than writing complex driver code. Beyond convenience, Cosmos DB is the ideal choice for this specific application because it uses a schema-less NoSQL model, which lets me store the nested JSON structure of my text analysis results directly without modification. This flexibility means that if I update my Python code to generate new metrics in the future, I can instantly save that new data structure without needing to perform difficult database migrations or update a rigid SQL schema. Finally, the serverless tier matches the sporadic nature of my application, ensuring I don't pay for idle server time while still handling traffic spikes automatically.

## Alternatives Considered: What other options did you evaluate and why did you reject them?

Azure SQL Database (Serverless): This was other ideal candidate I was looking at. The main reason why I did not choose SQL is because it adds a level of complexity that was not needed for this assignement. I believe for a unstructured json data that changed very often during its course of developement and testing, it would have been very annoying to change/update the schema.

## Cost Considerations: How does pricing work for your chosen database?

There are two cost factor for my chosen solution. The first the data cost which will increase as my data increases. The second is the per action cost which will incure when the action is with the database.
