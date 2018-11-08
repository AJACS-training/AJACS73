# AJACS番町1 実験データの生物学的解釈を助ける遺伝子発現DB・ウェブツールの使い方

大学共同利用機関法人 情報・システム研究機構  
データサイエンス共同利用基盤施設  
ライフサイエンス統合データベースセンター    
[小野 浩雅](https://sites.google.com/a/dbcls.rois.ac.jp/hono/)  
hono@dbcls.rois.ac.jp  
2018年8月29日(水)
AJACS番町1 @ JST東京本部（サイエンスプラザ）B1大会議室

----

これは統合データベース講習会 AJACS番町1「実験データの生物学的解釈を助ける遺伝子発現DB・ウェブツールの使い方」の講習資料です。  
講習会全体のプログラムは[こちら](http://events.biosciencedbc.jp/training/ajacs71)です。

----

## 概要

本講習は、だれでも自由に使うことができる公共データベースやウェブツールを活用して、研究のさまざまな場面で調べることの多い個々の遺伝子発現データを簡単に調べるための方法と基礎知識について学びます。  
また、自ら行なった大規模発現解析の(あるいは公共データベースから取得・解析した)結果として得られた数百〜数千におよぶ遺伝子セットについて、生物学的な解釈をする方法とその結果の考察を実践します。  

----

## 講習の流れ
今回の講習では、コンピュータを使って以下の内容について説明します。

- 研究現場で頻繁に使われるデータベースやツールを知る
    - 統合TV
- 個々の遺伝子の発現プロファイルを調べる
    - RefEx
        - 【実習1】RefExを使って、組織特異的遺伝子を検索する
- 数十～数千の遺伝子群の生物学的解釈
    - ChIP-Atlas
        - 【実習2】ChIP-Atlasのin silico ChIP を使って、興味ある遺伝子リストを制御する可能性の高い転写因子を調べる

----

## 講義に際しての注意とお願い
- みんなで同時にアクセスするとサイトにつながりにくくなることが予想されます。
    - 資料を見ながら自力で進められそうな方はどんどん先に、そうでない方は講師と一緒にすすめていきましょう。
    - サイトの反応が悪い時はタイミングをずらして実行してみてください。
    - 反応が無いからと言って何度もクリックするとますます繋がらなくなってしまいます。おおらかな気持ちで臨みましょう。
- こんなことは知ってて当たり前だと他の人に思われる質問を歓迎します。質問することのハードルを下げます。
    - 知っている人は講師を助けてください。サポート大歓迎です。
    - あなたが疑問に思ったことは、実は、隣の人やその隣の人もそう思っていることが多いです。
    - 当たり前に感じる質問や一見関係なさそうな質問がでると、「そういう質問をしてもよいのだ」という空気になり、この講義から得られる情報が増え、皆さんの受講満足度が上がります(たぶん)。
    - でも講師も知らないことは(多々)あります。(以下ループ)
- 実験的な試みとしてWeb上で匿名で質問・コメントできるフォームを用意してみました。
    - [講師用](https://docs.google.com/presentation/d/1Buj93jSKB-tWU1F37ykVEuv7Bu_q6KE_4hqICRCpTk4/edit#slide=id.p)
    - [受講者質問用フォーム](http://goo.gl/slides/as8xh7)(右クリックから「新しいタブで開く」推奨)    

----

#### 受講前アンケートにご協力いただき、ありがとうございます (回答数 87)

|統合TVを知っていますか?|人数|割合|
|:--|--:|:--:|
|知らない|25 名|29 %|
|聞いたことがある|8 名|9 %|
|知っている|15 名|17 %|
|使ったことがある|22 名|25 %|
|使っている|13 名|15 %|
|回答なし|4 名|5 %|
---
|自分で実験して得た、数十〜数千の遺伝子からなる<br>「遺伝子リスト」(例: 発現差のあった遺伝子など) を持っていますか?|人数|割合|
|:--|--:|:--:|
|これから実験をする・したい|16 名|18 %|
|公共データを活用する・したい|28 名|32 %|
|既に持っている|21 名|24 %|
|大規模発現解析の予定はない|15 名|17 %|
|回答なし|7 名|8 %|
---

## 研究現場で頻繁に使われるデータベースやツールを知る
### [統合TV](http://togotv.dbcls.jp/ja/)
- 生命科学分野の有用なデータベースやツールの使い方を動画で紹介するウェブサイト
    - http://togotv.dbcls.jp/ja/
    - ![統合TVトップページ](https://raw.githubusercontent.com/hiromasaono/training/master/images/180612_01.png)

    - YouTube版もあります http://www.youtube.com/user/togotv/
    - ![統合TV YouTube支店](https://raw.githubusercontent.com/hiromasaono/training/master/images/180612_02.png)
    - YouTubeのチャンネル登録をすると更新情報がメールで届きます。

- ウェブサイトへのアクセスの仕方から結果の解釈まで、操作の一挙手一投足がわかります。
    - 1400本を超える動画が公開されており、YouTube版だけで のべ 1,000,000回以上 再生されています。(2018年5月末現在)
    - ![YouTube統計](https://raw.githubusercontent.com/hiromasaono/training/master/images/180612_03.png)

- 講義・講習などの参考資料や後輩指導の教材として利用できます。
    - 本講義中、本家サイトが繋がらない時は、統合TVを見ればおおよその内容がわかるようになっています。
    - DBCLSの提供する便利な各種サービスをレビューする内容もあります。
      - [【NGSハンズオン2017】NBDC・DBCLSの各種サービス 今日から使える便利な生命科学系公共データベース in DBCLS](http://togotv.dbcls.jp/20171204.html)

- 統合TVに掲載されているコンテンツについてご引用いただく際に、恒久的な URL として [DOI](https://ja.wikipedia.org/wiki/デジタルオブジェクト識別子) (Digital Object Identifier) を使用することができます。

- 2014年8月以降に開催された過去の講習会の資料・テキストと動画が「[AJACS講習会資料](http://togotv.dbcls.jp/ja/ajacs_text.html)」で閲覧できるようになり、受講生の復習のみならず、初学者の学習教材として活用できます。

- 誰でも自由に利用可能なライフサイエンス分野のイラストが､統合TVから閲覧､利用することができるようになりました。[「自由に使える画像を探す」](http://togotv.dbcls.jp/ja/pics.html)
    - [Togo picture gallery](http://g86.dbcls.jp/~togoriv/)と[生物アイコン](http://togodb.biosciencedbc.jp/togodb/view/taxonomy_icon)の全画像500点以上を一覧できます。
    - 研究発表のスライド作成や資料作成等に､ぜひお使いください。
    - ![自由に使える画像を探す](https://raw.githubusercontent.com/hiromasaono/training/master/images/180612_04.png)

- お探しの動画が見つからない or 統合TV未掲載の場合は、[統合TV番組リクエストフォーム](http://togotv.dbcls.jp/ja/contact.html)へどうぞ!!

- 統合TVを作ってみたい方、募集中です。(オンラインで完結する作成環境を整備しており、遠隔地でもOKです。謝金あり。)

----

#### 習熟度ややりたいこと別にご参考ください
- 塩基配列解析に関わる基礎知識について
    - [「塩基配列解析のためのデータベース・ウェブツールとCRISPRガイドRNA設計 @ AJACSこまち」(2016年8月)](http://doi.org/10.7875/togotv.2016.122)

- 遺伝子発現データを公共DBで検索・取得・解析する方法について
    - [「遺伝子発現DB・ウェブツールの使い方 応用・実践編」(2015年5月AJACS御茶ノ水)](http://togotv.dbcls.jp/ja/ajacs2015007.html)

- 非モデル生物のデータをモデル生物のデータに見立てるためのID対応表づくりについて
    - [「コマンドラインで遺伝子配列を解析する」（2012年7月）](https://github.com/AJACS-training/AJACS32/blob/master/05_bono/README.md)

- 次世代シーケンス(NGS)データの解析について
    - [【NGS】に関係する動画・講習会資料・新着論文レビュー](http://togotv.dbcls.jp/tags.html?tag=NGS)

- NGS解析について、さらにもっと基礎から応用までを深く学びたい方向け (それぞれ約50時間程度)
    - [「バイオインフォマティクス人材育成カリキュラム（次世代シークエンサ）速習コース(2014年8月)](https://www.youtube.com/playlist?list=PL0uaKHgcG00abmj1Nzs1SUhqKLjf_PFBB)
    - [「バイオインフォマティクス人材育成カリキュラム 次世代シークエンサ(NGS)ハンズオン講習会(2015年8月)](https://www.youtube.com/playlist?list=PL0uaKHgcG00Yo0Cn0rcF23xof5hqCzGQb)
    - [NGSハンズオン講習会2016](https://www.youtube.com/watch?v=TSa1yPy_sdM&list=PL0uaKHgcG00ZNpICun17CEAFpV_5Q6GCA)
    - [NGSハンズオン講習会2017](https://www.youtube.com/watch?v=6Fzvl_I48tM&list=PL0uaKHgcG00YDmBXYWOgkmfeURjc8BZkk)
    - [上記の動画+講習会資料のまとめページ@統合TV](http://togotv.dbcls.jp/ja/tags.html?tag=NGS速習・ハンズオン)

- 疾患と多型、変異に関するデータベース (COSMIC,TCGA 等)
    - [【多型】に関係する動画・講習会資料・新着論文レビュー](http://togotv.dbcls.jp/tags.html?tag=%E5%A4%9A%E5%9E%8B)
----

## 個々の遺伝子の発現プロファイルを調べる
### [RefEx (Reference Expression dataset)](http://refex.dbcls.jp/)
- 遺伝子発現解析の基準となるデータを快適に検索できるウェブツール
    - [http://refex.dbcls.jp/](http://refex.dbcls.jp/)
    ![Fig-1](https://raw.githubusercontent.com/dbcls/website/master/services/images/DBCLSservices_RefEx_jp_fig-1_180523.png)  

    ![Fig-2](https://raw.githubusercontent.com/dbcls/website/master/services/images/DBCLSservices_RefEx_jp_fig-2_180523.png)
    ![fig-3'](https://raw.githubusercontent.com/dbcls/website/master/services/images/DBCLSservices_RefEx_jp_fig-3_180523.png)
- 公共DBにある正常組織や細胞株における遺伝子発現データを再利用・整理
- 4つの異なる実験手法（EST、GeneChip、CAGE、RNA-seq）によって得られた正常組織、初代培養細胞、細胞株における遺伝子発現データを検索、閲覧可能
    - 最近新たに、FANTOM5 CAGEデータが追加(ヒト556種、マウス286種)
    - 掲載しているデータやオリジナルデータなどの詳細については、[RefExについて](http://refex.dbcls.jp/about.php?lang=ja)
- このツールでできること
    - 正常組織における遺伝子発現データを調べる
    - 測定手法による遺伝子発現量の差異を比較する
    - 組織特異的遺伝子をワンタッチで検索可能
    - 遺伝子発現解析などで見出された不詳な遺伝子群の機能および関係性を調べる
- RefExで掲載されているデータはすべて再利用可能
    - オリジナルデータの再処理方法の詳細は[GitHub](https://github.com/dbcls/RefEx/tree/master/Rawdata_Processing)に
    - 再処理済みの発現データやサンプルアノテーション等のすべてのデータは[figshare](https://figshare.com/)に
    - 「The RefEx analysis」として論文に引用していただいた活用例
         - [Aberrant IDH3α expression promotes malignant tumor growth by inducing HIF-1-mediated metabolic reprogramming and angiogenesis, Oncogene, (22 December 2014) | doi:10.1038/onc.2014.411 @ Figure 6](http://www.nature.com/onc/journal/vaop/ncurrent/full/onc2014411a.html)
         - がん研究者が、発現解析実験で見出した数百個の治療標的・候補遺伝子の絞込みに使えないか検討した。
         - これらの候補遺伝子の正常組織における発現量が低ければ、治療標的とした場合に悪影響・副作用が小さくなると仮説した。
         - 実際に、これらの遺伝子の発現量をRefExで確認し、追加確認実験の優先順位付けを効率的に行うことができた。
    - その他RefExを引用した論文の一覧はこちらでご覧いただけます。
        - [https://dbcls.rois.ac.jp/references.html#RefEx](https://dbcls.rois.ac.jp/references.html#RefEx)

#### 参考文献
  * Hiromasa Ono, Osamu Ogasawara, Kosaku Okubo, Hidemasa Bono
     **RefEx, a reference gene expression dataset as a web tool for the functional analysis of genes**
             Scientific Data, 4:170105
             [DOI: 10.1038/sdata.2017.105](http://doi.org/10.1038/sdata.2017.105)
  * 川路 英哉、粕川 雄也、坊農 秀雅、小野 浩雅 「FANTOM5データを誰でも活用できる形に」 Scientific Data誌著者インタビュー (平成29年8月29日)
             https://www.natureasia.com/ja-jp/scientificdata/papers-from-japan/fantom5
  * 小野 浩雅・坊農 秀雅 「遺伝子発現解析の基準となるデータを快適に検索できるウェブツールRefEx」 ライフサイエンス新着論文レビュー (平成29年9月5日)
             [DOI: 10.7875/first.author.2017.093](http://doi.org/10.7875/first.author.2017.093)
  * 統合TV 「RefExの使い方」[DOI: 10.7875/togotv.2014.009](http://doi.org/10.7875/togotv.2014.009)
----

#### 【実習1】RefExを使って、組織特異的遺伝子を検索する
- 【復習用】[RefExの使い方](http://doi.org/10.7875/togotv.2014.009)

1. http://refex.dbcls.jp/ を開きます。
2. 画面中央の「組織特異的に発現する遺伝子を見る」の臓器アイコンにカーソルを合わせると、更に詳細な部位のアイコンが出るので、調べたい臓器（例として肝臓）をクリックします。  
  - ![http://gyazo.com/35c8f38340753e8f433cb8c4d8fd812b](http://i.gyazo.com/35c8f38340753e8f433cb8c4d8fd812b.jpg)

3. 検索結果一覧が表示されます。検索結果一覧では、「ソート項目の切り替え」や「絞り込み検索」、「リストへの追加」ができます。(手順11以降で解説します。)
4. 各遺伝子の青字の部分（例 [fibrinogen alpha chain](http://refex.dbcls.jp/gene_info.php?lang=ja&db=human&geneID=2243&refseq=NM_000508&unigene=Hs.351593&probe=205649_s_at))をクリックすると詳細情報を閲覧できます。
5. 「ヒートマップ on Bodyparts3D」では、表示する部位の切り替え（全身・体幹部・頭部）ができます。「皮膚・骨格筋を表示」もしくは「アニメーション表示」にチェックを入れるとどのように表示されるでしょうか。
6. 「組織40分類別データ」では、バーの上にマウスオーバーすると測定部位と発現値が表示されます。
7. 「Download」をクリックすると、表示中の遺伝子の組織40分類別の発現データがタブ区切り形式でダウンロードできます。
8. 「Probe set ID」のリンク先をクリックすると、どういう情報が参照できるでしょうか。
9. 遺伝子オントロジー([Gene Ontology](http://array.cell-innovator.com/?p=1085):GO ID)をクリックすると、そのGO termを持つ他の遺伝子を一括で検索できます。
  - 例として、[GO:0007596](http://refex.dbcls.jp/genelist.php?lang=ja&db=human&idkind=1&ids=GO:0007596)   blood coagulation をクリックしてみましょう。
  - ![遺伝子詳細情報](http://i.gyazo.com/3cca3d33c17e845ad5dae8749d7fbd15.jpg)

10. 右側のFANTOM5 CAGEのタブをクリックすると、FANTOM5 CAGEデータのビューアに切り替わります。
 - ビューアは上部が拡大図で、下部が全体表示になっています。
 - 検索窓にキーワードを入れるとサンプル名を検索できます。ヒットしたサンプルはオレンジ色で強調されます。
 - 右側に、サンプル名と発現値、サンプル分類が表示されます。
 - [RefEx用に整理したサンプル情報一覧](http://bit.ly/fantom5cagehuman)も閲覧可能です。
 - ![FANTOM5 CAGE Viewer](http://i.gyazo.com/51d0b3db07efe64a6fdafb054cd4217f.jpg)
11. 検索結果一覧に戻ります。ソート項目を切り替えて、どのように結果が変わるでしょうか。
 - ![検索結果一覧](http://i.gyazo.com/5e87d20d9b31711e797ef17677be7263.jpg)
12. 様々な条件で検索結果を絞り込むことができます。絞り込み検索は左のバーから行えます。
 - 遺伝子名に「liver」を含むデータは何件あるでしょうか。
 - 「遺伝子名」の下の「条件なし」をクリックして表示されるウインドウに「liver」と入力し、「Include」をクリックし、「この条件で絞り込み」を押します。
 - 「遺伝子名」の項目で「Exclude」に「solute」を加えると、検索結果はどう変わるでしょうか。
 - 「組織」の項目で、データ元をRNA-seqに変更したり、臓器の指定を追加すると検索結果はどう変わるでしょうか。
 - 「必ず含むデータセット」の「ALL」にチェックを入れると、検索結果はどう変わるでしょうか。
13.  個々の遺伝子の詳細情報は、リストに追加することで並列に比較することができます。
 - [肝臓特異的遺伝子の検索結果一覧](http://refex.dbcls.jp/genelist.php?lang=ja&db=human&roku_valid=1&rk[31]=31&order_key=score)に移動して、3つの遺伝子を「リストに追加」してみましょう。
 - 追加した件数は「リストを見る」の横に表示されます。
 - 「リストを見る」をクリックするとリストに移動します。
 - 『並べて表示する』にチェックを入れて、「遺伝子を並べて表示」をクリックします。
 - 遺伝子発現データやGeneOntology情報を並列に比較することで見えてくる「違い」はなんでしょうか。その違いからどういうことが推測できるでしょうか。
 - ![並列比較1](http://i.gyazo.com/ba11e4c7c38a4e78d3a64d7b8b6efee8.jpg)
 - ![並列比較2](http://i.gyazo.com/3f2f9e5cbf135a2c298ae164d6360302.jpg)
14. 自分の研究テーマに関連する、また興味のある遺伝子について検索してみましょう。

----

## 数十～数千の遺伝子群の生物学的解釈

- マイクロアレイやNGS実験を行うと大量の発現変動遺伝子 (Differentially Expressed Genes: DEGs)が得られます｡
- 一般的な遺伝子発現解析の第一歩は､実験条件によって得られた数十～数千のDEGsが生物学的にどういう意味を持つかを考えることです。
  - ![Gyazo](http://i.gyazo.com/52cb4c40b1313a52f8ded6923bdd8ef0.png)

### ChIP-Atlas
ChIP-Atlasは、論文などで報告された ChIP-seq データを閲覧し、利活用するためのウェブサービスです。データ処理の知識やスキルがない方でも簡単に利用できます。データソースは、公開 NGS データレポジトリ (NCBI, EMBL-EBI, DDBJ) に登録されたほぼ全ての ChIP-seq データです。ChIP-Atlas は、九州大学大学院医学研究院 発生再生学分野 (http://www.dev.med.kyushu-u.ac.jp) と DBCLS が共同で開発しています。  
 (http://chip-atlas.org/)

![fig10](https://raw.githubusercontent.com/hiromasaono/training/master/images/180612_10.png)

![fig11](https://raw.githubusercontent.com/hiromasaono/training/master/images/180612_11.png)

#### ChIP-Atlasの機能
##### Peak Browser
* 既報の ChIP-seq データをまとめて閲覧し、何がどこに結合しているかが一目でわかります。Integrative Genomics Viewer (IGV) によりスムーズなブラウジングが可能で、興味の遺伝子のシス調節領域を予測したり、それを制御する転写因子の予測ができます。
  * [ChIP\-Atlasを使って既報のChIP\-seqデータをまとめて閲覧する 〜Peak Browserの使い方〜](http://togotv.dbcls.jp/20180123.html)
##### Target Genes
* 興味のある転写因子を選択し、その標的遺伝子候補を検索できます。
  * 統合TV「[ChIP\-Atlasを使って興味のある転写因子を選択しその標的遺伝子候補を検索する 〜Target Genesの使い方〜](http://togotv.dbcls.jp/20180124.html)」
##### Colocalization
* 興味のある転写因子を選択し、それとゲノム上で共局在する転写因子候補を検索できます。
  * 統合TV「[ChIP\-Atlasを使って共局在タンパク質を探す 〜Colocalizationの使い方〜](http://togotv.dbcls.jp/20180128.html)」
##### Enrichment Analysis
* ユーザデータを受け付け、既存データとの比較解析をおこないます。たとえば、興味のある遺伝子リストを submit すると、それらをまとめて制御する転写因子候補が返されます。ほかにも BED 形式のファイルや、シーケンスモチーフを submit すると、それらに enrichment する転写因子群が返されます。


#### 利用例
* 論文として発表された ChIP-Seq データを閲覧したい
* 興味のあるゲノム領域における、転写因子や修飾ヒストンの分布を知りたい
* 興味のある転写因子の下流遺伝子や、複合体形成パートナーを知りたい
自身の研究データと公開 ChIP-seq データを用いて比較解析をおこないたい
#### 参考文献
- Source code and documentation    
  - https://github.com/inutano/chip-atlas
- Preprint
  - Shinya Oki, Tazro Ohta, et al. Integrative analysis of transcription factor occupancy at enhancers and disease risk loci in noncoding genomic regions. bioRxiv 262899; doi: https://doi.org/10.1101/262899
- Database
  - Oki, S; Ohta, T (2015): ChIP-Atlas. http://dx.doi.org/10.18908/lsdba.nbdc01558-000
- Publications citing ChIP-Atlas http://chip-atlas.org/publications

### 【実習2】ChIP-AtlasのEnrichment Analysis を使って、興味ある遺伝子リストを制御する可能性の高い転写因子を調べる
* 「発現差のあった遺伝子リスト」を持っている想定で、それらの遺伝子に結合しうる、あるいは上流でそれらの遺伝子の発現を制御する可能性がある転写因子を検索する
* 使用するデータ
  - [180627_List_of_GeneSymbol_txt](https://github.com/AJACS-training/AJACS71/blob/master/04_hono/180627_List_of_GeneSymbol.txt)
    - ある「興味ある遺伝子リスト」をGeneSymbolにID変換したデータ。
    - これを使って、もともとどういう遺伝子リストだったかを考察します。
  - ChIP-Atlas では、遺伝子IDとしてGeneSymbolのみを受け付けているので、それ以外のIDで遺伝子リストを持っている場合は、適宜変換が必要です。
    - ID変換はいろいろなツールがあるが、今回は[HGNC BioMart](https://biomart.genenames.org/)を利用する。
      - HGNC(The HUGO Gene Nomenclature Committee)はヒトのGeneSymbolを認定・管理している機関。
      - [DAVID(Database for Annotation, Visualization and Integrated Discovery)
   ](https://david.ncifcrf.gov/)のGene ID Conversion Toolも便利。([使い方動画](https://youtu.be/4f1t1ma9IRc?t=4m5s))

1. [ChIP\-Atlas \- Enrichment Analysis](http://chip-atlas.org/enrichment_analysis)にアクセスする
2. 下図のようにオプションを設定する
![fig12](https://raw.githubusercontent.com/hiromasaono/training/master/images/180612_12.png)
3. submit すると遺伝研スパコンへクエリが飛ぶ(ので、講義中は見てるだけにしてください)
4. submit したあとの画面
![fig13](https://raw.githubusercontent.com/hiromasaono/training/master/images/180612_13.png)
5. 計算が終わるまで待つ
![fig14](https://raw.githubusercontent.com/hiromasaono/training/master/images/180612_14.png)
6. 計算が終わると、「Result URL」が有効になる
  - 今回の例では、 http://ddbj.nig.ac.jp/wabi/chipatlas/wabi_chipatlas_2018-0606-1701-36-865-010614?info=result&format=html
7. 結果の解釈をする
  - 今回は、どういう「興味ある遺伝子リスト」をクエリとしたか考察してみましょう。
  - 結果の見方としては、「p-valueが低く、Overlaps/My dataが多く、Fold Enrichmentが高い」転写因子がたくさんヒットしてくると入力した遺伝子群をまとめて制御する、マスター転写因子を抽出できている確度が高い

8. [答え合わせ](https://github.com/AJACS-training/AJACS71/blob/master/04_hono/180627_ChIP-Atlas_answer.md)





## まとめ
- つまみ食い的ではありますが、通り一遍の今日から使える便利な生命科学系公共データベース・ウェブツールを学びました。
- 顕微鏡 や 実験試薬 などと同じ「道具(ツール)」
- 便利な「道具」を知って、その使い方が分かれば、あとは情報分析力と想像力の勝負。
- 仮説構築から始まり、実験計画・検証、データ解析、そして論文執筆(以下ループ)という研究サイクルを加速化・効率化していきましょう。
- 困ったら、統合TV!! (※宣伝)
- 研究に役立ったら、ぜひ引用・クレジットを!
- DBCLSの提供するサービス(あるいはそれ以外でも)が、あなたの研究に役立ったら、どんなに些細な事でもぜひ引用(論文、URL等)してください。DBCLSの活動は、提供するサービスがどのくらい活用されたかについて主に引用数などで評価されており、利用者の方の積極的なサポートが必要不可欠です!!


-----
#### もし時間が余れば
### [DAVID: The Database for Annotation, Visualization and Integrated Discovery](http://david.abcc.ncifcrf.gov/)
- アメリカ国立アレルギー・感染症研究所が開発･運用
- 原著論文 [PMID: 19131956](http://www.ncbi.nlm.nih.gov/pubmed/19131956)
- 遺伝子リストのコピペで簡単にエンリッチメント解析 ( GO､KEGG など )
- 対応生物種･遺伝子ID が 豊富｡ ID変換ツールもある
- IDリストしか投げられない (発現量込みやタイムコースデータは不可)
- 2010年以来データ更新が止まっていたが､最近､アップデートされた｡ [DAVID 6.8 (current beta release) May. 2016](https://david.ncifcrf.gov/content.jsp?file=release.html)  

#### マイクロアレイデータの準備
- サンプルデータとして、[NCBI GEO](http://www.ncbi.nlm.nih.gov/geo/)から取得した公共の遺伝子発現データを用います。このデータは、ある実験の前後の2群間で有意に発現減少した遺伝子群のリストです。  

     → [マル秘遺伝子リスト](https://github.com/AJACS-training/AJACS71/blob/master/04_hono/secret_list.txt)  （右クリックして「新しいタブで開く」もしくは「名前を付けてリンク先を保存」してください。）

- このデータは、どのような実験から得られたデータなのか、どのように解釈できるのかをDAVIDを使って考察してみましょう！  

#### 【実習2】DAVIDを用いて、発現データの結果を生物学的に解釈する
- 【復習用】[DAVIDを使ってマイクロアレイデータを解析する 2012](http://doi.org/10.7875/togotv.2012.079)
- 【復習用】[DAVIDの使い方 実践編](http://doi.org/10.7875/togotv.2013.033)  

1. [DAVID](http://david.abcc.ncifcrf.gov/)にアクセスし、上部メニューの「Start Analysis」をクリックします。

- ![Gyazo](http://i.gyazo.com/f976f39aeb060a96a790f0e5b281aabe.png)

2. 画面左側バーで、probe IDリストをコピペ or ファイルを指定します。
3. リストのIDの種類タイプを選択します。 … 今回は、「AFFY_ID」と「Gene List」
4. Submit List をクリックするとリストが読み込まれます。

- ![Gyazo](http://i.gyazo.com/e8275cf9dbb203b3d8577307b462c783.png)

5. アップロードしたリストは、左側バーの「List Manager」で「Uploaded List_1」として保存されています。削除やrenameもできます。

- ![Gyazo](http://i.gyazo.com/e8270d82a68decba0249daa49914fba9.png)

6. 解析を続けます。真ん中の「Functional Annotation Tool」をクリックします。
7. 「Gene Ontology」をクリックすると、Gene Ontologyを用いた解析の細かいメニューが表示されます。

- ![Gyazo](http://i.gyazo.com/38905ceb16d6b702059667e4fb404531.png)

8. 今回は、GOTERM_BP_FAT (BP = Biological Process)に注目します。その右の「Chart」をクリックすると結果がポップアップされます。

 - ![Gyazo](http://i.gyazo.com/78301700c3d952957dd599bbb83c785f.png)

9. タイトル行をクリックするとソートできます。  
10. さらに、GOTERM_CC_FAT や GOTERM_MF_FAT を見て、上位にリストされたGOTermにどのような共通点・相違点があるでしょうか。
 - CC = Cellular Component
 - ![Gyazo](http://i.gyazo.com/117720204dfb06a3f3605f4aedec2dba.png)
 - MF = Molecular Function  
 - ![Gyazo](http://i.gyazo.com/6feb8e34beab45769e2d3e66c3c5d570.png)
11. Pathways > KEGG_PATHWAY や Tissue Expression > UP_TISSUE なども見てみましょう。

12. DAVIDで得られた結果を踏まえ、「ある実験」とはどのような実験であったか考察してみましょう。
 - マル秘遺伝子リストは「ある実験の前後の2群間で有意に発現減少した遺伝子群のリスト」  
 - 生物種はArabidopsis thaliana (シロイヌナズナ)  

---

[答え合わせ](https://github.com/AJACS-training/AJACS71/blob/master/04_hono/answer.md)
