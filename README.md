# habs-mvt

MVT port of HABS

# About

このレポジトリでは [明治時代初期土地利用・被覆デジタルデータベース](https://github.com/wata909/habs_test) の GeoJSON ファイルを
ズームレベル12 の Mapbox Vector Tile 形式 に変換したものを提供します。

# Demo

- <https://frogcat.github.io/habs-mvt/>

[![demo](https://user-images.githubusercontent.com/12029629/80337956-270f2f80-8896-11ea-92cd-b40282ffae7d.png)](https://frogcat.github.io/habs-mvt/)



# Usage

- このレポジトリを clone すると `docs/12` フォルダ配下にデータが `pbf` ファイル群が格納されているので、ご利用ください
- または `https://frogcat.github.io/habs-vt/{z}/{x}/{y}.pbf` のテンプレートより直接利用することも可能です


# License

- 本レポジトリで提供するデータのライセンスは [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.ja) となります
- デモのための HTML および javascript は MIT ライセンスです

# Note

MVT ファイル群は以下の手順で生成しています

```
$ git clone https://github.com/wata909/habs_test.git
$ cd habs_test
$ tippecanoe --no-tile-compression -z12 -Z12 -e output_dir -y code -l habs -ai */*/*.geojson
```
