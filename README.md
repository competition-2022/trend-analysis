## 트렌드 분석 프레임워크
트렌드 분석 프레임워크는 디지털기술, 핀테크, 지급결제 등 특정 주제에 대해서만 국한하여 사용할 수 있는 것이 아니라, 분석하고자 하는 주제에 대한 텍스트 형태의 데이터만 있다면 동 프레임워크을 적용하여 해당 주제에 대한 트렌드를 분석할 수 있다.

--------------------------------------------------------------------------------

**아키텍처**

뉴스, 논문 등 트렌드 분석을 하고자 하는 주제와 관련된 ① 텍스트 데이터를 수집하여 입력하면, 분석에 적합한 형태로 ②전처리한 후 ③-(1)단어 순위 계산, ③-(2)동시출현 단어 계산, ③-(3)토픽 모델링을 수행한다. 그리고 ③의 결과로 ④-(1) 키워드 분석, ④-(2) 키워드 네트워크 분석, ④-(3) 시계열 토픽 분석을 수행한다.
<p align="center">
<img width="50%" src="https://user-images.githubusercontent.com/32153781/190425371-668e2395-11db-4313-b5ea-8b052eccfdb3.png" />
</p>

--------------------------------------------------------------------------------

**트렌드 분석 실험**

트렌드 분석 프레임워크를 사용하여 ‘지급결제’에 대한 트렌드 분석을 다음과 같이 Payments Strategy & Systems 저널 논문(이하 JPSS), 한국지급결제학회지 논문(이하 KPSA), 네이버 뉴스(이하 News)를 대상으로 수행하였다.

|매체|수집대상|분석대상|
|------|---|---|
|국외논문|[Journal of Payments Strategy & Systems(JPSS)](https://www.henrystewartpublications.com/jpss)|총164편 초록|
|국내논문|[한국지급결제학회지(KPSA)](http://www.kpsa.kr/)|총93편 초록|
|뉴스|[네이버 뉴스 카테고리](https://news.naver.com/)-‘지급결제’검색 (News)|총8119건 본문|

--------------------------------------------------------------------------------

**소스코드 실행 예시**

```sh
$ python kpsa.py
```
