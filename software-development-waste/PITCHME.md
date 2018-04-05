## TECH TALK VOL.0

# ソフトウェア開発のコスト
2018/04/05 @EDOCODE Inc.

### REFERENCE
[Software Development Waste](https://www.researchgate.net/publication/313360479_Software_Development_Waste)

_Todd Sedano, Paul Ralph, C´ecile P´eraire_ - May 2017

### SPEAKER
Kyo Yamada ([Github](https://github.com/YMD7))

---

# 論文の要旨
- ソフトウェア開発は、異なる素養やスキルセットを持つ人々が関連する、非常に複雑な活動である
- こうした活動は多くの無駄ーここでいう無駄とは顧客やユーザーにとって価値のない工数・稼働ーを生む機会が非常に多い
- この論文の目的は、ソフトウェア開発上の無駄（コスト）を異なるタイプに分類、説明することである

---

#### 論文の著者 #1

# Todd Sedano
### Pivotal
Palo Alto, CA, USA

### Carnegie Mellon University
Silicon Valley Campus

Email: professor@gmail.com

（※ アドレスがやばい）

---

#### 論文の著者 #2

# Paul Ralph
### University of Auckland
Auckland, New Zealand

### University of British Columbia
Vancouver, BC, Canada

Email: paul@paulralph.name

---

#### 論文の著者 #3

# C´ecile P´eraire
### Carnegie Mellon University
#### Electrical and Computer Engineering
Silicon Valley Campus

Moffett Field, CA 94035, USA

Email: cecile.peraire@sv.cmu.edu

---

# 論文の構成

1. INTRODUCTION
2. A BRIEF HISTORY OF LEAN
3. RESEARCH METHOD
4. RESULTS: TYPES OF WASTE IN SOFTWAREENGINEERING
5. COMPARING TO LEAN SOFTWARE DEVELOPMENT
6. RESULTS EVALUATION AND QUALITY CRITERIA
7. CONCLUSION

---

# とあるエンジニアのつらみ

> エンジニア達はめっちゃつらんでるんすよね。あのプロジェクトほんと疲弊するんすよ。。どの問題からやってったらいいのか、わからんのですよ。ていうか、あちこちで依存があってシステムの各レイヤーが無駄に複雑やし、システムに関する知見が足りてないし。。。あと、待ち時間多すぎ。Java のコードビルドするのに 10分でしょ、そんでサーバー起動に 7分。Javascript のテスト実行に 2分。結合テストで 47分。そんで CI（継続的インテグレーション）やるわけですけど、永遠みたいな時間がかかるわけですよ。まじフォーエバー。

> もうね、無駄の総合商社ですよ。

###### _――プロジェクト「Septem」に関わったエンジニア_

---

# There is 無駄 everywhere

---

# 無駄を減らすのってむずかしいっすよね

- 現状維持バイアス
- 謎の流儀
- 伝統芸能
- 慣習的にある悪弊

###### _（そこで Lean!! って話は割愛）_

---

# ９つの無駄タイプ

- どんな無駄があるかを知って
- 社内の共通認識・共通言語をつくり
- ユーザーにとって価値のある工数にしよう！

###### 以降のスライドで色んな無駄を紹介します →→→

---

# タイプ1.
# そもそも仕様や作ろうとしてるサービスが間違ってる

> 誰も求めてない、欲してない、使わない機能（や、最悪の場合プロダクトそのもの）を作ることは、全員の努力や時間を無駄にすることが明白である。この手の無駄はチームのモラル、コードオーナーシップ、そして顧客満足に影響する。

---

# User needs
# V.S.
# Business wants

- 意図だけで作るプロダクトはリスキーでだいたいは無駄に終わる
- ペルソナがフィクションでステレオタイプなユーザー像である
- 検証で誰も欲しいと言ってないのに追加される機能
- クライアントから言われたから実装される仕様

---

# タイプ2.
# 残課題（バックログ）の管理がへぐってる

> 課題管理の運用ミスはよく起こるし、たいてい重要機能の実装遅延やチームの生産性低下を引き起こす。そもそもエンジニアが課題に着手するとき、その課題は古い優先順位だ。管理ミスは重複作業も招く。二人のエンジニアが同種のタスクにとりかかってしまうケースなどが挙げられる。

---

# Finishing features
# V.S.
# Working on too many features simultaneously

- 一度に実装しようとする仕様や機能が多すぎる
- 小さくても良いから「終わらせる」ことよりも「仕様が完成する」ことを優先している
- 優先順位が変わったり、ふわっとした状態でやる仕事はだいたい無駄になる
- 単純で簡単な仕様をとりあえず作るより、立派な機能を実装することを好む傾向がある

---

# Intransigence
# V.S.
# Capricious adjustments

- 「変更に柔軟」であることは、すなわち「変更しない」ことの反対と考えられている
- それはアジャイル開発の信条におけるコアであるとされていた
- しかし「変更に柔軟」であることとは、「変更しない」と「ブレブレ」の中間点である
- 誰かが会員登録プロセスをいじくったりしてると、リリースは遅延する

---

# タイプ3.
# 作り直し

> 新しい情報が得られたことでより

---

- 技術的な近道や頻繁なデッドラインの設定は、技術的負債を生み、作り直しにつながる
- リファクタリングをしなかったり手っ取り早く作ると、その後何週間も作り直すハメになる
- 何が完了なのか明確に定義されていないストーリは、作り直しを生む
- 明確な完了要件が定義されてないと、作り終わった後に指摘が起こったりする

---

# タイプ4.
# 無駄に複雑なソリューション



