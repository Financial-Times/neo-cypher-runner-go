# neo-cypher-runner-go
Go library for running cypher against Neo4j.

Currently supports batch running of queries.

Import as "github.com/Financial-Times/neo-cypher-runner-go".

Create a batch cypher runner like this:

    cypherRunner := neocypherrunner.NewBatchCypherRunner(db, batchSize, time.Millisecond*time.Duration(timeoutMs))

Execute a batch of queries like this:

    cypherRunner.CypherBatch([]*neoism.CypherQuery{query})