# open-hinata
ol5+vueで作成したオープン版の「ひなたGIS」です。「ひなたGIS」の作者が作っています。
# Demo
<a href='https://kenzkenz.xsrv.jp/aaa/' target='_blank'>初期時</a>
<a href='http://bit.ly/2BPJGuQ' target='_blank'>２画面</a>
<a href='http://bit.ly/2BNnb9I' target='_blank'>３画面</a>
<a href='http://bit.ly/2QWvfiS' target='_blank'>４画面</a>

# Dependencies
地図ライブラリはol5を使用。フレームワークにvue+vuexを使用しています。vue CLI 3で開発、ビルドしています。
# Usage
vue CLI 3をインストールしてビルドします。js/layers.jsに追記することによりレイヤーを追加することができます。
```
npm run build
```
# Authors
ken ochiai

# 説明
## 変数
vuexを使用しています。
複数のコンポーネントから参照する可能性のある変数はstore(vuex)に設置しています。
自コンポーネントだけで済む変数は極力コンポーネントに置いています。
## URLにパラメータがないとき、初期起動時の動き
store.jsのlayerListsに従ってレイヤーを作成します。
store.jsのlayerListsはlayers.jsのlayersを参照しています。
## URLにパラメータがあるときの動き
pemalink.jsのpermalinkEventSetが作動して初期設定のレイヤーを削除します。その後にパラメータに従ってレイヤーを作成していきます。
## 起動時にレイヤーリスト下段を作成
起動時にレイヤーリスト下段（背景ダイアログの下段）を作成します。layerListsはlayers.jsのlayersに従ってリストを作っていきます。
## レイヤーリスト下段をクリックしたとき
クリックするとstoreにあるlayerListsにレイヤーの情報を追加します。追加されるとLayer.vueに仕掛けているwatchが動作してOLのレイヤーを操作します。

