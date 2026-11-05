# Хост WebGL-билда на GitHub Pages

Этот публичный репозиторий только раздаёт WebGL-билд Unity: **https://ocavit.github.io/unity-webgl-ci-pages/**

- Билд собирает пайплайн GitHub Actions (`.github/workflows/buildPipeline.yaml`) в приватном репозитории `OCAVIT/unity-webgl-ci`
  при каждом пуше в его ветку `build`.
- Готовые файлы пайплайн пушит в **корень ветки `gh-pages`** этого репозитория по SSH-ключу. Публичный ключ добавлен
  в Settings → Deploy keys с правом записи, приватный хранится в секрете `PAGES_DEPLOY_KEY` приватного репозитория.
- GitHub Pages: Settings → Pages → Deploy from a branch → `gh-pages`, папка `/ (root)`. Сайт обновляется после каждого пуша в ветку.
