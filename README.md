# リアルタイム地震ビューアー多観測網版

[リアルタイム地震ビューアー](https://github.com/kotoho7/scratch-realtime-earthquake-viewer-page)に、独自の観測網や海外の緊急地震速報を追加したものです。

## 概要

本プロジェクトは、日本国内だけでなく台湾や中国の地震情報、および有志によるコミュニティ観測網のデータを統合してリアルタイムに表示することを目的としています。

## 追加機能・対応データソース

公式版の機能に加え、以下のデータを受信・表示する機能を追加しています。

### 台湾 強震観測網 / 台湾 緊急地震速報
- 台湾のコミュニティ観測網のリアルタイム震度、緊急地震速報を表示します。
- 台湾強震観測網のデータは揺れ検出には使用されません。
- 台湾の震度は日本の震度と異なる尺度ですが、概ね一致するためそのまま表示しています。
* ソース: `Trem-RTS`


### 中国 緊急地震速報 / 日本 緊急地震速報
- 中国地震台網や四川地震局が発表する緊急地震速報や、気象庁が発表する緊急地震速報をwebsocet接続で即座に受信します。
* ソース: [wolfxAPI](https://wolfx.jp/apidoc)


### P2P強震モニタ（コミュニティ観測網）
- 私が作成しているP2P強震モニタの情報を受信して自動的に表示します。
- ユーザーのスマートフォンの加速度センサーを使って計測震度を求めていますが、防災科研の強震モニタのリアルタイム震度とは計算方法が一部異なります。  
- 意図的かどうかにかかわらず異常な値が出る可能性があります。
- このデータは揺れ検出には使用されません。
* ソース: [P2P強震モニタ (GitHub)](https://github.com/anesewo/P2Pkyousin)

### 緊急地震速報について
 - 気象庁以外の機関が発表する緊急地震速報においては、震源地名が気象庁の使用するコードと対応できないので、
   内容の緯度・経度から地名を求めています。
 - 気象庁以外の機関が発表する緊急地震速報内には日本の推定震度は含まれていないので、気象庁以外の機関が発表する推定最大震度は一律で全て「震度不明」として表示しています。
 - 使用しているAPIの仕様上、推定長周期地震動階級は表示されません。地図塗りつぶしの内「予想長周期地震動階級」は多観測網版ではリプレイなど特殊な状況を除き何も表示されないことに注意してください。


## ライセンス

### 元作品
本プロジェクトは、ベースとなった「リアルタイム地震ビューアー」のライセンスに基づき、 **CC BY-SA 2.0（クリエイティブ・コモンズ 表示 - 継承 2.0）** で公開されています。

* **継承元:** [リアルタイム地震ビューアー](https://github.com/kotoho7/scratch-realtime-earthquake-viewer-page)

### 緯度と経度から地名
[緯度経度からAreaEpicenterコード](https://scratch.mit.edu/projects/874829767/)


## 問い合わせ
リクエストやバグ報告等はこちらで受け付けています。  
 - [Googleフォーム](https://docs.google.com/forms/d/e/1FAIpQLSdbn7IblC1k0me4JgaFOAaIAEoHIyThoQmXslGGKRJvFdRFgg/viewform)
 - [discordサーバー（招待コード）](https://discord.gg/DDCvpYEa9A)
 - [多観測網版製作者X](https://x.com/aseneo2)  

## 注意事項
多観測網版製作者は **パッケージ版、turbowarp版、scratch版** 及び、**改造版**製作者とは全くの無関係です。  
元作品製作者、改造版製作者に対して、このバージョンに関する問い合わせは迷惑になる可能性があるため行わないでください。


## クレジット（元作品と同様）

### 日本地図

- [気象庁 予報区等GISデータ](https://www.data.jma.go.jp/developer/gis.html)
- [国土交通省 国土数値情報 湖沼データ](https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-W09-v2_2.html)

### 世界地図

- [Natural Earth 1:10m Cultural Vectors (Japan POV)](https://www.naturalearthdata.com/downloads/10m-cultural-vectors/)
- [NOAA ETOPO](https://www.ngdc.noaa.gov/mgg/global/)

### フォント

- [Akshar](https://fonts.google.com/specimen/Akshar)
- [BIZ UDPGothic](https://fonts.google.com/specimen/BIZ+UDPGothic)  
※どちらも SIL Open Font License

### 効果音

- [OtoLogic ニュース テロップ](https://otologic.jp/free/se/news-accent01.html)
