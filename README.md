# Hackathon_Oct_HinakoTerado

古橋研究室 2026年10月ハッカソンの成果リポジトリです。
ウォーキング記録アプリ（Fotoshi・YAMAP）の使用レポートと、Claude CodeによるGitHub操作の試行をまとめています。

- 関連記事（Medium）：[青キャンからさがキャンへ 45kmの道のりを記録（途中まで）](https://medium.com/furuhashilab/%E9%9D%92%E3%82%AD%E3%83%A3%E3%83%B3%E3%81%8B%E3%82%89%E3%81%95%E3%81%8C%E3%82%AD%E3%83%A3%E3%83%B3%E3%81%B8-45km%E3%81%AE%E9%81%93%E3%81%AE%E3%82%8A%E3%82%92%E8%A8%98%E9%8C%B2-%E9%80%94%E4%B8%AD%E3%81%BE%E3%81%A7-5c7ff021ba83)
- 元になったIssue：[#1](../../issues/1) / [#2](../../issues/2) / [#3](../../issues/3)

---

## 1. Introduction（はじめに）

### 背景
- 青山キャンパスから相模原キャンパスまでの約45kmを歩くNight Walkを行い、その道のりを記録した（途中まで）
- ウォーキング中の記録には、写真・位置情報を扱えるスマホアプリが使える
- また、生成AIツール（Claude Code）を使うと、GitHubの操作を対話的に行える

### 目的
- 位置情報付き写真を投稿できるアプリ **Fotoshi** を実際のウォーキングで使い、使い勝手と課題を明らかにする
- 登山・ウォーキング記録アプリ **YAMAP** と比べて、Fotoshiの特徴を整理する
- **Claude Code** をPowerShellから使い、GitHubのリポジトリ操作ができるかを試す

---

## 2. Methods（方法）

### 2.1 Fotoshi（[#2](../../issues/2)）
- Night Walk中に休憩所を撮影し、Fotoshiに投稿した
- スマホでWi-Fiのテザリングをしながら使用した

### 2.2 YAMAP（[#3](../../issues/3)）
- 以前から使ったことのあるYAMAPを、今回のウォーキングでも使用した
- 地図表示、記録機能、写真のリプレイ機能を確認した

### 2.3 Claude Code（[#1](../../issues/1)）
- PowerShellでClaude Codeを起動した
- GitHubのトークンを作成し、Claude CodeにGitHubを操作する権限を与える設定を行った
- furuhashilab Organizationのリポジトリ調査と、リポジトリの作成を依頼した

---

## 3. Results（結果）

### 3.1 Fotoshi

| 観点 | 結果 |
|---|---|
| 地図表示 | 使用したスマホが原因か、使用中にマップが表示されなかった |
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
- 受け答えはかなり速かった
- 約20秒でfuruhashilab Organizationのリポジトリを調べてくれた
- 本リポジトリの作成もClaude Codeから行えた

<img width="450" alt="furuhashilab Organizationを調べた結果" src="https://github.com/user-attachments/assets/7f1247cb-5d4b-4f7b-bd39-71bdde3d1239" />

<img width="450" alt="リポジトリ作成の結果" src="https://github.com/user-attachments/assets/243ffd26-2572-4461-ada5-d32738b077c5" />

---

## 4. Discussion（考察）

### 4.1 FotoshiとYAMAPの比較

| 観点 | Fotoshi | YAMAP |
|---|---|---|
| 地図表示 | 表示されないことがあった | 常に表示される |
| 通信がない環境 | その場でアップロードできなかった | 機内モードでも記録できる |
| 写真の活用 | ポイント制、場所・日付で区別 | 位置情報をもとにリプレイ動画を作成 |

- Fotoshiで困った点（地図が出ない、通信がないと使えない）は、YAMAPでは強みになっていた
- 長距離のウォーキングでは、オフラインでも使えることやバッテリー消費が重要だと分かった

### 4.2 Fotoshiへの改善提案
- 写真アプリ（Photo）から後でアップロードできる機能があるとよい。通信やバッテリーの問題で撮れなかった写真を後から補える
- ユーザー間のポイントランキングを表示すると、もっと写真を撮りたくなる動機づけになりそう

### 4.3 Claude Codeについて
- トークンのセキュリティを改めて確認した
  - トークンをAIに渡さない
  - メモ帳にメモしておく
  - 有効期限を決める
- トークンの消費量が気になった。どのように消費を抑えるか、どのくらいの作業でどれだけ減るのかを学び始めた
- 使うのが楽しみになってきた

### 4.4 今後の課題
- Fotoshiについて改めて調べる
- Fotoshiで撮った写真がOSMにどのように反映されるのかを確認する
- ChatGPTでも同じことができるのか、PowerShellで試してみる

---

## License

このリポジトリは [CC BY 4.0](LICENSE) で公開しています。
