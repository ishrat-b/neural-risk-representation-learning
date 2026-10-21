# Neural Representations of Financial Risk-Taking from EEG

> **Status: Ongoing collaborative project.** This README is a working plan. The work is being done alongside 3 peers. The dataset, methods, and final scope are still under assessment.

## Project overview

Financial risk preferences are usually inferred from choices and outcomes. This project asks whether deep learning can learn useful neural representations from EEG (electroencephalogram) recorded during monetary decision-making, and whether those representations help predict later risk-taking beyond behavioural history.

The main project is planned in two stages:

1. **Neural modelling:** Test whether EEG representations, alone and alongside behavioural history from the Iowa Gambling Task (IGT), help predict subsequent choices or capture individual differences such as risk tolerance and loss sensitivity.
2. **Possible cross-domain extension:** Consider whether behavioural patterns from the EEG task have analogues in corporate risk-taking. This would be a separate, cross-task transfer learning assessment using EEG data obtained from patients performing a different gambling game (GG).


## Provisional plan

- Assess candidate EEG datasets involving risk/reward and monetary decisions, including Iowa Gambling Task (IGT) and Gambling Game (GG).
- Preprocess EEG and explore learned latent representations (`z`); study different permutations and combinations of architecture, preprocessing, and loss functions.
- Define a prediction target, such as a subsequent choice, using EEG and prior choices, outcomes, and reaction times where available.
- Compare behavioural-only, EEG-only, and combined models, including suitable conventional baselines.
- Assess cross-task generalization by pretraining on the third dataset and evaluating whether the learned EEG representations improve risk-taking predictions.
- Use participant-level evaluation splits to reduce leakage between trials from the same person.

Candidate datasets under assessment include [an IGT dataset on Mendeley Data](https://data.mendeley.com/datasets/2pw2m39yct/1), [an IGT dataset on Dryad](https://datadryad.org/dataset/doi%3A10.5061/dryad.8vp47), and [OpenNeuro ds004511](https://github.com/OpenNeuroDatasets/ds004511). These are candidates only; Dataset details and compatibility still need to be checked.

## Limitations

- Participant counts may be small, limiting reliable model comparison and generalization. 
- Trial-level splits can leak participant-specific information, so evaluation will keep participants separate across train and test sets. 
- Results will be described cautiously and will not be generalized beyond the data and task studied.

