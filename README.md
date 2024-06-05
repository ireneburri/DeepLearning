### Sentence Reconstruction
The purpose of this project is to take in input a sequence of words corresponding to a random permutation of a given english sentence, and reconstruct the original sentence.

The otuput can be either produced in a single shot, or through an iterative (autoregressive) loop generating a single token at a time.

# CONSTRAINTS:
- No pretrained model can be used.
- The neural network models should have less than 20M parameters.
- No postprocessing should be done (e.g. no beamsearch).
- You cannot use additional training data.

# Dataset
The dataset is composed by sentences taken from the generics_kb dataset of hugging face. We restricted the vocabolary to the 10K most frequent words, and only took sentences making use of this vocabulary.

!pip install datasets
ds = load_dataset('generics_kb',trust_remote_code=True)['train']
