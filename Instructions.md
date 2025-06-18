Follow: https://huggingface.co/blog/nvidia/gr00t-n1-5-so101-tuning

## Before copying getting_started/examples/so100__modality.json
edit the video params 

## Build env
az ml environment create --name gr00t-env --build-context . --dockerfile-path Dockerfile --resource-group  robotics-ch-north-secure --workspace-name robotics-ch-north-secure

## Run finetuning
az ml job create --file .\aml\train.yaml --resource-group robotics-ch-north-secure --workspace-name robotics-ch-north-secure
