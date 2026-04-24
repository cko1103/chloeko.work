# Chloe Ko — Portfolio Site

GitHub Pages로 무료 운영하는 포트폴리오 사이트입니다.

---

## 파일 구조

```
portfolio/
├── index.html        ← ShowReel (메인)
├── work.html         ← Work 갤러리
├── about.html        ← About
├── resume.html       ← Resume
├── drawings.html     ← Drawings
├── style.css         ← 공용 스타일
├── work/             ← 개별 프로젝트 상세 페이지
│   └── vanessa-hair-vibeswap.html (예시)
├── images/
│   ├── work/         ← Work 썸네일 이미지
│   ├── about/        ← 프로필 사진
│   └── drawings/     ← 드로잉 이미지
└── files/
    └── chloe-ko-resume.pdf
```

---

## 수정해야 할 것들

### 1. 비디오 임베드 (index.html)
Vimeo 또는 YouTube 임베드 URL을 교체하세요:
```html
<!-- ShowReel -->
src="https://player.vimeo.com/video/YOUR_VIMEO_ID"

<!-- Cycle thesis film -->
src="https://player.vimeo.com/video/YOUR_CYCLE_VIDEO_ID"
```

### 2. 이미지 (work.html)
각 work item의 이미지를 `images/work/` 폴더에 넣고,
파일명을 맞춰주세요 (예: `vanessa-hair-vibeswap.jpg`)

### 3. 프로필 사진 (about.html)
`images/about/profile.jpg` 경로에 사진을 넣으세요.

### 4. 이메일 주소
`about.html`과 `resume.html`의 `hello@chloeko.com`을 실제 이메일로 교체하세요.

### 5. Resume PDF (resume.html)
`files/chloe-ko-resume.pdf` 경로에 PDF를 넣으세요.

### 6. Drawings (drawings.html)
이미지를 `images/drawings/`에 넣고, HTML에 아이템을 추가하세요:
```html
<div class="drawing-item" data-src="images/drawings/drawing-01.jpg">
  <img src="images/drawings/drawing-01.jpg" alt="" loading="lazy">
</div>
```

---

## GitHub Pages 배포

1. GitHub에서 새 레포 생성 (예: `cko1103.github.io` 또는 `portfolio`)
2. 이 파일들을 전부 업로드
3. Settings → Pages → Source: `main` branch, `/ (root)` → Save
4. 몇 분 후 `https://cko1103.github.io/` 또는 `https://cko1103.github.io/portfolio/` 에서 확인

---

## 커스텀 도메인 연결

1. Namecheap / Cloudflare 등에서 도메인 구매 (예: `chloeko.com`) — 약 $12/년
2. 레포 루트에 `CNAME` 파일 생성:
   ```
   chloeko.com
   ```
3. DNS 설정에서 A 레코드 4개 추가:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
4. GitHub Settings → Pages → Custom domain에 도메인 입력
5. "Enforce HTTPS" 체크

---

## 개별 프로젝트 페이지 추가 (work/ 폴더)

각 프로젝트마다 `work/프로젝트명.html` 파일을 만들어서
`work.html`의 각 `<a href="">` 링크에 연결하면 됩니다.
원하시면 템플릿 만들어드릴게요!
