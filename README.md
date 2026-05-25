# 내 가방에 내가 없다 — 홍보 사이트

8인의 여성 작가 에세이 《내 가방에 내가 없다》(작가의 집)의 공식 홍보 페이지입니다.
별도 빌드가 필요 없는 **정적 사이트**라, 파일을 올리기만 하면 끝입니다.

## 파일 구성
- `index.html` — 사이트 본체 (표지 이미지는 파일 안에 내장되어 있음)
- `cover.jpg` — 링크 공유 시 미리보기(썸네일)에 쓰이는 표지 이미지
- `vercel.json` — Vercel 설정 (그대로 두세요)
- `.gitignore`

---

## 방법 A. GitHub + Vercel (요청하신 방식)

### 1) GitHub에 저장소 만들기
1. https://github.com 로그인 → 우측 상단 **+** → **New repository**
2. 이름 입력(예: `bag-book`) → **Public** 선택 → **Create repository**
3. 만든 저장소 화면에서 **Add file → Upload files** 클릭
4. 이 폴더의 파일 전부(`index.html`, `cover.jpg`, `vercel.json`, `.gitignore`)를 끌어다 놓기 → **Commit changes**

### 2) Vercel에 연결하기
1. https://vercel.com 접속 → **Continue with GitHub** 로 가입/로그인
2. **Add New… → Project**
3. 방금 만든 GitHub 저장소 옆 **Import** 클릭
4. 설정은 건드릴 필요 없이(Framework: Other 자동 인식) **Deploy** 클릭
5. 잠시 뒤 `https://bag-book.vercel.app` 같은 주소가 생성됩니다. 끝!

이후 GitHub 저장소의 파일을 수정하면 Vercel이 자동으로 다시 배포합니다.

---

## 방법 B. GitHub 없이 Vercel에 바로 올리기 (가장 빠름)
1. https://vercel.com 로그인
2. **Add New… → Project → Deploy** 화면에서 이 폴더를 통째로 드래그&드롭
3. 끝. (단, 이 방식은 자동 업데이트 연동이 없습니다.)

> 더 간단하게는 https://app.netlify.com/drop 에 이 폴더를 끌어다 놓아도 즉시 주소가 생깁니다.

---

## 배포 후 한 가지 (선택) — 공유 썸네일 정확히 띄우기
카카오톡·인스타 등에 링크를 공유할 때 표지가 안정적으로 보이게 하려면,
배포된 실제 주소를 알게 된 뒤 `index.html` 상단의 주석 두 줄을 이렇게 바꾸세요.

```html
<!-- 아래 두 줄의 주석(<!-- -->)을 풀고 [내사이트주소]를 실제 주소로 교체 -->
<meta property="og:image" content="https://내주소.vercel.app/cover.jpg">
<meta property="og:url" content="https://내주소.vercel.app">
```

선택 사항이며, 안 해도 사이트와 영상은 정상 작동합니다.

---

## 검색 노출(선택)
- 구글: https://search.google.com/search-console 에서 사이트 등록
- 네이버: https://searchadvisor.naver.com 에서 사이트 등록
  (등록 시 받은 인증 코드는 `index.html` 상단의 해당 주석 줄에 넣으면 됩니다.)
