# ラムサウンディング柱状図

ラムサウンディング試験の結果（深度・打撃回数・貫入量・トルク）を入力し、修正Nd値の表とグラフを柱状図として DXF に出力するブラウザアプリ。

## 機能

- 画面での直接入力、Excel 範囲の貼り付け、.xlsx／.xls／.csv（Shift_JIS 可）の読込
- 修正Nd = Ndm − 0.04Mv（係数は変更可、Mv 空欄は 0）、貫入量 200mm 以外は Ndm = 打撃回数 × 200 ／ 貫入量 に換算
- 換算N値（係数 × 修正Nd、係数は利用者が設定）
- 出力形式
  - 簡易柱状図（断面図貼付用）：1 図面単位 = 1m、土質柱状（模様は土質名から自動判定または手動選択）と修正Nd値グラフ。土層の有無を切替可
  - A4 シート：標尺・標高・層厚・深度・推定土質・記事・測定値表・グラフ。縮尺 1:50／1:100、深い地点は複数枚に分割
- DXF は R12（AC1009）、Shift_JIS、文字スタイル JP（txt.shx＋extfont2.shx）
- 複数地点の管理、プロジェクトの JSON 保存・読込、計算表の CSV 出力

## 使い方

https://kazu0818.github.io/ram-sounding-log/ を開く。または `index.html` をダウンロードしてブラウザで開く（DXF は .dxf のまま保存される）。ライブラリは jsDelivr から読み込むため、Excel 読込と DXF 出力にはネット接続が必要。

## 使用ライブラリ

- [SheetJS Community Edition](https://sheetjs.com/) 0.18.5（Apache License 2.0）
- [encoding-japanese](https://github.com/polygonplanet/encoding.js) 2.5.0（MIT License）

いずれも jsDelivr から読み込む（リポジトリには同梱しない）。
