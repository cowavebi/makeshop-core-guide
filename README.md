# 메이크샵 코어 가이드

메이크샵 코어(CORE) 고객 안내 매뉴얼입니다. 노션에서 이전했습니다.

## 폴더 구조

```
.
├── index.html          ← INDEX : 매뉴얼 전체 목록
├── assets/
│   ├── style.css       ← 공통 디자인 (색상·여백)
│   └── cover.png       ← 상단 배너
└── pg/
    ├── index.html      ← PG(전자결제) 신청 가이드
    └── images/         ← 가이드 화면 캡처 16장
```

## 웹에 공개하기 (GitHub Pages)

1. 저장소 **Settings** → 왼쪽 메뉴 **Pages**
2. Source 를 **Deploy from a branch** 로 선택
3. Branch 는 **main**, 폴더는 **/ (root)** 선택 후 **Save**
4. 1~2분 뒤 주소가 생성됩니다 → `https://<계정명>.github.io/<저장소명>/`

> 저장소가 **비공개(Private)** 면 Pages 도 열리지 않습니다. 고객에게 전달할 문서이므로 **공개(Public)** 로 두어야 합니다.

## 내용 수정하기

GitHub 웹에서 바로 고칠 수 있습니다.

1. 수정할 파일 선택 (예: `pg/index.html`)
2. 오른쪽 위 **연필 아이콘(Edit this file)** 클릭
3. 글자를 고친 뒤 아래 **Commit changes** 클릭
4. 1~2분 뒤 사이트에 반영됩니다

### 자주 하는 수정

| 하고 싶은 것 | 고칠 파일 | 찾을 부분 |
|---|---|---|
| 가이드 내용 수정 | `pg/index.html` | `<!-- ▼▼▼ 본문 시작 ▼▼▼ -->` 아래 |
| 매뉴얼 목록에 새 가이드 추가 | `index.html` | `<!-- ▼▼▼ 매뉴얼 목록 ▼▼▼ -->` 아래 |
| 색상·여백 변경 | `assets/style.css` | 맨 위 `:root` |

### 이미지 추가

`pg/images/` 폴더에 파일을 올린 뒤, HTML 에서 이렇게 넣습니다.

```html
<figure class="image"><img src="images/파일명.jpg" alt=""></figure>
```

### 새 가이드 추가

1. `pg` 폴더를 복사해 새 이름으로 만듭니다 (예: `design`)
2. 그 안의 `index.html` 내용을 새 가이드로 고칩니다
3. 최상위 `index.html` 의 목록에 카드 한 칸을 추가합니다

```html
<a class="card" href="design/">
  <h2>🎨 디자인 설정 가이드</h2>
  <p>스킨 선택과 메인 화면 구성 방법</p>
</a>
```

## 참고

- 이미지는 모두 저장소 안에 있어 외부 서비스에 의존하지 않습니다.
- `index.html` 파일은 브라우저로 그냥 열어도 동작합니다. (인터넷 없이 확인 가능)
