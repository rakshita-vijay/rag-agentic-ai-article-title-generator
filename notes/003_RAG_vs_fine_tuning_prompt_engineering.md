**LINK:** https://www.youtube.com/watch?v=zYGDpG-pTho

---

## Types of Model Response Reneration: 
- RAG (Retrieval Augmented Generation): the model goes out, finds things that have been updated in the world after it has breen trained, and incorporates that information into its answer
  
- Fine Tuning: specialized model that is trained on, say, transcripts of a video, or basically, specific, small, niche dataset
  - the process of taking a pre-trained model and further training it on a specific, smaller dataset related to a particular task or domain

- Prompt Engineering: giving specifics to the model to differentiate between useful and useless data from the web 

---

## RAG:
>     query → LLM → returns response
>              ↓
>              ↓RAG  
>              ↓
>              🛢️ 
>      corpus (documents)  
>           of info 

1. converts the query (user question) and all the documents into vector embeddings (long list of numbers that represent its meaning)
2. finds semantically equivalent info
3. converts it into human-readable format
4. returns back to user

---

Pros:
- for up-doate info
- for domain-specific info

Cons:
- performance: retrieval step - adds latency
- cost of processing this - storing, processing, infrastructure
  
---

## Fine Tuning: 
take an existing model - has broad knowledge
give it additional focused training on a specialized data set
this updates internal parameters through additional training
we provide q-a pairs to show what kind of responses we want

Pros:
- deep domain experience
- faster
- knowledge is baked into db, so no need separate vector db

Cons:
- training complexity - 1000s of high-quality examples
- computational cost - many GPUs
- maintenance - updating db needs another round of training
- risk of catastrophic forgetting: model loses some of its general capabilities when it is learning these specialized ones

---

## Prompt Engineering: 
input a prompt
model receives it 
processes it through diff layers 
  - tension mechanisms
  - each one focuses on different aspects of input prompt
each of the specifics included in the prompt is what the model is directed to look at 

Pros:
- no infrastructure changes
- immediate responses

Cons:
- trial and error to find effective prompts
- limited to existing knowledge
