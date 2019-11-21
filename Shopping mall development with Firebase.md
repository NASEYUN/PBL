# Firebase로 쇼핑몰 구현하기

### Firebase로 쇼핑몰 구현하기 시도한 내용
* 각 카테고리를 선택하면 해당 액티비티(Top, Bottom, Outer)로 이동한다.
* 각 카테고리 페이지로 이동하면 카테고리 별 제품을 GridView로 나열한다.
* 각 제품의 이름과 가격이 보여진다.

<img src="https://user-images.githubusercontent.com/55873484/68854996-a95cca80-0720-11ea-91dd-72655b22e44e.png" width=300></img>
<img src="https://user-images.githubusercontent.com/55873484/68855041-c0032180-0720-11ea-9d34-c34ed256b01c.png" width=300></img>
<img src="https://user-images.githubusercontent.com/55873484/68855044-c09bb800-0720-11ea-90d4-45a61c74311c.png" width=300></img>
<img src="https://user-images.githubusercontent.com/55873484/68855045-c09bb800-0720-11ea-89db-c47b3349efc2.png" width=300></img>
<img src="https://user-images.githubusercontent.com/55873484/68855047-c09bb800-0720-11ea-95fc-0d8db3da3120.png" width=300></img>
<img src="https://user-images.githubusercontent.com/55873484/68855048-c1344e80-0720-11ea-9cb6-4755bce9b19d.png" width=300></img>
<img src="https://user-images.githubusercontent.com/55873484/68855049-c1344e80-0720-11ea-92ca-f14f794d2a38.png" width=300></img>

### 문제점 분석
* Firebase에서 불러온 값은 저장되지만 보여지는 속도가 매우 느리다.
* Realtime Database나 Firestore나 쿼리가 빈약하다.
  * 특히 검색 쿼리의 종류가 매우 제한적이다. 관계형 데이터베이스의 LIKE문도 존재하지 않기 때문에 비슷한 데이터도 검색을 할 수 없다. 모든 케이스를 고려하여 작성해야 한다.
* Storage에 이미지를 저장하였으나, imageView에 불러 오지 못했다.

### 대안 제시
