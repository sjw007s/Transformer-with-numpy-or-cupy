# Transformer-with-numpy-or-cupy
E-mail: sjw007s@korea.ac.kr
Transformer with numpy or cupy // Transformer without frameworks.

This is a code that implements the transformer in the paper below with numpy or cupy.
Vaswani, Ashish, et al. "Attention is all you need." arXiv preprint arXiv: 1706.03762 (2017).
Perhaps this is the first publicly available code to implement the transformer without frameworks.
TensorFlow and Pytorch can implement the transformer, but it makes all the arrays to see how the transformer works in detail.
It reproduces weight generation, forward propagation, and back propagation except for a batch normalization layer.
It was confirmed that bleu 1.0 was obtained with 9 sentences (data included, Korean->English data).
It was confirmed that bleu 1.0 was obtained with 100 sentences (data not included, a project is in progress, Korean->Korean sign language data).
I think it will be useful for those who want to acquire the ability to implement artificial neural networks without the frameworks.
The code has been transformed using https://github.com/KONANtechnology/Academy.ALZZA.

How to run: Run the last code in chap15/NLP_result.ipynb.
This code is set up with the cupy library to compute numpy on the GPU.
To run it with cpu
1. Remove 'import cupy as np' from 'chap01/abalone.ipynb' and enable 'import numpy as np'.
2. Remove 'import cupy as np' from 'chap05/mathutil.ipynb' and enable 'import numpy as np'.
3. Remove 'with np.cuda.Device(0):' in chap15/NLP_result.ipynb.

Unnecessary codes are inserted in the middle.
Unnecessary operations may be performed.
Code is not optimized for computational speed.

---------------------------------------------------------

아래 논문에서 구현된 transformer를 numpy 또는 cupy로 구현한 코드입니다.
Vaswani, Ashish, et al. "Attention is all you need." arXiv preprint arXiv:1706.03762 (2017).
아마도 이 코드가 프레임워크 없이 transformer를 구현한 공개된 첫 코드일 것입니다.
텐서플로우와 파이토치로도 충분히 구현이 가능하지만, 구체적으로 내부가 어떻게 동작하는지 보기 위해 배열을 전부 선언하여
가중치 생성, 순전파, 역전파를 전부 구현한 것이 특징입니다.
batch normalization layer는 제외되고 구현되었습니다.
한국어-영어 1대1 대응 9문장(데이터 포함)으로 bleu 1.0을 얻어내는 것을 확인하였으며
한국어-한국수어문장 1대1 대응 100문장(데이터 미포함, 과제 수행중)으로 bleu 1.0을 얻어내는 것을 확인하였습니다.
인공신경망을 자유자재로 구현하는 능력을 얻고싶은 분들에게 유용할 것이라 생각합니다.
해당 코드는 https://github.com/KONANtechnology/Academy.ALZZA 을 이용하여 만들었습니다.

실행방법: chap15/NLP_result.ipynb 에서 맨 마지막 코드를 실행하시면 됩니다.
이 코드는 numpy를 GPU로 연산시키기 위해 사용하는 cupy 라이브러리로 설정되어 있습니다.
cpu로 돌리기 위해서는 
1. 'chap01/abalone.ipynb' 에서 'import cupy as np' 를 삭제하고 'import numpy as np'를 활성화하세요.
2. 'chap05/mathutil.ipynb' 에서 'import cupy as np' 를 삭제하고 'import numpy as np'를 활성화하세요.
3. 'with np.cuda.Device(0):'를 제거하세요.

필요없는 코드들이 중간에 삽입되어있습니다.
필요없는 연산이 진행될 수 있습니다.
코드는 계산 속도에 최적화되어 있지 않습니다.






