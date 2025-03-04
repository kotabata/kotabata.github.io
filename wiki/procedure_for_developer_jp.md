# プロジェクト構築手順

## 1. プロジェクトの初期化

```bash
# Viteを使用してReact+TypeScriptプロジェクトを作成
npm create vite@latest academic-website -- --template react-ts

# プロジェクトディレクトリに移動
cd academic-website

# 必要な依存関係をインストール
npm install i18next i18next-browser-languagedetector i18next-http-backend react-i18next markdown-to-jsx
npm install -D tailwindcss postcss autoprefixer papaparse gh-pages @types/node
```

## 2. Tailwind CSSのセットアップ

```bash
# Tailwind CSSの初期化
npx tailwindcss init -p
```

## 3. ディレクトリ構造の作成

```bash
# 必要なディレクトリを作成
mkdir -p src/{components,hooks,types,utils}
mkdir -p public/{api,images,locales/{en,ja},content/{bio,awards,career}}
mkdir -p data
mkdir -p scripts
mkdir -p .github/workflows
```

## 4. CSVデータファイルの配置

```bash
# データディレクトリにCSVファイルを配置
cp path/to/rm_published_papers.csv data/
cp path/to/rm_presentations.csv data/
```

## 5. API生成スクリプトの設定

```bash
# API生成スクリプトを配置
cp path/to/generatePublicApi.js scripts/
```

## 6. 各ファイルの作成

```bash
# 生成したコードファイルを適切な場所に配置
```

## 7. 必要な画像の準備

```bash
# プロフィール画像と研究室のロゴ画像を配置
cp path/to/profile-image.jpg public/images/profile.jpg
cp path/to/lab-logo.png public/images/lab-logo.png
```

## 8. コンテンツファイルの作成

```bash
# 各種JSONデータファイルを作成
touch public/content/awards/awards_en.json
touch public/content/awards/awards_ja.json
touch public/content/awards/grants_en.json
touch public/content/awards/grants_ja.json
touch public/content/awards/projects_en.json
touch public/content/awards/projects_ja.json
touch public/content/career/career_en.json
touch public/content/career/career_ja.json
```

## 9. APIの生成

```bash
# CSVからAPIを生成
npm run generate-api
```

## 10. 開発サーバーの起動

```bash
# 開発サーバーを起動
npm run dev
```

## 11. GitHubリポジトリの設定

```bash
# Gitリポジトリを初期化
git init
git add .
git commit -m "Initial commit"

# GitHubリポジトリを作成し、リモートとして追加
git remote add origin https://github.com/yourusername/academic-website.git
git push -u origin main
```

## 12. GitHub Pagesへのデプロイ

```bash
# ウェブサイトをビルドしてデプロイ
npm run deploy
```

あるいは、GitHub Actionsを使った自動デプロイを設定します。リポジトリにプッシュすると自動的にデプロイされます。

## 13. カスタマイズ

- `public/locales/` 内の翻訳ファイルを編集して個人情報を更新
- `public/content/bio/` 内のマークダウンファイルでバイオを更新
- `data/` 内のCSVファイルで論文や発表データを更新
- `tailwind.config.js` でテーマカラーをカスタマイズ
