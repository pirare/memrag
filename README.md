# Memrag
This is the journey of me 1. Learning how to code with Go 2. Becoming a more rounded AI developer 3. Develop a memory rag package with practical implimentation

How to use this package:
Given a sentence or paragraph -> memrag -> Context that might be related to the topic.

Memory: Just like how people get to know each other, the goal is to simulate how human memorize, which in theory is just another complex neural network.
How do we do that: 1. Read a bunch of memory related stuff 2. Go down the rabbit hole of building a memory model 3. Figure out what the my training data is 4. Figure out how memory should be structured

# Memory storage type
## Hippocampus
*Forming and storing declarative memory that links to each cortex through presynaptic neurons and postsynaptic nuerons*
### Declarative Memory
**Structure:**
mem_gen_dt, knowledge graph[node, node, edge], relations to other declarative memory, relations to other cortex
## Visual Cortex (Vision)
no development plan
## Sensory Cortex (Touch)
no development plan
## Auditory Cortex (Sound)
no development plan
## Olfactory Cortex (Smell)
no development plan
## Place Cell (Spatial)
no development plan

# Memory Retrieval Mechanism  
## Nueron links
Directional connection stength between each node. Strong/important impression of a memory input or retrieval increases the strength. As time passes by, the strength decays.
**Structure:**
presynaptic, postsynaptic, strength, last_retrieved_date
## strength computation
New strength = original strength + n* **importance**(computed by a ML model taking in the factors of 1. time relation of the memory 2. )
## Mechanism
Whenever a memory is retrieved, the Nueron links used in the retrieval should be strengthened
### Memory retrieval
1. Compile a knowledge graph for the current message
2. Query the strength of all the Nueron links used, recursively. Given the **MEMORY_CAPACITY**(calculated by tokens). Each memory retrieved accumulates towards the tokens and returns the The depth is determined by **RETRIEVAL_DEPTH**(ML model computed for each question) and **DEPTH_CAP**, which are computed by a ML model that estimates the depth needed for each question.
3. Retrieve the 
### Compute new score 3. 
2. 

## Reference
https://www.youtube.com/watch?v=51pPsbV-e9s
https://www.ncbi.nlm.nih.gov/books/NBK234153/
https://www.ibm.com/topics/knowledge-graph
https://ceur-ws.org/Vol-1695/paper4.pdf
https://medium.com/@lars.chr.wiik/best-embedding-model-openai-cohere-google-e5-bge-931bfa1962dc

## Memory Consolidation
The process of STM to LTM. Repetative stimulation of the same memory makes more transmitter and receptor active in the presynaptic and postsynaptic nuerons, which make the access of memory faster and easier.
To simulate this, memory would be

# ***Update: 2024/05/15***
Memory is largely dependent of the mechanism of exracting memory. The retrival speed is addative, either by strong impression or recurring stimulation.

# ***Update: 2024/05/20***
Grasping on to the idea of how a well designed infrastructure would should be like, the insfrastructure would be encapsulated in a roadmap, whereas the master branch would be a the latest deployment.
