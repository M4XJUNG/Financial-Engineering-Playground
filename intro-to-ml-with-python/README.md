# [개정2판] 파이썬 라이브러리를 활용한 머신러닝

#### 사이킷런(Scikit-Learn) 핵심 개발자가 쓴 머신러닝과 데이터 과학 실무서

![cover](cover.jpg)

이 레파지토리는 안드레아스 뮐러(Andreas Mueller)와 세라 가이도(Sarah Guido)의 책인 "Introduction to Machine
Learning with Python"의 번역서 "[(개정2판)파이썬 라이브러리를 활용한 머신러닝](https://tensorflow.blog/python-ml-2nd-revised/)"의 코드와 주피터 노트북을 담고 있습니다. 개정2판은 **풀 컬러 인쇄**이며 사이킷런의 1.x의 최신 기능과 한글 부록이 포함되어 있습니다.

##### ** 개정1판의 코드는 [여기](https://github.com/rickiepark/introduction_to_ml_with_python/)를 참고하세요. **

이 책의 내용은 Python 3.7, 3.10, scikit-learn 1.0.1, 1.2, 1.3에서 테스트 되었습니다.

이 레파지토리는 책에 포함된 코드를 주피터 노트북 형태로 가지고 있으며 그래프와 데이터셋을 위한 ``mglearn`` 라이브러리를 함께 제공합니다.
aclImdb 데이터셋과 Naver sentiment movie corpus를 제외하고는 책에서 사용하는 데이터도 모두 포함하고 있습니다.
aclImdb 데이터셋은 앤드류 마스(Anrew Mass)의 [웹사이트](http://ai.stanford.edu/~amaas/data/sentiment/)에서 다운받을 수 있습니다. 자세한 내용은 책을 참고하세요.
Naver sentiment movie corpus는 루시 님의 [깃허브](https://github.com/e9t/nsmc/)에서 다운받을 수 있습니다.

책 커버에 있는 도룡뇽은 [헬벤더](https://ko.wikipedia.org/wiki/%ED%97%AC%EB%B2%A4%EB%8D%94)입니다.

## 에러타(Errata)

"[(개정2판)파이썬 라이브러리를 활용한 머신러닝](https://tensorflow.blog/python-ml-2nd-revised/)"의 에러타는 옮긴이의 [블로그](https://tensorflow.blog/python-ml-2nd-revised/)에서 확인할 수 있습니다. 코드에 오류가 있다면 깃허브에 이슈를 남겨 주시거나 옮긴이의 [블로그](https://tensorflow.blog/python-ml-2nd-revised/)를 통해 연락 주세요.

## 설치

이 코드를 실행하려면 ``numpy``, ``scipy``, ``scikit-learn``, ``matplotlib``, ``ipython``, ``pandas``, ``imageio``와 ``pillow`` 패키지가 필요합니다.
결정 트리와 신경망 구조에 대한 그래프를 그리려면 ``graphviz``도 필요합니다. 7장 텍스트 데이터 다루기에서는 ``ntlk``와 ``spacy``도 사용합니다.

[아나콘다](https://www.continuum.io/downloads)(Anaconda)나 pip를 사용해 개발 환경을 만드는 것이 편리한 방법입니다.

### conda를 사용한 패키지 설치

설치된 파이썬이 있다면 ``conda`` 패키지 매니저를 사용하여 다음 명령을 실행하면 필요한 패키지를 모두 얻을 수 있습니다.

    conda install numpy scipy scikit-learn matplotlib ipython pandas imageio pillow graphviz python-graphviz

7장을 위해서는 ``nltk``와 ``spacy``도 설치해야 합니다.

    conda install nltk spacy

### pip를 사용한 패키지 설치

파이썬이 있고 pip를 사용하여 패키지를 설치하려면 다음 명령을 사용합니다.

    pip install numpy scipy scikit-learn matplotlib ipython pandas pillow imageio graphviz

또한 graphviz C 라이브러리를 설치해야 합니다. 패키지 매니저를 사용하여 쉽게 설치할 수 있으며 macOS는 homebrew를 사용하여 ``brew install graphviz`` 명령을 사용합니다. 우분투나 데비안이라면 ``apt-get install graphviz`` 명령을 사용합니다. 윈도우즈에서 graphviz를 설치하는 것은 쉽지 않습니다. 대신 conda나 아나콘다를 사용하세요. 7장을 위해서는 ``nltk``와 ``spacy``도 설치해야 합니다.

    pip install nltk spacy

### 영어 언어 모델 다운로드하기

7장에서 ``spacy``의 영어 언어 모델을 다운로드하려면 다음 명령을 사용합니다.

    python -m spacy download en


### 공부 사이트 정리 
[ 홍대 머신 러닝 스터디(https://www.meetup.com/Hongdae-Machine-Learning-Study/) (epoch #2)의 "파이썬 라이브러리를 활용한 머신러닝"(옮긴이 박해선) 슬라이드 자료. ]
- [1.introduction(epoch#2)](https://www.slideshare.net/slideshow/1introductionepoch2/81331715)
- [2.supervised learning(epoch#2)-1](https://www.slideshare.net/slideshow/2supervised-learningepoch21/81376909)
- [2.supervised learning(epoch#2)-2](https://www.slideshare.net/slideshow/2supervised-learningepoch22/81921021)
- [2.supervised learning(epoch#2)-3](https://www.slideshare.net/slideshow/2supervised-learningepoch23/82877781)
- [3.unsupervised learing(epoch#2)](https://www.slideshare.net/slideshow/3unsupervised-learingepoch2/83847096)
- [4.representing data and engineering features(epoch#2)](https://www.slideshare.net/slideshow/4representing-data-and-engineering-featuresepoch2/85852414)
- [5.model evaluation and improvement(epoch#2) 1](https://www.slideshare.net/slideshow/5model-evaluation-and-improvementepoch2-1-87291436/87291436)
- [5.model evaluation and improvement(epoch#2) 2](https://www.slideshare.net/slideshow/5model-evaluation-and-improvementepoch2-2-87291677/87291677)
- [6.algorithm chains and piplines(epoch#2)](https://www.slideshare.net/slideshow/6algorithm-chains-and-piplinesepoch2/88363838)
- [7.woring with text data(epoch#2)](https://www.slideshare.net/slideshow/7woring-with-text-dataepoch2/88363848)
