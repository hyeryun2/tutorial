# 영상 자막 규칙 (사용자 지정)

## 항상 고정: 자막 위치
세로 쇼츠(1080×1920)에서는 별도 요청이 없는 한 자막 위치를 항상 아래처럼 둔다.

- 화면 하단 중앙, 아래에서 약 620px 위(포스터 제목 로고 바로 위). 모든 줄을 같은 높이로 통일한다.
  - ffmpeg/libass: `Alignment=2, MarginV=93` (PlayResY 288 기준)
- 글자 뒤에는 너무 진하지 않은 반투명 배경을 깔아 어떤 장면에서도 읽히게 한다.

## 영상마다 다르게: 폰트·색·스타일
폰트, 글자색, 배경색은 고정하지 않는다. 영상의 장르와 분위기(포스터 색감, 로고 서체 등)에 맞게 그때그때 고른다.
- 예: 로맨스 판타지·궁정물은 세리프체에 금색, 스릴러는 날카로운 고딕체에 흰색이나 빨강, 코미디는 둥근 굵은 글씨.
- 정하기 애매하면 후보를 짧게 제안하고 사용자에게 고르게 한다.

### 참고 예시: 「재혼황후」 (로맨스 판타지)
```
FontName=Playfair Display,Bold=1,FontSize=13,PrimaryColour=&H00B5E3F3,OutlineColour=&H8C000000,BackColour=&HFF000000,BorderStyle=3,Outline=1.6,Shadow=0,Spacing=0.3,Alignment=2,MarginV=93
```
- 폰트: Playfair Display Bold (`remarried_empress_shorts/font/PlayfairDisplay.ttf`)
- 글자색: 연한 금색 #F3E3B5
- 배경: 반투명 검정 박스, 불투명도 약 55%
