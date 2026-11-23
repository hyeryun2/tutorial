# 영상 자막 기본 스타일 (사용자 지정 — 항상 이 설정 사용)

세로 쇼츠(1080×1920) 영상에 자막을 넣을 때는 별도 요청이 없는 한 아래 설정을 기본으로 사용한다.

- 위치: 화면 하단 중앙, 아래에서 약 620px 위 (포스터 제목 로고 바로 위). 모든 줄을 같은 높이로 통일.
  - ffmpeg/libass: `Alignment=2, MarginV=93` (PlayResY 288 기준)
- 폰트: Playfair Display Bold (`remarried_empress_shorts/font/PlayfairDisplay.ttf`)
  - ffmpeg/libass: `FontName=Playfair Display, Bold=1, FontSize=13, Spacing=0.3`
- 글자색: 연한 금색 #F3E3B5 (`PrimaryColour=&H00B5E3F3`)
- 배경: 반투명 검정 박스, 불투명도 약 55% (`BorderStyle=3, OutlineColour=&H8C000000, Outline=1.6, Shadow=0`)
- 캡컷: 텍스트 → 배경 검정 불투명도 50~60%, 자막 전체를 로고 위 높이로 일괄 이동

전체 force_style 예시:

```
FontName=Playfair Display,Bold=1,FontSize=13,PrimaryColour=&H00B5E3F3,OutlineColour=&H8C000000,BackColour=&HFF000000,BorderStyle=3,Outline=1.6,Shadow=0,Spacing=0.3,Alignment=2,MarginV=93
```
