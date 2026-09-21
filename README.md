# test15

// [TypeScript] 인터페이스(Interface)를 활용한 장바구니 총액 계산

// 상품 데이터의 타입을 정의하는 인터페이스
interface Product {
  name: string;  // 상품명 (문자열)
  price: number; // 가격 (숫자)
  count: number; // 수량 (숫자)
}

// Product 타입의 객체 배열 생성
const cart: Product[] = [
  { name: "키보드", price: 35000, count: 1 },
  { name: "마우스", price: 20000, count: 2 }
];

// 장바구니의 총 금액을 계산하는 함수 (반환 타입: number)
function calculateTotal(items: Product[]): number {
  return items.reduce((total, item) => total + (item.price * item.count), 0);
}

// 계산 결과 출력
const totalPrice = calculateTotal(cart);
console.log(`장바구니 총 결제 금액: ${totalPrice}원`);
