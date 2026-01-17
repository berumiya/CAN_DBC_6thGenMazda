# CAN DBC for MAZDA Roadster 2015-2023 (ND1)



## このリポジトリについて

このリポジトリは、マツダ ロードスター 2015-2023(ND1) における CAN 通信を解析し、  
その結果を [DBC形式](https://www.csselectronics.com/pages/can-dbc-file-database-intro) にまとめて公開するためのものです。

本 DBC は実車通信の観測、ログ解析、既知仕様との照合などをもとに、  
個人が独自に調査・推定した内容です。

「完成版」を目指すというよりも、知見を共有しながら育てていくことを目的としています。
解析途中の成果も含めて共有し、今後継続的に発展していくことを前提としています。



## 収録内容

- HS-CAN, MS-CAN 用 DBC ファイル  
  - 信号定義（ID、信号名、スケール、オフセット等）  
  - コメント（信号の意味、挙動、推定根拠など）

個人の解析結果をベースとしており、現時点では枠組みのみが定義されているメッセージや、検証途中のシグナルも多く含まれています。
今後の解析の進展に伴い、内容の精緻化や補完を進めていく予定です。  
Issue による指摘や情報共有、検証結果に基づく Pull Request を歓迎します。



## 対象車両

本 DBC が直接対象とする車両は以下のとおりです。

- メーカー：マツダ  
- 車種／型式：ロードスター ND  
- 年式：2015-2023 (ND1前期 & 後期)  
- バス種別： HS-CAN(500kbps), MS-CAN(125kbps)  

上記以外の車両・年式について
- 他のマツダ第６世代電装車両とも類似性が高いですが、一部異なる可能性があります。
  - **BCMM** 構成車は類似性が非常に高く、相互に参考になるはずです。
    - DEMIO/MAZDA2(DJ), CX-3(DK)
  - **FBCM/RBCM** 構成車は一部構成が異なりますが、大枠では類似しています。
    - CX-5(KE), CX-5(KF), CX-8(KG), アクセラ(BM/BY), アテンザ/MAZDA6(GJ) 等
- ND2(2024以降)はまったく様子が異なります。

### 補足：NDの世代呼称について
マツダ・ロードスター (MX-5 ND) では、日本国内と海外で世代通称が異なります。  
本リポジトリでは各 README の言語に応じて一般的に使われている通称を採用しており、同一の年式範囲に対して異なる世代通称となっています。
対象車両の実際の範囲は一致しています。

| 年式範囲        | 日本での通称 | 海外での通称 |
|-----------------|--------------------------|------------------------------------|
| 2015–2018       | ND1 前期                 | ND1                                |
| 2018–2023       | ND1 後期                 | ND2                                |
| 2024–           | ND2                      | ND3                                |



## DBC（CAN DBC）とは何か

CAN DBC（DBC ファイル）は、CAN バス上で送受信される生データ（バイナリ）と人間が読める値（物理量）を対応付ける **データベース形式ファイル** です。  
Vector 社によって開発され、自動車業界でデファクトスタンダードとして広く使われています。

詳しくは CSS Electronics [**a simple intro to DBC**](https://www.csselectronics.com/pages/can-dbc-file-database-intro) をどうぞ

### DBC 対応ツール

- [**SavvyCAN**](https://www.savvycan.com/)  
  オープンソースのフリーソフトです。DBCを活用して強力なCANバス解析ができます。  

- [**Vector CANdb++ / CANalyzer / CANoe など**](https://www.vector.com/jp/ja/products/products-a-z/software/)  
  DBC形式を開発した本家本元です。完全にエンタープライズ向けです。  
  個人で買う性質のものではありませんが、カーメーカーや電装サプライヤ等の開発部門では最もメジャーです。



## 注意事項・免責

- 本 DBC の内容はメーカー公式資料ではなく、個人の趣味による解析に基づきます。  
  内容の正確性・完全性を保証するものではありません。  
  本データを使用したことによるいかなる損害についても、作者は責任を負いません  
- 基本的にND1後期(2022年式990S)日本仕様車ベースで解析を行っています。ND1前期(2015-2018前半)や海外仕向車では一部異なる場合があります。

特に走行中の車両CANバスへの接続・送信については、
十分な知識と責任のもとで行ってください。



## 改善へのご参加について

誤りの指摘、追加情報、改善提案などの改善を歓迎します。  
Issue や Pull Request を通じてご連絡ください。
その際のコントリビューション部分は CC-BY 4.0 に同意したものとします。

その際、以下の情報があると助かります。

- 対象車両情報  
- 観測条件（走行状態、操作内容など）  
- ログや根拠となる情報  



## ライセンス
本作品は Creative Commons Attribution 4.0 International（CC-BY 4.0）ライセンスの下で公開されています。



## 作者自己紹介
**berumiya** です。よろしくお願いします。  
2022年式 NDロードスター **990S** で日々電装カスタムを楽しんでいます。  
みんカラよければ見ていってください！ [minkara.carview.co.jp](https://minkara.carview.co.jp/userid/615186/car/3285399/profile.aspx)

<a href="images/Author_berumiya_1.jpg"  style="display: inline-block; margin-right: 20px;">
  <img src="images/Author_berumiya_1.jpg" alt="Author berumiya" height="200"/>
</a>
<a href="images/Author_berumiya_2.jpg" style="display: inline-block;">
  <img src="images/Author_berumiya_2.jpg" alt="Author berumiya" height="200"/>
</a>