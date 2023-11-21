# Section - Vectoring example - Tuesday Oct 31 2023

- ess tasks
	- af-fine-tuning
		- essential goal: to discover what type of data leads to the best fine-tuning on the model on a specific task. 
			- The hypothesis is that the more aligned the data is the more the test set performance (ce loss, ppl) should go up.
		- sanity: compute the aligment btw
			- AF, AF
			- AF, C4
			- C4, C4
		- sanity:
			- H: fine-tune some model that makes the compute work for long enough and the training conditions are "fair" s.t. you know the cause of the eval/test loss being loss is due to alginment
			- deliverable: 
				- fine-tune a model on AF, C4 and hopefully AF has better performance (lower loss/ppl)
					- train a model GPT2 large/xl on AF on the train split then test on the AF test split
					- train a model GPT2 large/xl on C4 on the train split then test on the AF test split
				- fair comparison: 
					- optimizer the similar
					- both models are trained on approximately the same number of tokens
						- epoch/its
						- sequence length truncation
						- batch size
		- diversity
			- ess goal: div --> general intelligence
			- prep
				- calculate how many epochs, etc you need to train on s.t. the same number tokens is seen
			- sanity:
				- train for a few steps 
					- train = uspto, pubmed
					- eval = openwebtext2
					- gpt2 
					- batch ~ 16, 32
			- sanity
				- train a larger or for longer
		- prover equivalence
			- test set
				- (informal stmt, formal stmt)
				- (is*, fs*)
				- fs^ = fm(is*)
				- |- fs^ <==> fs*
					- iff how to write with implications
			- ess goal: the goal is we want the eval to actually measure what we want to solve, which is output a formal stmt that is equivalent to the ground truth formal statement
			- goal: produc
				- correct_equivalence_loss := equivalence(fs1, fs2, prover, LeanDojo) -> 0, 1
					- fs1 ==> fs2 /\ fs2 ==> fs1
			- sanity:
				- equivalence(fs*, fs*, prover, LeanDojo)
				- prover := tidy (some simple but powerul
				- prover := ReProver
			- sanity:
				- equivalence(fs*, transformation(fs), prover, LeanDojo)
				- equivalence(fs*, LLM(is*), prover, LeanDojo)
		- todo:
			- https://docs.google.com/spreadsheets/d/1dEWWzjuEXwf9s4II0CixH4sqopc1flIMFx19UjHiyNU/edit?resourcekey=0-_G7oxmbh7szV5jx-HxhepQ#gid=1063821127 
- tasks
- Wish


- SD
	- ...
	- ...