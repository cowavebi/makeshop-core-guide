# 메이크샵 코어 PG(전자결제) 신청 가이드

메이크샵 코어(CORE) 고객 안내 매뉴얼입니다. 노션에서 이전했습니다.

## 폴더 구조

```
.
├── index.html       ← PG 신청 가이드 (사이트 접속 시 바로 이 페이지)
├── assets/
│   ├── style.css    ← 공통 디자인 (색상·여백)
│   └── cover.png    ← 상단 배너
└── images/          ← 가이드 화면 캡처 16장
```

## 공개 주소

GitHub Pages 설정 후:

```
https://cowavebi.github.io/makeshop-core-guide/
```

## 내용 수정하기

GitHub 웹에서 바로 고칠 수 있습니다.

1. `index.html` 선택
2. 오른쪽 위 **연필 아이콘(Edit this file)** 클릭
3. 글자를 고친 뒤 아래 **Commit changes** 클릭
4. 1~2분 뒤 사이트에 반영됩니다

찾기 쉽게 본문 앞뒤에 표시를 넣어뒀습니다.

```html
<!-- ▼▼▼ 본문 시작 ▼▼▼ -->
...
<!-- ▲▲▲ 본문 끝 ▲▲▲ -->
```

### 이미지 추가/교체

`images/` 폴더에 파일을 올린 뒤, 본문에서 이렇게 넣습니다.

```html
<figure class="image"><img src="images/파일명.jpg" alt=""></figure>
```

### 색상·여백 변경

`assets/style.css` 맨 위 `:root` 부분의 색상 값을 바꾸면 전체에 반영됩니다.

## 참고

- 이미지는 모두 저장소 안에 있어 외부 서비스(노션 등)에 의존하지 않습니다.
- `index.html`은 브라우저로 그냥 열어도 동작합니다. (인터넷 없이도 확인 가능)
