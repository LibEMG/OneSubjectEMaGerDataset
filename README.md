# OneSubjectEMaGerDataset

Single-subject regression dataset used primarily for continuous estimation of hand open/close and wrist rotation in `LibEMG` demos. The subject was shown a visual prompt and asked to modulate their contraction intensity to mimic the prompt. 

## Usage

We recommend that this dataset is used with our open-source toolkit, `LibEMG`, [publicly available on GitHub](https://github.com/LibEMG/libemg). This dataset can be imported, downloaded, and ready for use in a few lines of code when used with `LibEMG`.

```python
from libemg.datasets import OneSubjectEMaGerDataset
odh = OneSubjectEMaGerDataset().prepare_data()
```

## Data Structure

Data can be found in the `open-close` (hand open/close) and `pro-sup` (wrist pronation/supination) directories, representing the active DOF for the data in that directory.

A `labels.txt` file is provided in each directory representing the ground truth shown to the participant. Each row represents a frame in an animation and each column represents a DOF - column 1 is hand open (+)/close (-) and column 2 is wrist pronation (-)/supination (+).

## Device Details

Data were collected using the HD-EMG EMaGer cuff from Université Laval. Device details are shown below:

- **Name:** EMaGer
- **Sampling frequency:** 1010 Hz
- **Channels:** 64

## Citation

If you are using this dataset in any publications, please cite <https://ieeexplore.ieee.org/document/10340612> for use of the EMaGer cuff.
