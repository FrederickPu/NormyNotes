- RNN
- Transformers

2 main kinds:
- State-transition Based: store memory in the internal state of the model (RNN, and post-transformer architectures)
- Context/attention based: get memories from the context window (transformers, lin-formers)

information theoretic insight:
- state based models: can have a finite amount of total information but that information can stretch as far back in time as you want in principle (eg you see a 10/10 baddie and you never remember anything else until the day you die). More specifically, any distribution of information (a distribution of information is how certain you are of the value of each of the previous tokens) over time can be encoded in the RNNs internal representation
- context/attention based models: have a much higher information certainty within it's context window in comparison with the state based model. However, outside of its context window it has a minimal possible information certainty (it could be anything). In principle a transformer should be able to have 100% information certainty about the value of each of the tokens within it's context window.
Note: when we talk about information certainty we mean, given the current internal activations of the model (a single RNN unit or a single GPT unit) what is the probability distribution for the value each of the previous tokens.