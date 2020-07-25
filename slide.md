## Kaigi on Rails new 
- - -

## Ruby の開発について

---

#### 自己紹介
- - -

* 名前：osyo
* Twitter : [@pink_bangbi](https://twitter.com/pink_bangbi)
* github  : [osyo-manga](https://github.com/osyo-manga)
* ブログ  : [Secret Garden(Instrumental)](http://secret-garden.hatenablog.com)
* Rails 歴 約2年半           <!-- .element: class="fragment" -->
* 趣味で Ruby にパッチを投げたりしてます           <!-- .element: class="fragment" -->
* Ruby で一番好きな機能は Refinements です           <!-- .element: class="fragment" -->

---


#### 投げたパッチ
- - -

* Refinements の緩和案                            <!-- .element: class="fragment" -->
    * [`#public_send`](https://bugs.ruby-lang.org/issues/15326)
    * [`#respond_to?`](https://bugs.ruby-lang.org/issues/15327)
    * [`#method`, `#instance_method`](https://bugs.ruby-lang.org/issues/15373)
    * [ブロック引数で `&:hoge` 渡した場合](https://bugs.ruby-lang.org/issues/15114)
* Time にメソッドを追加                            <!-- .element: class="fragment" -->
    * [`Time#floor`](https://bugs.ruby-lang.org/issues/15653) / [`Time#ceil`](https://bugs.ruby-lang.org/issues/15772)
* RubyVM::AbstractSyntaxTree のバグ修正                            <!-- .element: class="fragment" -->
    * [RubyVM::AbstractSyntaxTree.parse has the same result on `proc { |a| }` and `proc { |a,| }`](https://bugs.ruby-lang.org/issues/17015)
    * [`RubyVM::AbstractSyntaxTree.parse("struct.field += foo")` has no operator](https://bugs.ruby-lang.org/issues/17013)

---

## 今日話すこと
- - -

### Ruby はどうやって開発されているのかざっくり話してみる

---

#### Ruby の議論はどこで行われているのか
- - -

* [bugs.ruby](https://bugs.ruby-lang.org/)でチケット管理してる
* このサイトでバグ報告をしたり機能の提案を行ったりしている
* [ここにチケット一覧](https://bugs.ruby-lang.org/projects/ruby-master/issues)が載っている

---

#### 開発者会議
- - -

* 毎月 Ruby コミッタが集まって議論している
    * 今月の議題とか https://bugs.ruby-lang.org/issues/17019
    * 議事録とか https://github.com/ruby/dev-meeting-log/blob/master/DevelopersMeeting20200720Japan.md
* 議論してほしい議題があればここに追加する
* ここで議論が行われ、まつもとさんが承認すれば次期 Ruby に組み込まれる
  
---

#### Ruby の github リポジトリ
- - -

* Ruby は git で開発を行われている
* github のミラーもある
    * https://github.com/ruby/ruby
* pull request は投げられてくるが議論は基本的に bugs.ruby で行っている

---


#### Ruby を開発したい方は
- - -

* [Ruby Hack Challenge](https://rhc.connpass.com/) というイベントを不定期でやってる
    * 最近はお休み気味
    * [Hamada.rb](https://hamadarb.connpass.com/event/179928/) でも行っている
* [ここに書いてある資料](https://github.com/ko1/rubyhackchallenge/tree/master/JA)を読むと便利
    * Ruby 本体のビルドの仕方や Ruby にメソッドを追加する演習、デバッグの仕方などが書いてある
    * これを読めば簡単な機能追加などは行える
    * ただし、最低限の C言語の知識は必要になってくるので先にそっちを勉強する必要があるかも

---

#### Ruby に機能が追加されるまでの流れ
- - -

1. Ruby に必要か考える            <!-- .element: class="fragment" -->
1. パッチを書く            <!-- .element: class="fragment" -->
    * なくてもいいけどあるとよりよい
1. bugs.ruby にチケットをつくる            <!-- .element: class="fragment" -->
1. 開発者会議の議題で取り上げてもらう            <!-- .element: class="fragment" -->
    * 議論してもらうようにコメントする必要がある
1. まつもとさんが承認すれば言えば取り込まれる            <!-- .element: class="fragment" -->
    * パッチがあればそのままマージされる
    * なければ誰かがよしなにパッチを書く
    * 問題があれば修正する
    * だめって言われたら却下される

---

#### Ruby に機能を取り込まれやすくるコツ
- - -

* 現行の Ruby との整合性
    * 非互換な機能はやっぱり取り込まれづらい
* ユースケースが具体的
* パッチ(PR)がある
* まつもとさんを説得できるだけの材料がある


---

#### まとめ
- - -

* Ruby は bugs.ruby というサイトで管理されている           <!-- .element: class="fragment" -->
* bugs.ruby で追加する機能の議論やバグ報告を行われている           <!-- .element: class="fragment" -->
* 日本語でも OK           <!-- .element: class="fragment" -->
* bugs.ruby の ML に登録しておくとチケットの内容とかがメール通知されるので便利           <!-- .element: class="fragment" -->

---


## ご清聴
## ありがとうございました

