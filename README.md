# get-geojson-from-gsivector
地理院地図Vectorのベクトルタイルからgeojsonを取得するツール

https://mghs15.github.io/get-geojson-from-gsivector/index.html

（試作版：範囲指定モードがあるもの）
https://mghs15.github.io/get-geojson-from-gsivector/getgeojson_heavy.html

## 使い方
### source layer 単位での取得
1. レイヤリストから、ダウンロードしたいレイヤ（source layer）にチェックを入れる。
2. 「実行」ボタンをクリック。
3. 「ダウンロード」ボタンからGeoJSONをダウンロード。

### 地物一つ毎の取得
1. 地図上で、取得したい地物をクリックして選択。
2 「ダウンロード」ボタンからGeoJSONをダウンロード。

### 試作版：範囲指定モード

以下の2通りから選択

* `表示タイル内地物をすべて取得`：表示している範囲でロードされているタイルに存在する地物をすべて取得する。
* 地図上で範囲を指定し、その範囲内の地物をすべて取得する。こちらの方が負荷が大きい。

いずれの場合も、`取得したGeoJSONをダウンロード`ボタンからGeoJSONをダウンロード。

## 技術メモ
* Mapbox GL JSの`queryRenderedFeatures()`を用いている関係上、表示している「タイル」に入っている地物をすべて取得する。
* タイル境界の重複が含まれてしまう。
* 範囲指定で切り出す場合、切り出した後に空の地物が残ってしまう。

## 参考文献
* Turf <br> https://turfjs.org/docs/
* Mapbox GL JS API Referece (queryRenderedFeatures) <br> https://docs.mapbox.com/mapbox-gl-js/api/#map#queryrenderedfeatures
* 地理院地図Vector（仮称）提供実験 <br> https://github.com/gsi-cyberjapan/gsimaps-vector-experiment
