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

## 캐스팅
캐스팅 함수의 종류는 Physics와 Physics2D가 조금 달라질 수 있다  
3D와 2D가 다르듯 구형태 캐스팅은 2D에서 원영태 캐스팅으로 정의되어 있다   
### Raycast(), SphereCast(), BoxCast(), CapsuleCast() 
일반적으로 첫번째로 충돌된 오브젝트에 대한 여부를 나타냄  
bool값의 반환값을 받거나 RayCastHit 타입의 객체를 반환
### RaycastAll(), SphereCastAll(), BoxCastAll(), CapsuleCastAll()
RayCastHit[] 타입의 배열을 반환한다   
첫번째 충돌에 대한 정보가 아닌 최대거리까지 캐스트 영역을 발사하여 충돌한 모든 오브젝트의 정보를 반환
### LineCast(Vector3 a, Vector3 b)
a와 b 사이에 충돌될 오브젝트가 있는지 여부를 반환한다 실질적으로 Raycast의 시작점을 a, 방향을 b를 바라보고 최대거리를 a,b사이 거리를 넣는다면 같은 기능이지만   
Vector3값 두개만을 인자로 받기 때문에 두 물체사이의 충돌물체검증에 있어서 훨씬 간편하게 사용할수 있음


