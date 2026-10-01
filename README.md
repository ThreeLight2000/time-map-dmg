# TimeMap.dmg — historical web portfolio

TimeMap.dmg is a personal portfolio website built with Next.js, not a disk image or downloadable desktop app. The source describes it as a way to map personal activities and work over time.

- **Portfolio:** [time-map-dmg.vercel.app](https://time-map-dmg.vercel.app)
- **Demo video:** [Watch the original demo](https://www.youtube.com/embed/EE_m0jAGuVw?si=QPYPn-oT5OfFWJzz)

[![TimeMap.dmg demo](https://i.imgur.com/t7xuFP1.png)](https://www.youtube.com/embed/EE_m0jAGuVw?si=QPYPn-oT5OfFWJzz)
- **Project description and stack:** [src/data/timemap-dmg.md](src/data/timemap-dmg.md)
- **Activity page and API:** [activity page](src/app/%28info%29/activities/page.tsx) · [activities endpoint](src/app/api/v1/info/activities/route.ts)

## Run locally

This historical source uses Yarn (`yarn.lock`) and defines `dev` and `build` scripts in [`package.json`](package.json):

```bash
yarn install
yarn dev
# Optional production build
yarn build
```

The audited source has not had a fresh dependency install or build verification. Local development may still read deployed data: [`src/constants/urls.ts`](src/constants/urls.ts) points `API_URL` at the Vercel API, and the [activities page](src/app/%28info%29/activities/page.tsx) requests data from that endpoint.

The update log below records changes from December 2023 through January 2024. It is historical project context, not a current maintenance statement. The repository has no test script; available commands are listed in [package.json](package.json).

## TimeMap.dmg UPDATE

### 24/1/15

- 마크다운 파일을 받아 프로젝트 상세 페이지로 적용

### 23/12/17

- 시작페이지 변경

### 23/12/11

- 반응형 헤더 설정
- 활동내역 박스 클릭 시 url 이동하도록 변경

### 23/12/10

- 홈페이지 애니메이션 추가
- 홈페이지 불필요 요소 제거
- 모바일에서 애니메이션 전체 범위 커버하기
- 홈페이지 모바일 레이아웃 적용

### 23/12/09

- 최초 Release
- 글자 색상 미지정 시 시스템 모드에 따라 색상 변경되는 오류 해결
- 이미지 가공 후 교체, 불필요 속성 제거

---

### 나중에 추가해보면 좋을 것

- Tailwind Typegraphy: 마크다운 형식의 글을 자동 스타일링해줌
