# 情報処理学会全国大会の非公式LaTeXテンプレート

毎年3月に開催されている「[情報処理学会全国大会](https://www.ipsj.or.jp/event/national_conv/national-conv.html)」の原稿テンプレートがWord形式しか公開されていないため，LaTeXテンプレートを作成しました（非公式）．

なお，本テンプレートは令和5年度（2023年度）の公式テンプレート（Word）にほぼ準拠しています．

## 想定環境
- オンラインLaTeXエディタ[Overleaf](https://ja.overleaf.com/)で使用することを想定していますが，[TeX Live](https://texwiki.texjp.org/?TeX%20Live)でも利用できると思います（未確認）．
- upLaTeXおよびdvipdfmxを利用してPDFを生成することを想定しています．pLaTeXなど異なるコマンドを使う場合は，`latexmkrc`ファイルを適宜編集してください．

## 原稿レイアウトの設定
下記の項目については，公式テンプレートで指定された値を`ipsj-zenkoku.sty`で設定しています．
| 設定項目 | 設定値 |
| :--- | :--- |
| 上マージン | 30mm |
| 下マージン | 25mm |
| 左マージン | 20mm |
| 右マージン | 20mm |
| カラム間マージン | 7mm |

## フォントサイズ・行送りの設定
下記の項目については，公式テンプレートで指定された値を基準として`ipsj-zenkoku.sty`で設定しています．
| 設定項目 | フォントサイズ |
| :--- | :--- |
| 和文表題 | 16pt |
| 和文著者名・所属 | 10pt |
| 英文表題 | 9pt |
| 英文著者名・所属 | 9pt |
| 章タイトル | 10pt |
| 本文 | 10pt |
| 参考文献 | 8pt |

なお，本文のフォントサイズと行送りについては，公式テンプレートで指定された値を`ipsj-zenkoku-template.tex`内の下記の場所で設定しています．
| 設定項目 | 設定場所 |
| :--- | :--- |
| フォントサイズ | `\documentclass`のオプション |
| 和文著者名・所属 | `\maketitle`の直後 |

## オリジナルマクロ
下記のマクロを`ipsj-zenkoku.sty`で定義しています．`\figref`と`\tabref`はIPSJ論文誌のLaTeXスタイルと同じ使い方です．
| マクロ | 用途 |
| :--- | :--- |
| `\DAG{n}` | 短剣符．著者の所属を複数記載する場合に，著者名および所属の前につけます．`n`に著者番号を指定します． |
| `\figref{xxx}` | 本文で図を参照します．`xxx`に図のラベルを指定すると，`図1`のように出力されます． |
| `\tabref{yyy}` | 本文で表を参照します．`yyy`に表のラベルを指定すると，`表1`のように出力されます． |

## バグを見つけた場合
issueやpull requestで報告をお願いします．また，改善案がありましたら，issueでご提案いただければ幸いです．

## 免責事項
本テンプレートは，公式のWordテンプレートで指定されている余白やフォントサイズなどを，可能な限り準拠してスタイルを調整していますが，完全に一致している保証はありません．本テンプレートを用いることで生じた損害等の一切の責任を負いかねますので，ご了承下さい．