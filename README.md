### 모델 / 평가

* 학습 데이터는 데이콘에서 개최한 경진대회 데이터를 활용했습니다. (https://dacon.io/competitions/official/236216/overview/description)
* train data는 전처리 과정 없이 단순히 데이콘에서 주어진 train 데이터를 학습한 것을 의미합니다.
* train_preprocess_data_aug는 데이콘에서 주어진 train 데이터를 전처리하고 증강한 데이터를 의미합니다. 자세한 방법은 preprocess.ipynb 파일에서 확인할 수 있습니다.
* 이번 경진대회에서 활용한 모델은 모두 QLoRA 기법으로 fine-tuning을 진행했습니다.
* 성능은 데이콘 리더보드에서 계산된 Public 점수(코사인 유사도)입니다.
* 최종적으로 KoSOLAR 모델을 통해 Public 23위를 기록했습니다.

|파일명|성능|Epoch|학습 데이터|Public 순위|
|------|---|-----|----------|-----------|
|KoSOLAR|0.79|5|train_preprocess_data_aug|23위|
|KoSOLAR|0.74|4|train_preprocess_data_aug||
|Llama-2-koen-13b|0.70|5|train_preprocess_data_aug||
|Llama_7b_original| |5|train data||
|Llama_7b|0.70|5|train_preprocess_data_aug||
|KoAlpaca|0.63|3|train data||

* 학습으로 활용한 사전학습 LLM 모델은 다음과 같습니다.
* KoSOLAR: https://huggingface.co/kimwooglae/WebSquareAI-Instruct-KoSOLAR-10.7b-v0.5.34
* Llama-2-koen-13b: https://huggingface.co/beomi/llama-2-koen-13b
* Llama_7b: https://huggingface.co/beomi/llama-2-ko-7b
* KoAlpaca: https://huggingface.co/beomi/KoAlpaca-Polyglot-5.8B