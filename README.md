# QuantizedESNs

The Kolmogorov complexity measures the compressibility of real numbers. Accordingly, our study finds its full relevance in the context of theoretical analog computation. In practice, real-valued weights cannot be manipulated exactly, making approximation and compression techniques essential. These compression techniques can be viewed as practical counterparts to the theoretical concept of Kolmogorov complexity. Among them, \textit{quantization} has become a critical technique in recent years, actively explored in research for its ability to enhance computational efficiency during training while preserving, and sometimes even improving, network performance~\cite{Young24}. In the case of echo state networks (ESNs), where only the output weights are trained, we show that the predictive capabilities of the networks are strongly impacted by the degree of quantization applied to their weights.

- An experiment is implemented in the notebook `quantized_ESNs.ipynb`.
- The automatization of the experiments is implemented in the notebook `run_experiments.ipynb`.
- The experiment results are saved in the `/runs` folder.
