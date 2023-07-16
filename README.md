# interp-hackathon-layernorm

Investigating problem 4.39 from [Concrete Open Problems](https://www.lesswrong.com/s/yivyHaCAmMJ3CqSyj/p/o6ptPu7arZrqRCxyz#Problems).

> - B-C* 4.39 - The paper speculates that the LayerNorm after the SoLU activations lets the model "smuggle through" superposition, by smearing features across many dimensions, having the output be very small, and letting the LayerNorm scale it up. Can you find any evidence of this in solu-1l?
>    - I would start by checking how much the LayerNorm scale factor varies between tokens/inputs. 
>    - I would also look for tokens where the neuron has (comparatively) low activation pre-LayerNorm but high direct logit attribution
>    - I would also look for tokens where the direct logit attribution of the MLP layer is high, but no single neuron is high. 
