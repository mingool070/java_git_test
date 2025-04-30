HTML, CSS, JavaScript를 활용한 **쇼핑몰 FrontEnd 프로젝트**는 웹 브라우저에서 사용자가 상품을 보고, 선택하고, 장바구니에 담고, 결제 페이지로 이동하는 과정을 **시각적이고 동적인 웹 인터페이스**로 구현하는 프로젝트입니다.

---

## 🛍️ 쇼핑몰 FrontEnd 프로젝트 구성 설명

### 1. **HTML (구조)**
HTML은 웹 페이지의 뼈대를 담당합니다.

- `index.html`: 메인 홈 페이지, 제품 목록 나열
- `product.html`: 제품 상세 설명 페이지
- `cart.html`: 장바구니 페이지
- 각 HTML 파일에는 공통적으로 헤더, 네비게이션, 푸터 포함

#### 예시
```html
<div class="product-card">
  <img src="assets/images/shirt.jpg" alt="셔츠">
  <h2>깔끔한 흰 셔츠</h2>
  <p>₩25,000</p>
  <button>장바구니에 담기</button>
</div>
```

---

### 2. **CSS (스타일)**
CSS는 페이지를 보기 좋게 디자인합니다.

- 레이아웃 구성 (Flexbox, Grid)
- 버튼, 텍스트, 카드 스타일링
- 반응형 디자인 (모바일 대응)

#### 예시
```css
.product-card {
  border: 1px solid #ddd;
  padding: 1rem;
  border-radius: 8px;
  width: 200px;
}
```

---

### 3. **JavaScript (동작/기능)**
JavaScript는 페이지에 **동적인 기능**을 추가합니다.

- 장바구니 기능 (제품 담기, 삭제)
- 수량 조절 및 총합 계산
- 로컬 스토리지 사용: 새로고침해도 장바구니 유지
- 버튼 클릭 시 페이지 이동 또는 동작 수행

#### 예시
```javascript
const addToCart = (productId) => {
  let cart = JSON.parse(localStorage.getItem("cart")) || [];
  cart.push(productId);
  localStorage.setItem("cart", JSON.stringify(cart));
  alert("장바구니에 담겼습니다!");
}
```

---

## 💡 주요 페이지 요약

| 페이지 | 설명 |
|--------|------|
| **index.html** | 전체 상품 목록을 보여주는 메인 |
| **product.html** | 선택한 상품의 상세 정보를 보여주는 페이지 |
| **cart.html** | 장바구니에 담긴 상품 확인 및 결제 진행 |

---

## ✅ 기술적으로 배우는 점

- **HTML/CSS 기본 구조와 구성 능력**
- **DOM 조작과 이벤트 처리** (JS)
- **로컬 스토리지 활용법**
- **사용자 경험(UX)을 고려한 인터페이스 구성**
- **기본적인 코드 구조 설계와 유지 관리**

---
