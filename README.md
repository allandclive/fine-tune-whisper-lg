# fine-tune whisper vi

jupyter notebooks to fine tune whisper models on vietnamese using kaggle (should also work on colab but not throughly tested)

*N.B.1* import any trainer or pipeline class from `transformers` crash kaggle TPU session so better use GPU

*N.B.2* trainer class from `transformers` can auto use multi-GPU like kaggle free T4×2 without code change

## scripts

evaluate accuracy (WER):
- on whisper models: [evaluate-whisper.ipynb](evaluate-whisper.ipynb)
- on whisper with PEFT LoRA: [evaluate-whisper.ipynb](evaluate-whisper-lora.ipynb)
- on wav2vec BERT v2 models: [evaluate-w2vBERT.ipynb](evaluate-w2vBERT.ipynb)

fine-tune whisper tiny with traditional approach:
- script: [whisper-tiny-traditional.ipynb](whisper-tiny-traditional.ipynb)
- model with evaluated WER: https://huggingface.co/doof-ferb/whisper-tiny-vi

fine-tine whisper large with PEFT-LoRA + int8: [whisper-large-lora.ipynb](whisper-large-lora.ipynb)

fine-tune wav2vec v2 bert: [w2v-bert-v2.ipynb](w2v-bert-v2.ipynb)

convert to `openai-whisper`, `whisper.cpp`, `faster-whisper`, ONNX, TensorRT: *not yet*

## datasets

my collection of vietnamese speech datasets: https://huggingface.co/collections/doof-ferb/vietnamese-speech-dataset-65c6af8c15c9950537862fa6

other datasets but cannot find download links:
- Broadcasting Speech Corpus VOV: https://www.isca-archive.org/iscslp_2006/luong06_iscslp.html
- VNSpeechCorpus: https://aclanthology.org/L04-1364/
- VAIS-1000: https://ieee-dataport.org/documents/vais-1000-vietnamese-speech-synthesis-corpus
- https://arxiv.org/abs/1904.05569
