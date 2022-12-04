# Graph Network Simulator (GNS)

## Reference
[https://arxiv.org/abs/2002.09405](https://arxiv.org/abs/2002.09405)

[https://github.com/deepmind/deepmind-research/tree/master/learning_to_simulate](https://github.com/deepmind/deepmind-research/tree/master/learning_to_simulate).


## To run the model
> Training
```shell
python3 -m src.train --data_path="<input-training-data-path>" --model_path="<path-to-load-save-model-file>" --output_path="<path-to-save-output>" -ntraining_steps=100
```

> Resume training

To resume training specify `model_file` and `train_state_file`:

```shell
python3 -m src.train --data_path="<input-training-data-path>" --model_path="<path-to-load-save-model-file>" --output_path="<path-to-save-output>"  --model_file="model.pt" --train_state_file="train_state.pt" -ntraining_steps=100
```

> Rollout
```shell
python3 -m src.train --mode="rollout" --data_path="<input-data-path>" --model_path="<path-to-load-save-model-file>" --output_path="<path-to-save-output>" --model_file="model.pt" --train_state_file="train_state.pt"
```

> Render
```shell
 python3 -m src.render_rollout --rollout_path="<path-containing-rollout-file>/rollout_0.pkl" 
```


#### Dataset
https://doi.org/10.17603/ds2-0phb-dg64
