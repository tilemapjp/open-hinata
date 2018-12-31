# open-hinata
じわじわ作成中！
## 変数
複数のコンポーネントから参照する可能性のある変数はstoreに設置している。
## URLにパラメータがないとき。初期起動時
store.jsのlayerListsに従ってレイヤーを作成する。
store.jsのlayerListsはlayers.jsのlayersを参照している。
## URLにパラメータがあるとき
pemalink.jsのpermalinkEventSetが作動して初期設定のレイヤーを削除する。その後にパラメータに従ってレイヤーを作成していく。
## 起動時にレイヤーリスト下段を作成
起動時にレイヤーリスト下段（背景ダイアログの下段）を作成する。layerListsはlayers.jsのlayersに従ってリストを作っていく。
## レイヤーリスト下段をクリックしたとき
クリックするとstoreにあるlayerListsにレイヤーの情報を追加する。追加されるとLayer.vueに仕掛けているwatchが動作してOLのレイヤーを操作する。

