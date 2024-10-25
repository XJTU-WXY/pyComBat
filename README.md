# ⚠ About this fork
The original version of pyCombat has the following code in setup.py:
```python
with open("README.md", "r") as fh:
    long_description = fh.read()
```
This will cause an error due to encoding issues in non-English versions of Windows, which will cause the library to fail to be installed through pip. The author's original repository is already in the public archive state. For new projects, it is recommended to use the author's new version [InMoose](https://github.com/epigenelabs/inmoose). For old projects that use pyCombat and have not been updated, I created this fork for non-English users.

You can install my fork by pip:
```shell
pip install combat@git+https://github.com/XJTU-WXY/pyComBat
```

# MIGRATION WARNING

pyComBat has been merged into [InMoose](https://github.com/epigenelabs/inmoose), and is no
longer maintained as a standalone package.
This repository remains up for reference, but will no longer be updated.

# pyComBat

pyComBat [1] is a Python 3 implementation of ComBat [2], one of the most widely used tool for correcting technical biases, called batch effects, in microarray expression data.

More detailed documentation can be found at [this address](https://epigenelabs.github.io/pyComBat/).


## Usage example

### Running pyComBat

The simplest way of using pyComBat is to first import it, and then simply use the pycombat function with default parameters:

```python
from combat.pycombat import pycombat
data_corrected = pycombat(data,batch)
```

* data: The expression matrix as a dataframe. It contains the information about the gene expression (rows) for each sample (columns).

* batch: List of batch indexes. The batch list describes the batch for each sample. The list of batches contains as many elements as the number of columns in the expression matrix.

## How to contribute

Please refer to [CONTRIBUTING.md](https://github.com/epigenelabs/pyComBat/blob/master/CONTRIBUTING.md) to learn more about the contribution guidelines.

## References

[1] Behdenna A, Haziza J, Azencot CA and Nordor A. (2020) pyComBat, a Python tool for batch effects correction in high-throughput molecular data using empirical Bayes methods. bioRxiv doi: 10.1101/2020.03.17.995431
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        

[2] Johnson W E, et al. (2007) Adjusting batch effects in microarray expression data using empirical Bayes methods. Biostatistics, 8, 118–127
