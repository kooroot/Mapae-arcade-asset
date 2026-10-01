# Mapae Arcade assets

Mapae Arcade에서 사용하는 이미지 107개를 메인 [Mapae 저장소](https://github.com/kooroot/Mapae)와 분리해 관리합니다. 이미지 경로는 `arcade/` 아래에서 `apps/web/public/arcade/`의 경로와 같습니다.

메인 저장소를 빌드하거나 배포하기 전에 에셋을 복사하세요. 예를 들어 두 저장소가 같은 상위 디렉터리에 있다면:

```bash
cd Mapae-arcade-asset
shasum -a 256 -c SHA256SUMS
mkdir -p ../Mapae/apps/web/public/arcade
rsync -a arcade/ ../Mapae/apps/web/public/arcade/
test -f ../Mapae/apps/web/public/arcade/lobby-scene.webp
```

업데이트할 때는 이 저장소에서 `git pull --ff-only origin main`을 실행한 다음 검증과 복사를 반복합니다. `.git` 디렉터리를 웹의 `public/` 아래로 복사하지 마세요.
