# Hackathon_Oct_HinakoTerado

古橋研究室 2026年10月ゼミ内ハッカソン（FOSS4G Hiroshima / SotM Asia OSAKA 振り返りハッカソン）の成果リポジトリです。
先生に紹介していただいた写真共有アプリ **Fotoshi** を実際に試用したレポートと、**Claude Code** によるGitHub操作の試行をまとめています。

- 関連記事（Medium）：[青キャンからさがキャンへ 45kmの道のりを記録（途中まで）](https://medium.com/furuhashilab/%E9%9D%92%E3%82%AD%E3%83%A3%E3%83%B3%E3%81%8B%E3%82%89%E3%81%95%E3%81%8C%E3%82%AD%E3%83%A3%E3%83%B3%E3%81%B8-45km%E3%81%AE%E9%81%93%E3%81%AE%E3%82%8A%E3%82%92%E8%A8%98%E9%8C%B2-%E9%80%94%E4%B8%AD%E3%81%BE%E3%81%A7-5c7ff021ba83)
- 元になったIssue：[#1](../../issues/1) / [#2](../../issues/2) / [#3](../../issues/3)
- [Nigh Wlak map](https://usakooon.github.io/night-walk-photomap/)も作りました。

---

## 1. Introduction（はじめに）

### 1.1 背景
- 今回のゼミ内ハッカソンのテーマは「FOSS4G Hiroshima / SotM Asia OSAKA 振り返りハッカソン」
- 国際会議での新たな知見というよりは、先生が紹介していた写真共有アプリ「Fotoshi」を題材に選んだ
  - Fotoshiは Android ユーザー向けにβテストユーザーを募集中だった
  - 自分がAndroidユーザーで都合がよかった

### 1.2 Fotoshiとは
Fotoshiは、写真を使って現地の情報を集め、OpenStreetMap（OSM）などの地理空間データの作成・更新に役立てるためのツール・プラットフォームである。

- **ジオタグの活用**：写真のExifデータ（GPSの緯度・経度、撮影方向など）を解析し、地図上の正確な位置に写真を配置する
- **現地データの裏付け（グラウンドトゥルース）**：衛星画像や遠隔調査では確認しにくい、店舗名・営業時間・バリアフリー情報・道路標識・建物の入口などを写真で記録する
- **地図エディタとの連携**：整理した写真をJOSMやiDエディタに参照データとして読み込み、正確で効率的なマッピングを支援する

### 1.3 目的
- Fotoshiを実際の屋外での移動中に使い、使い勝手と課題を明らかにする
- 普段使っている **YAMAP** と比べて、Fotoshiの特徴を整理する
- **Claude Code** をPowerShellから使い、GitHubの操作ができるかを試す

---

## 2. Methods（方法）

### 2.1 Fotoshi（[#2](../../issues/2)）
- 使用端末：Galaxy A30（以前使っていたスマホ。普段使いのGoogle Pixel 10は避けた）
- 長距離ウォーキング（青山キャンパス→相模原キャンパス）の途中で、休憩所を撮影してFotoshiに投稿した
- Wi-Fiのテザリングをしながら使用した

### 2.2 YAMAP（[#3](../../issues/3)）
- 以前から使っているYAMAPも同じウォーキングで使用した
- 地図表示、記録機能、写真のリプレイ機能を確認した

### 2.3 Claude Code（[#1](../../issues/1)）
- PowerShellでClaude Codeを起動した
- GitHubの個人トークンを作成し、Claude CodeにGitHubを操作する権限を与える設定を行った
- furuhashilab Organizationのリポジトリ調査と、リポジトリの作成を依頼した

---

## 3. Results（結果）

### 3.1 Fotoshi

| 観点 | 結果 |
|---|---|
| 地図表示 | 使用したスマホが原因か、使用中にマップが表示されなかった |
| 機内モード | 機内モードではマップが表示されなかった |
| アップロード | テザリングしていたが、その場でアップロードできず「保留」のままだった |
| バッテリー | 途中で充電が切れ、普通のカメラでの撮影に切り替えた |
| ポイント制 | 撮影でポイントがもらえるのが少しうれしかった |
| 記録の精度 | 場所と日付が正確に区別されていた |

<img width="300" alt="Fotoshiでの撮影成果" src="https://github.com/user-attachments/assets/0e87f270-b09a-493b-b078-a4d419d31740" /> <img width="300" alt="ウォーキング中にマップが表示されない画面" src="https://github.com/user-attachments/assets/9c457d5b-8cda-4363-b7aa-96a721b372c4" />

*左：撮影成果　右：ウォーキング中、マップが表示されなかった画面*

### 3.2 YAMAP
- 機内モードでも記録ができた
- 地図が常に表示されていた
- ウォーキング中に撮った写真を、位置情報をもとに最後にリプレイ動画で表示してくれた

<img width="300" alt="YAMAPの画面" src="https://github.com/user-attachments/assets/159b84b6-aa95-4dba-865b-7d9f5701f5df" />

### 3.3 Claude Code
- Claude CodeにGitHubを操作する権限を付与する設定を完了した（個人的に大きな収穫）
- 受け答えはかなり速かった
- 約20秒でfuruhashilab Organizationのリポジトリを調べてくれた
- 本リポジトリの作成もClaude Codeから行えた
- Claude Codeが付けた謎の呼び名「ハッシーさん」について、後でClaude Codeから謝罪があった

<img width="450" alt="furuhashilab Organizationを調べた結果" src="https://github.com/user-attachments/assets/7f1247cb-5d4b-4f7b-bd39-71bdde3d1239" />

<img width="450" alt="リポジトリ作成の結果" src="https://github.com/user-attachments/assets/243ffd26-2572-4461-ada5-d32738b077c5" />

---

## 4. Discussion（考察）

### 4.1 FotoshiとYAMAPの比較

| 観点 | Fotoshi | YAMAP |
|---|---|---|
| 地図表示 | 表示されないことがあった | 常に表示される |
| 機内モード | マップが表示されない | 記録できる |
| 通信が不安定な環境 | その場でアップロードできなかった | 記録を続けられる |
| 写真の活用 | ポイント制、場所・日付で区別 | 位置情報をもとにリプレイ動画を作成 |

- Fotoshiで困った点（地図が出ない、通信がないと使えない）は、YAMAPでは強みになっていた
- 長時間の屋外利用では、充電の減りを抑えるために機内モードを使う。オフラインでも使えることとバッテリー消費の少なさが重要である

### 4.2 Fotoshiへの改善提案
- 写真アプリ（Photo）から後でアップロードできる機能があるとよい。通信やバッテリーの問題で投稿できなかった写真を後から補える
- 機内モードでもマップが表示されるとありがたい
- ユーザー間のポイントランキングを表示すると、もっと写真を撮りたくなる動機づけになりそう

### 4.3 Claude Codeについて
- 個人トークンのセキュリティを改めて確認した
  - トークンをAIに渡さない
  - メモ帳にメモしておく
  - 有効期限を決める
- トークンの消費量が気になった。どのように消費を抑えるか、どのくらいの作業でどれだけ減るのかを学び始めた
- 使うのが楽しみになってきた

### 4.4 今後の課題
- Fotoshiで撮った写真がOSMにどのように反映されるのかを確認する
- ChatGPTでも同じことができるのか、PowerShellで試してみる

---

## License

このリポジトリは [CC BY 4.0](LICENSE) で公開しています。
