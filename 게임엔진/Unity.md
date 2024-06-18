# Unity
---
## 목차
1. [컴포넌트](#컴포넌트(Component))
---
## 2024_06_12
유니티 C# 스크립트에서 Start() 메소드는 Update()메서드가 호출되기 전 한번 호출됨 Update()메서드는 매 프레임 마다 호출.  
InPut.GetAxis("Vertical")은 'A','D'와 좌우 방향키를 키다운시 -1에서 1값을 리턴.  
InPut.GetAxis("Horizontal")은 'W','S'와 상하 방향키를 키다운시 -1에서 1값을 리턴.  
Time.deltaTime은 1초를 프레임을 나눈값, 기기마다 프레임이 달라도 같은 결과를 만들때 사용.  

## 2024_06_13
사물의 Rigidbody 컴포넌트를 추가해서 중력,충돌등 물리 요소를 추가할수 있음  
onCollisionEnter 이벤트는 사물이 충돌시 호출되는 이벤트  
Audio Source 컴포넌트는 소리를 추가해줄수 있음  
Collider이름을 가진 컴포넌트는 사물에 충돌 범위를 지정가능 물리요소를 지상위에 있게 할려면 필수  
Transform클래스에는 Transform 컴포넌트가 붙어 있는 게임 오브젝트 기준으로 상대 방향 벡터로 변환해주는 TransformDirection()함수가 있음  

## 컴포넌트(Component)
Rigidbody 와 Charactor Controller의 차이
priority의 값에 따라서 같은 기능이 동시에 활성화 되어도 우선선적으로 작동하게할 기능을 선택 가능하다 (값이 높을수로 우선순위가 높음)  




