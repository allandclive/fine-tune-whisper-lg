# fine-tune whisper lg

jupyter notebooks to fine tune whisper models on luganda using kaggle (should also work on colab but not throughly tested)

*N.B.1* import any trainer or pipeline class from `transformers` crash kaggle TPU session so better use GPU

*N.B.2* trainer class from `transformers` can auto use multi-GPU like kaggle free T4×2 without code change

## scripts

evaluate accuracy (WER):
- on whisper models: [evaluate-whisper.ipynb](eval/evaluate-whisper.ipynb)
- on whisper with PEFT LoRA: [evaluate-whisper.ipynb](eval/evaluate-whisper-lora.ipynb)
- on wav2vec BERT v2 models: [evaluate-w2vBERT.ipynb](eval/evaluate-w2vBERT.ipynb)

fine-tune whisper tiny with traditional approach:
- script: [whisper-tiny-traditional.ipynb](train/whisper-tiny-traditional.ipynb)
- model with evaluated WER: https://huggingface.co/doof-ferb/whisper-tiny-vi

fine-tine whisper large with PEFT-LoRA + int8:
- script: [whisper-large-lora.ipynb](train/whisper-large-lora.ipynb)
- model with evaluated WER: https://huggingface.co/doof-ferb/whisper-large-peft-lora-vi

fine-tune wav2vec v2 bert: [w2v-bert-v2.ipynb](train/w2v-bert-v2.ipynb)

docker image to fine-tune on AWS: [Dockerfile](docker/Dockerfile)

convert to `openai-whisper`, `whisper.cpp`, `faster-whisper`, ONNX, TensorRT: *not yet*

## datasets
