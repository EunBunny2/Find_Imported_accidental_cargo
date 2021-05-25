# Find_Imported_accidental_cargo
2021 관세청 수입화물 우범도 예측 AI 경진대회
<br><br>
> <h3>배경 및 목적</h3> <br>
> 수입 화물 검사 인력의 한계를 극복하기 위해 고위험물품을 선별하여 선제적으로 차단하는 AI를 개발한다.
<br><br>
> <h3>데이터 분석</h3>
> <h4>- 신고일자에 따른 우범률 분석</h4>
> Try 1 : 한 달을 반으로 갈라서 월초, 월말로 구분한다<br>
> Try 2 : 분기별로 나눈다<br>
> Try 3 : 더울 때, 추울 때를 구분해 10~3월, 4~9월로 나눈다<br>
> <b>=>Try 3에서 정상 데이터와 우범 데이터의 차이가 가장 크다</b>
![image](https://user-images.githubusercontent.com/44043468/119469792-a8c7da00-bd82-11eb-8176-23cb0eda7318.png)
  
<br><br>
> <h4>- 데이터 값이 다양한 항목들에 대한 처리</h4>
> 아래 그래프는 특송업체부호에 따른 정상 및 우범 데이터를 나타낸 그래프이다.<br>
> 한 항목이 갖는 데이터 값이 다양할 경우 One-Hot-Encoding 했을 때 칼럼 수가 매우 커진다.<br><br>
> Try 1 : 부호의 첫 번째 문자로 묶는다.<br>
> Try 2 : nan일 때와 nan이 아닐 때로 구분한다.<br>
> Try 3 : 정상과 우범의 비율에 따라 묶는다.<br>
> <b>=>Try 2도 유의미한 시도였으나 Try 3의 성능이 더 좋았다. 부호가 복잡한 데이터는 모두 Try 3 방법을 사용하여 전처리한다.</b>
![image](https://user-images.githubusercontent.com/44043468/119470547-6bb01780-bd83-11eb-8ee3-ab46ff2f9b70.png)

> <h3>데이터 전처리</h3>
> ![image](https://user-images.githubusercontent.com/44043468/119539173-df274880-bdc6-11eb-8c51-e9b2680a77d6.png)
![image](https://user-images.githubusercontent.com/44043468/119539207-e51d2980-bdc6-11eb-81d1-04c4c68ed202.png)
![image](https://user-images.githubusercontent.com/44043468/119539233-ea7a7400-bdc6-11eb-83c9-a710ef82393b.png)
![image](https://user-images.githubusercontent.com/44043468/119539260-f1a18200-bdc6-11eb-8fb5-150aae58fd36.png)
![image](https://user-images.githubusercontent.com/44043468/119539288-f8c89000-bdc6-11eb-80b9-382fa2f91287.png)
![image](https://user-images.githubusercontent.com/44043468/119539308-fd8d4400-bdc6-11eb-839f-18df022a29f2.png)
![image](https://user-images.githubusercontent.com/44043468/119539327-03832500-bdc7-11eb-8ad8-55c8e9caa270.png)
![image](https://user-images.githubusercontent.com/44043468/119539345-07af4280-bdc7-11eb-9fde-be2bea831a10.png)
<br>
><h3> 모델 생성 및 훈련</h3>
![image](https://user-images.githubusercontent.com/44043468/119539360-0d0c8d00-bdc7-11eb-8cdf-453ada5d0937.png)
<br><br>
><h3> 모델 성능 평가</h3>
![image](https://user-images.githubusercontent.com/44043468/119539380-11d14100-bdc7-11eb-9120-1c2060ca74ce.png)
![image](https://user-images.githubusercontent.com/44043468/119539405-185fb880-bdc7-11eb-934c-7e5e37ca55d3.png)
![image](https://user-images.githubusercontent.com/44043468/119539438-24e41100-bdc7-11eb-83b0-024fb6732df8.png)
