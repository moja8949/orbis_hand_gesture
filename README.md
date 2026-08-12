# Hand Particle Sphere

노트북 웹캠으로 손을 인식해 Three.js 파티클 구체를 조작하는 1-file 데모입니다.

## 실행

### 가장 쉬운 방법: VS Code Live Server
1. VS Code에서 이 폴더를 엽니다.
2. `index.html`을 엽니다.
3. Live Server 확장 프로그램으로 `Open with Live Server`를 실행합니다.
4. 브라우저에서 카메라 권한을 허용합니다.

### 또는 터미널
```bash
npx serve .
```
그 다음 표시되는 localhost 주소를 엽니다.

## 인터랙션
- 손을 좌우/상하로 이동: 구체가 따라 이동
- 주먹을 쥠: 파티클이 작은 구로 응집
- 손바닥을 펼침: 구가 커지고 파티클이 유기적으로 확산
- 손의 방향: 구체의 기울기/회전에 반영
- `D`: 우측 하단 카메라 디버그 미리보기 토글

## 감도 조절
`index.html` 상단의 아래 값을 조절하세요.

```js
const OPENNESS_MIN = 0.86;
const OPENNESS_MAX = 1.58;
```

주먹을 쥐었는데도 구가 너무 크면 `OPENNESS_MIN`을 조금 올리고,
손바닥을 펴도 충분히 커지지 않으면 `OPENNESS_MAX`를 조금 낮추면 됩니다.
