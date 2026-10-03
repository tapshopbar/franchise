# 탭샵바 가맹 안내 랜딩페이지

주소: https://franchise.tsb.wine (GitHub Pages)

## 구성

| 파일 | 내용 |
|---|---|
| `index.html` | 랜딩페이지 전체 (HTML, CSS, JS 한 파일) |
| `assets/img/` | 매장·교육 사진 (웹용으로 줄인 파일) |
| `assets/wordmark-white.png` | 상단·하단 로고 (BI 가로형 워드마크, 흰색) |
| `assets/favicon.png` | 브라우저 탭 아이콘 (TSB 심볼) |
| `assets/tsb-franchise-brochure.pdf` | 상담 신청 후 다운로드되는 가맹 안내서 |
| `CNAME` | 커스텀 도메인 (franchise.tsb.wine) |

## 상담 신청 폼

- 페이지 안의 폼은 Google Form "탭샵바 가맹 상담 신청"으로 전송됩니다 (hello@tsb.wine 소유).
- 응답은 Drive `02_Projects` 폴더의 "탭샵바 가맹 상담 신청 (응답)" 시트에 쌓입니다.
- 신청이 들어오면 Apps Script "탭샵바 가맹상담 폼"이 hello@tsb.wine 으로 알림 메일을 보냅니다.
- Google Form 질문을 바꾸면 `index.html` 의 `entry.숫자` 이름도 맞춰야 합니다.

## 자주 하는 수정

- **브로셔 교체:** `assets/tsb-franchise-brochure.pdf` 를 같은 이름으로 새 파일 업로드
- **문구 수정:** `index.html` 에서 해당 문장 검색 후 수정
- 저장(Commit)하면 1~2분 뒤 사이트에 반영됩니다.

## 도메인 (DNS)

tsb.wine DNS는 AWS Route 53에서 관리합니다. 아래 레코드가 필요합니다.

| 이름 | 유형 | 값 |
|---|---|---|
| `franchise.tsb.wine` | CNAME | `tapshopbar.github.io` |
