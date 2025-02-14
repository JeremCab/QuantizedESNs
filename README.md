# QuantizedESNs

## Problem

The Kolmogorov complexity measures the compressibility of real numbers. Accordingly, our study finds its full relevance in the context of theoretical analog computation. In practice, real-valued weights cannot be manipulated exactly, making approximation and compression techniques essential. These compression techniques can be viewed as practical counterparts to the theoretical concept of Kolmogorov complexity. Among them, \textit{quantization} has become a critical technique in recent years, actively explored in research for its ability to enhance computational efficiency during training while preserving, and sometimes even improving, network performance~\cite{Young24}. In the case of echo state networks (ESNs), where only the output weights are trained, we show that the predictive capabilities of the networks are strongly impacted by the degree of quantization applied to their weights.

- An experiment is implemented in the notebook `quantized_ESNs.ipynb`.
- The automatization of the experiments is implemented in the notebook `run_experiments.ipynb`.
- The experiment results are saved in the `/runs` folder.

## Results

The results of our experiments are presented below. As expected, the predictive performance of the networks improves significantly as the number of quantization bits increases (from $2$ to $64$). The forecast horizon also affect the networks performance, to a lesser extent. The logarithmic scale of the heatmaps highlights the substantial gains achieved by increasing weight precision, or equivalently, the drastic losses induced by greater weight quantization. Overall, these results demonstrate that in echo state networks -- where the reservoir primarily functions as a dynamical encoder and predictions rely heavily on the output weights $\vec{W}_{\text{out}}$ -- the level of quantization plays a crucial role in the network's capabilities. This contrasts with deep feedforward architectures, such as Transformers and convolutional neural networks (CNNs), where weight approximation and compression techniques have been successfully applied~\cite{Mittal16,Young24}. We conjecture that this difference arises from the ability of deep architectures to distribute approximation errors across successive layers, thereby mitigating their impact on overall performance.

<img src="https://github.com/JeremCab/QuantizedESNs/blob/main/fig_mackeyglass_all_heatmap.png" width="32%"/>
<img src="https://github.com/JeremCab/QuantizedESNs/blob/main/fig_lorenz_all_heatmap.png" width="32%"/>
<img src="https://github.com/JeremCab/QuantizedESNs/blob/main/fig_henonmap_all_heatmap.png" width="32%"/>
