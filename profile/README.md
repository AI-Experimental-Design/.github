# AI-Integrated Experimental Design

Course materials for AI-Integrated Experimental Design, a graduate course at
CU Boulder on using predictive models as scientific instruments.

The course focuses on understanding how models make predictions, evaluating
when those predictions can be trusted, and using them to guide scientific
experiments. Examples come from genetics and animal communication.

## Lectures

| Week | Topic | Repository |
| --- | --- | --- |
| 1 | Introduction, ethics, and epistemology | TBD |
| 2 | Model systems: genetics and animal communication | TBD |
| 3 | Evaluating model trustworthiness | TBD |
| 4 | Regression and classification | [regression](https://github.com/AI-Experimental-Design/regression) |
| 5 | Overfitting, regularization, and data leakage | [model-generalization](https://github.com/AI-Experimental-Design/model-generalization) |
| 6 | Neural networks and convolution | [neural-networks](https://github.com/AI-Experimental-Design/neural-networks), [convolution](https://github.com/AI-Experimental-Design/convolution) |
| 7 | Embeddings and self-supervised pretraining | TBD |
| 8 | Attention and transformers | TBD |
| 9 | Fine-tuning | TBD |
| 10 | Model failure, instability, and disagreement | TBD |
| 11 | Case study: genotype to phenotype | TBD |
| 12 | Spring break | — |
| 13 | Case study: prey-predator interactions | TBD |
| 14–16 | Student presentations | — |

## Study tools

| Resource | Repository |
| --- | --- |
| Flashcards | [flashcards](https://github.com/AI-Experimental-Design/flashcards) |

## Setup

Lecture code runs in a software environment managed with
[micromamba](https://mamba.readthedocs.io/en/latest/installation/micromamba-installation.html).

### 1. Install micromamba

On macOS or Linux, run this in a terminal and accept the defaults.

```
"${SHELL}" <(curl -L micro.mamba.pm/install.sh)
```

On Windows, first install WSL by running `wsl --install` in PowerShell, then
restart and open the Ubuntu app. Run the command above inside Ubuntu, and do
all course work there. Some course packages (pysam and snakemake) have no
native Windows builds.

Close and reopen the terminal when the install finishes.

### 2. Create the environment

Download the environment file and build the environment. This takes a few
minutes the first time.

```
curl -O https://raw.githubusercontent.com/AI-Experimental-Design/.github/main/environment.yml
micromamba create -f environment.yml
```    

### 3. Activate it

Activate the environment each time you open a new terminal for class work.

```
micromamba activate ai4ed
```

To check that everything installed, run

```
python -c "import numpy, matplotlib, torch, pysam; print('ready')"
```

### Updating

If the environment file changes during the semester, download it again and run

```
micromamba env update -f environment.yml --prune
```

