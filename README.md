### Grade-School Math with Irrelevant Context (GSM-IC)

This repository contains the dataset Grade-School Math with Irrelevant Context (GSM-IC) used in this paper: [Large Language Models Can Be Easily Distracted by Irrelevant Context](https://arxiv.org/abs/2302.00093).

#### Data Format

* ```GSM8K_validation.jsonl```: the development split of [GSM8K dataset](https://github.com/openai/grade-school-math) used in the experiments.

| Field name | Value |
|-------|--------------|
| question | Input question. |
| answer  | The ground truth answer. |
| n_steps  | The number of intermediate steps to calculate the answer. |

* ```GSM-IC_2step.json```: GSM-IC split with problems that require 2 intermediate steps.

| Field name | Value |
|-------|--------------|
| original_question | Original question from the GSM8K development set. |
| new_question  | The new question with irrelevant context added to the original question. |
| answer  | The ground truth answer. |
| n_steps  | The number of intermediate steps to calculate the answer. |
| role_label, number_label, sentence_label| Categories of the added irrelevant context. Needed for result analysis, not needed for model prediction.|
| role, number, sentence_template| Added irrelevant context. Not needed for experiments. |

* ```GSM-IC_mstep.json```: GSM-IC split with problems that require more than 2 intermediate steps. Same format as ```GSM-IC_2step.json```.


#### Citation
If you use the data released through this repository, please cite the following paper:

```
@article{shi2023large,
  title={Large Language Models Can Be Easily Distracted by Irrelevant Context},
  author={Shi, Freda and Chen, Xinyun and Misra, Kanishka and Scales, Nathan and Dohan, David and Chi, Ed and Schärli, Nathanael and Zhou, Denny},
  journal={arXiv preprint arXiv:2302.00093},
  year={2023}
}
```