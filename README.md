<h1>storevibe</h1>
온라인 쇼핑몰 주문 관리 시스템<br><br>

<h3>ERD</h3>
<img src=https://github.com/user-attachments/assets/39b80dfb-c486-4f8b-89a5-342e41ac6879></img>


<h3>테이블 설계</h3>
<b>1. 고객(Customer) 테이블</b><br>
- 고객ID<br>
- 고객명<br>
- 이메일<br>
- 전화번호<br>
- 주소<br>
<b>2. 주문(Order) 테이블</b><br>
- 주문ID<br>
- 고객ID<br>
- 주문일<br>
- 총금액<br>
<b>3. 주문내역(OrderItem) 테이블</b><br>
- 주문내역ID<br>
- 주문ID<br>
- 상품ID<br>
- 수량<br>
<b>4. 상품(Product) 테이블</b><br>
- 상품ID<br>
- 상품명<br>
- 가격<br>


<h3>API 명세</h3>
<b>1. 고객<br>
<table>
  <thead>
    <tr>
      <th>기능</th>
      <th>메서드</th>
      <th>URL</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>회원가입</th>
      <th>POST</th>
      <th>/customers</th>
      <th>회원 가입을 할 수 있습니다.</th>
    </tr>
    <tr>
      <th>회원탈퇴</th>
      <th>DELETE</th>
      <th>/customers/{customer_id}</th>
      <th>회원 탈퇴를 할 수 있습니다.</th>
    </tr>
    <tr>
      <th>로그인</th>
      <th>POST</th>
      <th>/customers/login</th>
      <th>로그인을 할 수 있습니다.</th>
    </tr>
    <tr>
      <th>로그아웃</th>
      <th>POST</th>
      <th>/customers/logout</th>
      <th>로그아웃을 할 수 있습니다.</th>
    </tr>
  </tbody>
</table>
  
<b>2. 주문<br>
<table>
  <thead>
    <tr>
      <th>기능</th>
      <th>메서드</th>
      <th>URL</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>주문 생성</th>
      <th>POST</th>
      <th>/orders</th>
      <th>새로운 주문을 생성합니다.</th>
    </tr>
    <tr>
      <th>전체 주문 조회</th>
      <th>GET</th>
      <th>/orders</th>
      <th>모든 주문을 조회합니다.</th>
    </tr>
    <tr>
      <th>주문 조회</th>
      <th>GET</th>
      <th>/orders/{order_id}</th>
      <th>특정 주문을 조회합니다.</th>
    </tr>
    <tr>
      <th>주문 삭제</th>
      <th>DELETE</th>
      <th>/orders/{order_id}</th>
      <th>특정 주문을 삭제합니다.</th>
    </tr>
  </tbody>
</table>
  
<b>3. 주문내역<br>
<table>
  <thead>
    <tr>
      <th>기능</th>
      <th>메서드</th>
      <th>URL</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>주문내역 조회</th>
      <th>GET</th>
      <th>/orders/{order_id}/items</th>
      <th>특정 주문의 주문내역을 조회합니다.</th>
    </tr>
  </tbody>
</table>
  
<b>4. 상품<br>
<table>
  <thead>
    <tr>
      <th>기능</th>
      <th>메서드</th>
      <th>URL</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>상품 조회</th>
      <th>GET</th>
      <th>/products</th>
      <th>모든 상품을 조회합니다.</th>
    </tr>
    <tr>
      <th>특정 상품 조회</th>
      <th>GET</th>
      <th>/products/{product_id}</th>
      <th>특정 상품을 조회합니다.</th>
    </tr>
    <tr>
      <th>상품 추가</th>
      <th>POST</th>
      <th>/products</th>
      <th>새로운 상품을 추가합니다.</th>
    </tr>
    <tr>
      <th>상품 삭제</th>
      <th>DELETE</th>
      <th>/products/{product_id}</th>
      <th>특정 상품을 삭제합니다.</th>
    </tr>
  </tbody>
</table>
