# 안전한 등굣길 지도 (GitHub Pages)

이 저장소는 설문 응답으로부터 추출한 지명 후보를 Leaflet + OpenStreetMap + Nominatim으로 지오코딩하여
언급 빈도에 비례하는 원(크기/진하기)으로 표시합니다. **API 키가 필요하지 않습니다.**
그대로 GitHub Pages에 올리면 작동합니다.

## 배포 방법 (GitHub Pages)
1. 이 폴더의 모든 파일을 새 GitHub 저장소에 업로드합니다.
2. `Settings > Pages`에서 **Source: Deploy from a branch** 선택 → `main` 브랜치와 `/ (root)` 경로 지정 → Save.
3. 약간의 빌드 대기 후 Pages URL이 발급됩니다. Gabia에서 해당 URL로 CNAME 연결을 설정하세요.

## 좌표 보정(선택)
- `index.html`의 `manualCoords` 객체에 특정 지점의 확정 좌표를 넣으면 지오코딩을 우회하고 그 좌표로 표시합니다.

## 지역 힌트 변경(선택)
- `REGION_HINT`를 귀교/지역 이름으로 변경하면 지오코딩 정확도가 올라갑니다.

## 공개 API 유의사항
- 브라우저가 Nominatim에 직접 요청합니다. 요청량이 많을 경우 자동으로 딜레이(250ms)를 둡니다.
