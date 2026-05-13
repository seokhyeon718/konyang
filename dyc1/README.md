# 제1회 한·일 불교문화 축제 홈페이지

GitHub Pages로 호스팅되는 정적 홈페이지입니다.

## 📁 폴더 구조

```
/
├── index.html          ← 메인 홈페이지 (수정 불필요)
├── data/
│   ├── notices.json    ← 공지사항 데이터
│   ├── schedule.json   ← 일정 데이터
│   └── gallery.json    ← 갤러리 파일 목록
└── gallery/
    └── 2026/           ← 사진 파일 업로드 폴더
        └── (여기에 jpg/png/webp 파일 업로드)
```

## ✏️ 콘텐츠 수정 방법

### 공지사항 추가 (`data/notices.json`)
```json
{
  "intro": "상단 안내 문구",
  "items": [
    {
      "badge": "NEW",
      "badgeType": "badge-new",
      "title": "공지 제목",
      "date": "2026.06.20",
      "content": "자세한 내용 (선택사항)"
    }
  ]
}
```
- `badgeType`: `badge-new`(초록) / `badge-warn`(주황) / `badge-info`(파랑)

### 일정 수정 (`data/schedule.json`)
```json
{
  "status": "tba",
  "events": [
    {
      "type": "MAIN EVENT",
      "name": "EDM 축제 & 드론쇼",
      "time": "18:00 ~ 21:00",
      "color": "teal"
    }
  ]
}
```
- `status`: `"tba"` → 준비중 표시, `"confirmed"` → 바로 일정 표시
- `color`: `teal` / `gold` / `light` / `warm`

### 갤러리 사진 추가 (`data/gallery.json` + 파일 업로드)

1. `gallery/2026/` 폴더에 사진 파일 업로드 (jpg, png, webp)
2. `data/gallery.json` 수정:

```json
{
  "albums": [
    {
      "id": "2026",
      "title": "2026 제1회 한·일 불교문화 축제",
      "folder": "gallery/2026",
      "images": [
        "photo01.jpg",
        "photo02.jpg",
        { "src": "photo03.jpg", "caption": "스탬프투어 현장" }
      ]
    }
  ]
}
```

## 🚀 GitHub Pages 배포

1. GitHub 저장소 생성 (또는 기존 저장소 사용)
2. 이 폴더의 모든 파일 업로드
3. Settings → Pages → Source: `main` branch, `/ (root)` 선택
4. 저장하면 `https://username.github.io/repo-name/` 으로 접속 가능

## 🔑 관리자 패널

우측 하단 🔧 버튼 → 비밀번호 `2022` → 각 JSON 파일 수정 안내 확인
