# Hearable Advertise Viewer
---
## Overview
Hearable Advatise Viewerはヒアラブルデバイス（フォスター電機 RN002）に実装されているアドバタイズ機能で通知されるデータを表示するためのフロントエンドアプリケーションです。\
★ デモ用Webサイト [https://foster-hearable.github.io/AdvertiseViewer/](https://foster-hearable.github.io/AdvertiseViewer/)

WebBluetoothを用いてヒアラブルデバイスRN002のアドバタイズをサーチし、各センシングデータの表示やWebSocketサーバーへのデータ送出を行います。\
WebSocketのデータはManufacturer Specific Dataをデータ列としたものが送出されるため、WebSocketサーバー側での加工や解析に用いることができます。

## 対応ブラウザ
WebBluetoothに対応したブラウザ\
　参考：[ブラウザー互換性一覧表 Mozilla.org]\
　https://developer.mozilla.org/ja/docs/Web/API/Web_Bluetooth_API#ブラウザーの互換性)
\
\
　※OSやバージョンによっては、対応ブラウザであっても動作しない場合があります

#### 動作することを確認しているブラウザ
- Chrome（Windows,Android）
- Edge（Windows）

\
※上記のいずれにおいてもchrome://flags#enable-experimental-web-platform-featuresを有効に切り替える必要があります
  
#### 動作しないことを確認しているブラウザ
- Safari（Mac,iOS）
- Chrome (Mac, iOS)
- Edge (Mac)

\
※Macで実行した場合は、継続的なアドバタイズのデータ受信が行えませんのでご注意ください

## データ構造

## 注意事項
- ヒアラブルデバイスに接続してから生体データが更新されるまで最大で20秒程度の時間がかかる場合があります。
- 左右のヒアラブルデバイスを使用している場合、状況に応じて自動的にどちらか片側のヒアラブルデバイスからのセンサー情報を取得します。\
  右または左の任意のヒアラブルデバイスからデータ取得を行いたい場合は、使用しないヒアラブルデバイスをチャージケースに収納してから接続してください。
- 動作確認されているブラウザであっても、バージョンやプラグインの状況などによってはアプリケーションが正常に動作しないことがあります。また、ブラウザまたはシステムの省エネモードなどの影響によりデータ更新タイミングが変化する場合があります。

  
※ワイヤレス通信は周囲の状況によりデータ欠落や再送・遅延が発生します。センサーデータはこれらの事象を考慮したうえでご利用ください。\
※このアプリケーションおよびヒアラブルデバイス（フォスター電機 RN002）は医療機器ではありません。医療行為には使用できません。\
※このアプリケーションはヒアラブルデバイス（フォスター電機 RN002）の評価を目的として[MITライセンス](https://github.com/foster-hearable/HeadTracker/blob/e59c1e2fe2de506fb53649f6b3cb550f1e6ca852/LICENSE.txt)の下に公開しております。
