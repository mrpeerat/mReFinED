# Overview
We propose mReFinED, the first end-to-end MEL model. mReFinED supports 9 languages: AR, EN, ES, DE, FA, JA, TA, TR, and TH. Our experimental results in the research paper demonstrated that mReFinED outperformed the best existing work in the end-to-end MEL task while being 44 times faster compared to existing state-of-the-art (mGENRE).

# mReFinED's Paper
The mReFinED model architecture is described in the paper below (https://aclanthology.org/2023.findings-emnlp.1007):
```bibtex
@inproceedings{limkonchotiwat-etal-2023-mrefined,
    title = "m{R}e{F}in{ED}: An Efficient End-to-End Multilingual Entity Linking System",
    author = "Limkonchotiwat, Peerat  and
      Cheng, Weiwei  and
      Christodoulopoulos, Christos  and
      Saffari, Amir  and
      Lehmann, Jens",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2023",
    month = dec,
    year = "2023",
    address = "Singapore",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.findings-emnlp.1007",
    doi = "10.18653/v1/2023.findings-emnlp.1007",
    pages = "15080--15089",
```

## mReFinED
- This is the replica of mReFinED from [Amazon's mReFinED](https://github.com/amazon-science/ReFinED/tree/mrefined).
- In contrast to mReFinED's paper, we add the Thai language.  
- We improve the training and inference codes to make them easier to reproduce.
- We also provide the mReFinED model and training data :) 

## Hardware Requirements
- mReFinED has a low hardware requirement. For fast inference speed, a GPU should be used, but this is not a strict requirement.
- We create training data for 15 days (CPU only).
- We use 8 V100 in the training step for ~10 days.
- For the inference setting, we use only a single V100.

# Model, Data, and Codes

## Materials
- **Model**: XXXXXXX
- **Training data**: XXXXXXXX

## Example Script
- mReFinED: Creating training data
```
cd mReFinED/src/
export PYTHONPATH=$PYTHONPATH:src
python refined/offline_data_generation/preprocess_all_multilingual_combine.py
```
- mReFinED: Training
```
cd mReFinED/src/
export PYTHONPATH=$PYTHONPATH:src
bash refined/training/train/multilingual_train.sh
```
- Mention Detection For Unlabeled Entity in Wikipedia
```
cd mReFinED/src/refined/training/train
python multilingual_md_train_xtreme.py
python md_on_wiki.py
python multilingual_md_train_xtreme_wikipedia.py
```
- mReFinED: Inference
```python
print('hi')
```
- mReFinED on Mewsli-9
```python
print('hi')
```  
 
## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the CC-BY-NC 4.0 License.

## Contact us
If you have questions please open Github issues instead of sending us emails, as some of the listed email addresses are no longer active.
