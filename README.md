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
> 
