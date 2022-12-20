Playing with neo4j database and .NET
It uses bolt API through TCP/IP.


Based on:
1. 
https://console.neo4j.io/?language=.NET&product=aura-db#how-to-connect


2. Installed Neo4j Desktop
https://neo4j.com/download-center/#desktop

3. Pluralsight training
Introduction to Graph Databases, Cypher, and Neo4j 4 by Roland Guijt
https://app.pluralsight.com/library/courses/graph-databases-neo4j-introduction

3.1 Import graphml file:
CALL apoc.import.graphml('drwho.graphml',{batchSize:10000, storeNodeIds: false, readLabels:true})

Error:
Not a recognised system command or procedure. This Cypher command can only be executed in a user database: EXPLAIN CALL apoc.import.graphml('drwho.graphml',{batchSize:10000, storeNodeIds: false, readLabels:true})

3.2 Setting below cause database to fail:
apoc.import.file.enabled=true