# continual-pretrain-tinyllama

추가 사전학습 실습용 코드입니다. 자세한 설명은 다음 글을 참고하길 바랍니다: [글 링크](https://jkspace.notion.site/11-20-238b1a84a5a9409fb895ce349fef85e1?pvs=4)

본 실습에서는

1. 한국어 뉴스 데이터로 사전학습을 하고
2. 상담 데이터로 추가 사전학습(Continual Pretraining)을 해도
3. 첫 번째 도메인(뉴스 데이터)에 대한 정보를 모델이 잘 기억하고 있는지 확인하는 것을 목표로 합니다.
   
📌 특히 Colab에서 돌릴 때, HuggingFace (이하, HF) Hub에 데이터셋, 체크포인트를 백업하는 것을 권장합니다.

다음 데이터셋을 사용합니다. 이미 사전학습을 위해 청크로 나누었고, 토큰화한 데이터셋입니다.
방법 및 코드는 `Continual_Pretraining_With_TinyLlama_120M.ipynb`의 `Create Dataset` 섹션에서 볼 수 있습니다.

* 첫 번째 사전학습 데이터셋 HF repo: [lectura/naver_news_1024](https://huggingface.co/datasets/lectura/naver_news_1024)
* 두 번째 사전학습 데이터셋 HF repo: [lectura/counsel-ko_1024](https://huggingface.co/datasets/lectura/counsel-ko_1024)

토크나이저는 이미 한국어로 학습된 것을 사용합니다.

* 토크나이저 HF repo: [beomi/llama-2-ko-7b](https://huggingface.co/beomi/llama-2-ko-7b)


