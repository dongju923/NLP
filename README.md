# NLP(자연어 처리_1.ipynb)

## 단어 토큰화  
1. 파이썬 내장 함수 `split()`을 이용한 토큰화  
```python
from nltk.tokenize import word_tokenize
```
2. nltk패키지의 `word_tokenize()`함수를 사용한 토큰화  
#### 한국어의 토큰화는 KoNLPy패키지 사용  
1. 한국어의 형태소 분석은 `pos()`함수 이용  
2. 형태소만 실행할 때는 `morphs()`함수 이용  
3. 명사만 사용하고 싶을 때는 `nouns()`함수를 이용하여 조사, 접속사 등을 제거  

---
## 문장 토큰화
1. `split('\n')`을 사용한 토큰화
```python
from nltk.tokenize import sent_tokenize
```
2. nltk패키지의 `sent_tokenize()`를 사용한 문장 토큰화  
#### 한국어의 문장 토큰화  
1. kss라이브러리를 사용해 `split_sentences()`함수를 사용해 문장 토큰화  
&#42; 한국어는 전치 표현이 존재해 제대로 토큰화가 안되기 때문에 사용자가 따로 처리해야 함 &#42;  

---
## 정규 표현식을 이용한 토큰화
```python
from nltk.tokenize import RegexpTokenizer
```
1. nltk패키지의 `RegexpTokenizer`를 사용  
2. 한국어도 토큰화 가능  

---
## TextBlob을 이용한 토큰화
```python
from textblob import TextBlob
```
1. `TextBlob()`함수를 이용한 토큰화  
2. 한국어도 토큰화 가능  

---
## 케라스를 이용한 토큰화
```python
from keras.preprocessing.text import text_to_word_sequence
```
1. `text_to_word_sequence()`함수를 사용한 토큰화
2. 한국어도 토큰화 가능

---
## 품사 태깅
1. `nltk.download('averaged_perceptron_tagger')`를 사용하여 필요한 데이터 다운로드  
2. `pos_tag()`를 이용하여 품사 태깅 가능

---
### n-gram추출
### 불용어 제거
### 철자 교정
### 단수화, 복수화
### 어간 추출
### 표제어 추출
### 개체명 인식
### 의존 구문 분석

---
# NLP(자연어 처리_2.ipynb)

## 명사 추출  
1. Mecab을 사용한 명사 추출  
```python
from knolpy.tag import Mecab
tagger = Mecab()
tagger.nouns()
```
## 단어 빈도수 측정  
1. 단어 빈도수 측정에는 `collections`라이브러리의 `Counter()`함수를 이용
```python
from collections import Counter
```
## 트리맵 시각화  
```python
import squarify
```
## 워드클라우드 시각화
```python
from wordcloud import WordCloud
```

---
# NLP(자연어 처리_3.ipynb)

## 텍스트 처리
## 정규표현식
## 어휘 빈도-문서 역빈도(TF-IDF)
## 로지스틱 회귀
## 나이브 베이스 분류기
## 서포트 벡터 머신
## 확률적 경사 하강법
## 결정 트리
## 랜덤 포레스트
## XGBoost
