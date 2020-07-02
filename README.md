# get-geojson-from-gsivector
地理院地図Vectorのベクトルタイルからgeojsonを取得するツール

https://mghs15.github.io/get-geojson-from-gsivector/getgeojson.html

（範囲指定モードがないもの）
https://mghs15.github.io/get-geojson-from-gsivector/getgeojson_simple.html

## 使い方
以下の2通りから選択

1. `表示タイル内地物をすべて取得`：表示している範囲でロードされているタイルに存在する地物をすべて取得する。
2. 地図上で範囲を指定し、その範囲内の地物をすべて取得する。こちらの方が負荷が大きい。

いずれの場合も、`取得したGeoJSONをダウンロード`ボタンからGeoJSONをダウンロード。

## 課題
* 範囲指定で切り出す場合、切り出した後に空の地物が残ってしまう。

## 参考文献
* Turf <br> https://turfjs.org/docs/
* Mapbox GL JS API Referece (queryRenderedFeatures) <br> https://docs.mapbox.com/mapbox-gl-js/api/#map#queryrenderedfeatures
* 地理院地図Vector（仮称）提供実験 <br> https://github.com/gsi-cyberjapan/gsimaps-vector-experiment
