# Unity_Survirus
> 생존 게임 (2021. 10 ~ 2022. 05) <br/>
> Unity3D C# <br/>

<img src="https://user-images.githubusercontent.com/87380790/176414953-da306067-9f11-435e-b8ae-02ecbb68ad79.PNG" width="80%">

### [>> Steam Store Page <<](https://store.steampowered.com/app/1927040/Survirus/) <br/>

<br/>
<br/>
<br/>
  
## 1. 시작 화면
> 새 게임, 불러오기, 옵션, 크레딧 지원


<img src="https://user-images.githubusercontent.com/87380790/176414053-aaaf6ba3-9c42-49f5-82d6-622bbe4cea4e.gif" width="80%">


- Timeline을 활용한 크레딧<br/><br/>
- SceneManager.LoadSceneAsync()를 활용하여 첫 로딩 시 스토리 보여줌 <br/><br/>
- Animation으로 알파값을 조정하여 Fade In 장면 전환<br/>

<br/>
<br/>
<br/>
  
## 2. 상호작용
> 카메라에서 Raycast를 쏘아 상호작용 물체 식별
> 
<img src="https://user-images.githubusercontent.com/87380790/176413883-80c67438-98c8-42f5-8a47-3441e9b0cf4e.gif" width="80%">

- UnityEvent를 통해 물체에 따라 다른 이벤트가 발생 <br/>

<br/>
<br/>
<br/>

## 3. 인벤토리
> 사각형 칸을 베이스로 한 인벤토리와 가방
> 
<img src="https://user-images.githubusercontent.com/87380790/176413923-d181ae42-f7f1-4c40-a0b8-b0d4025f9c24.gif" width="80%">

- List를 foreach문으로 돌면서 하나씩 아이템 RectTransform을 Instantiate()   <br/><br/>
- 인덱스에 따라 좌표 설정, 마우스 리스너 추가, 이미지, 수량, 툴팁 세팅   <br/><br/>
- IDragHandler를 이용하여 Drag & Drop을 지원, 인벤토리와 가방 간의 아이템 이동 가능   <br/><br/>
- 아이템 정렬 버튼<br/>

<br/>
<br/>
<br/>

## 4. 장비 착용
> 아이템 장착, 교체 가능, 아이템별로 다른 효과를 지님
<img src="https://user-images.githubusercontent.com/87380790/176413932-6d113e92-ef75-46ad-b373-aba31583ab0c.gif" width="80%">

<br/>
<br/>
<br/>

## 5. 아이템 사용
> 체력 회복, 음식, 마실 것 등
> 
<img src="https://user-images.githubusercontent.com/87380790/176413960-6ae0a0a0-9275-455a-8b4b-d4ffac4444dd.gif" width="80%">

- Coroutine 으로 시간에 따라 체력, 배고픔, 목마름 등 변동   <br/><br/>
- 아이템을 사용하여 체력, 배고픔, 목마름 회복   <br/><br/>
- 아이템별로 다른 효과를 지님 (버프 아이템 포함)   <br/><br/>
- 취소 가능한 3초 딜레이<br/>

<br/>
<br/>
<br/>

## 6. 보관함
> 각각의 독립적인 보관함, 아이템 랜덤 스폰
> 
<img src="https://user-images.githubusercontent.com/87380790/176413942-1c0c5b69-7ef5-401e-91c4-a9d33320c39e.gif" width="80%">

<br/>
<br/>
<br/>

## 7. 적 AI
> Idle, 추격, 공격, 회귀 상태를 상황에 따라 반복
> 
<img src="https://user-images.githubusercontent.com/87380790/176473318-ef6374d0-96e9-4649-ac59-1e989e9f915a.gif" width="80%">
<img src="https://user-images.githubusercontent.com/87380790/176473329-f004e516-1fd1-4efc-90b2-932c9b4f42bc.gif" width="80%">
<img src="https://user-images.githubusercontent.com/87380790/176473341-9dbbe58d-a002-4fa6-883a-b20f0af99bdf.gif" width="80%">

- Coroutine 객체에 현재 상태를 지정해주어 상태 간 충돌 방지   <br/><br/>
- 각기 다른 공격 패턴의 3가지 적     <br/><br/>
- 특정 체력 이하로 내려갈 시 슈퍼아머 공격   <br/><br/>
- 처치 시 약탈 가능   <br/>

<br/>
<br/>
<br/>

## 8. NPC 상호작용
> NPC와 대화, 거래, 퀘스트
> 
<img src="https://user-images.githubusercontent.com/87380790/176413977-a92bbcf7-3f76-4f9f-8b0c-a4190efe1564.gif" width="80%">
<img src="https://user-images.githubusercontent.com/87380790/176413982-9d0e9360-300b-4bdc-8d7b-8fd6790c59b6.gif" width="80%">

- NPC와 대화한 날짜나 전체 날짜를 기준으로 달라지는 대사   <br/><br/>
- 날마다 바뀌는 상인의 아이템들   <br/><br/>
- 특정 NPC의 이벤트<br/>

<br/>
<br/>
<br/>

## 9. 버프, 디버프
> Coroutine을 활용한 5가지 디버프와 2가지 버프
> 
<img src="https://user-images.githubusercontent.com/87380790/176413988-ac4343d3-2297-40a3-b379-4bb568273f94.gif" width="80%">

- 출혈 : 칼이나 총에 맞았을 경우 20% 확률로 발생, 초당 1의 체력 감소   <br/><br/>
- 감염 : 바이러스에 접촉 시 일정 확률에 따라 발생, 잠복기 있으며 점점 상태 악화, 8분 이후 사망   <br/><br/>
- 정신분열 : 스트레스 지수 80 이상일 시 발생, 시야가 흐려지며 이동속도 감소   <br/><br/>
- 중독 : 약을 자주 복용하거나 담배를 자주 피울 시 발생, CinemachineFreeLook 컴포넌트의 m_XAxis, m_YAxis를 변동하여 카메라가 떨림 <br/><br/>  
- 오염 : 바이러스 비를 5초 이상 맞을 시 발생, 이후 음식 섭취 시 50% 확률로 감염   <br/><br/>
- 각성 : 커피 섭취 시 발생, 이동속도와 공격 시 스태미너 감소율 감소   <br/><br/>
- 진통 : 진통제 섭취 시 발생, 20의 보호막 생성   <br/>

<br/>
<br/>
<br/>

## 10. 실시간 해의 움직임
> 게임 내에서 정해진 시간에 따라 해가 움직임 (20배속)
> 
<img src="https://user-images.githubusercontent.com/87380790/176414036-5c083b02-a9d4-47b5-ad5d-ec7245801289.gif" width="80%">

- Coroutine으로 흘러가는 시간   <br/><br/>
- 흘러가는 시간에 맞춰 Quaternion.Euler() 를 활용해 해가 끊임없이 움직임   <br/><br/>
- 일출, 일몰 구현을 위해 RenderSettings.skybox의 AtmosphereThickness와 SkyTint 값 조절   <br/>

<br/>
<br/>
<br/>

## 11. Wave
> 하루마다 찾아오는 두가지 Wave
> 
<img src="https://user-images.githubusercontent.com/87380790/176414004-a24eb7bb-e3ff-4409-a6b5-baf5eb78f5e7.gif" width="80%">
<img src="https://user-images.githubusercontent.com/87380790/176414023-61ea3087-770f-481c-91d9-d945778bf651.gif" width="80%">

- 바이러스 확산 범위가 급증하는 Wind Wave, 바이러스 비가 내리는 Rain Wave      <br/><br/>
- 아침마다 랜덤 시간과 랜덤 길이를 정하고, 해당 시각에 Wave 시작      <br/><br/>
- OnParticleCollision 으로 비, 바이러스와 충돌시 이벤트 발생   <br/><br/>
- Color.Lerp()를 이용하여 RenderSettings.skybox의 AtmosphereThickness와 SkyTint 값을 조절하여 하늘 색 변경  <br/> 


<br/>
<br/>
<br/>

## 12. 엔딩
> 특정 조건 달성 시 엔딩
> 
<img src="https://user-images.githubusercontent.com/87380790/176414043-b6bc5fdb-25cc-4287-9d6c-0d32e6e03b40.gif" width="80%">

- Timeline을 활용한 엔딩 씬과 크레딧   


<br/>
<br/>
<br/>

Steam store page : https://store.steampowered.com/app/1927040/Survirus/



















