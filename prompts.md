# search-book
検索本（仮）のメタプロンプト、参考URLを集めたレポジトリです。
プロンプトについては、https://chatgpt.com/ にアクセスして、入力して使ってみてください。
# まえがき

# 第1部　臨床疑問の調べ方

## コラム：（本書における）ChatGPTの使い方
### ライムプロンプト
```
あなたは今からラップのライムを生成するAIアシスタントとして振る舞ってください。ユーザーからの入力に対して、以下の手順でライムを生成します。
ユーザーからの入力単語やフレーズを受け取ったら、その言葉に対する日本語ライムを3つ生成してください。
生成したライムは、入力された言葉と同じ音で終わるか、または類似した発音になるようにしてください。
ライムは、意味的にもユーザー入力と関連性があるものを生成するようにしてください。
ライムは、できるだけユーモアやウィットに富んだ表現になるよう心がけてください。
生成したライムは、以下のフォーマットで出力してください。
ユーザー入力: [入力単語やフレーズ]
ライム1: [生成されたライム1]
ライム2: [生成されたライム2] 
ライム3: [生成されたライム3]
ユーザーからの新たな入力があるまで、このプロセスを繰り返します。
ユーザーが明示的に終了を求めるまで、ライム生成を続けてください。
理解したらyesとだけ答えてください
```
[入力サンプル](https://chat.openai.com/share/063c80fe-e9e6-4230-9f62-07f89d31aec0)

[ライムGPT](https://chatgpt.com/g/g-FVlmC0nxJ-raimugpts)

###
[慢性期の肺線維症の治療は？:ChatGPTの履歴](https://chat.openai.com/share/85481595-9705-4b26-818d-242b103cc40b)

## 1　臨床疑問の分類
### 疑問の分類プロンプト
```
#order
あなたはプロの疫学者です。
#疑問の分類
最初に、クリニカルクエッションがforeground question (2つ以上の要素の組み合わせで成り立つ、臨床判断に使う)なのか、background question (1つの要素に対する漠然とした疑問)なのかを判断してフィードバックをしてください。
#出力例
質問例1: 高血圧の治療にはどんな薬がありますか？
→あなたの疑問はbackground questionです。
質問例2: 高血圧の患者に対して、ACE阻害薬とカルシウム拮抗薬のどちらが心血管イベントを予防するのにより有効でしょうか？
→あなたの疑問はforeground questionです。
理解したらyesとだけ答えてください。
```

## 2　EBMの5つのステップ

## 3　Background questionの扱い方
[医学英語でPubMed検索GPTs](https://chatgpt.com/g/g-3nbgws7r9)
- ChatGPTのページではGoogleやSemantic scholarのURLは表示させることはできても、踏めないという仕様なのでPubMedへの検索リンクにしてますが、もちろん表示されたキーワードで他のデータベースで検索しても大丈夫です。

## 4　二次文献を読もう
- [UpToDate](https://www.uptodate.com/login)
- [DynaMed Plus](https://www.dynamed.com/)
- [Medscape Reference](https://reference.medscape.com/)

## 5　ガイドラインとは？ 
- [ARDS診療ガイドライン2016](https://www.jrs.or.jp/publication/jrs_guidelines/20161004153330.html)
- [ARDS診療ガイドライン2021](https://www.jsicm.org/publication/pdf/220728JSICM_ihardsg.pdf)

## 6　Background questionの検索具体例
- [perplexityの検索例](https://www.perplexity.ai/search/Gi6KTLoXSFe4xKOS.zlB8g)

## 7　Foreground questionの分類と構造化
- [臨床疑問の構造化GPTs](https://chatgpt.com/g/g-6ZRDanfBU-lin-chuang-yi-wen-nogou-zao-hua-gpts)


## 8　エビデンスのピラミッドから系統的レビューへ
- [Cochrane Library:質の高いシステマティックレビュー](https://www.cochranelibrary.com/)
- [Epidtemonikos:システマティックレビュー](https://www.epistemonikos.org/)
- [PubMed Clinical Queries:雑多](https://pubmed.ncbi.nlm.nih.gov/clinical/)
- [Trip:各国のガイドライン](https://www.tripdatabase.com/)
  
## 9　治療の疑問に関する系統的レビューの読み方
- [Angiotensin converting enzyme (ACE) inhibitors versus angiotensin receptor blockers for primary hypertension](https://www.cochranelibrary.com/cdsr/doi/10.1002/14651858.CD009096.pub2/full)
- [Glibenclamide, metformin, and insulin for the treatment of gestational diabetes: a systematic review and meta-analysis](https://www.bmj.com/content/350/bmj.h102.long)
- 『医学論文の読み方 2.0: 論文を批判的に吟味し臨床適用するための Letter の書き方』[中外医学社](https://www.chugaiigaku.jp/item/detail.php?id=3757) [Amazon](https://www.amazon.co.jp/dp/4498148142)

## コラム：AIを使った検索結果の読み方
### 生成AIを使った検索ツールリスト
- [Elicit](https://elicit.com/)
- [consensus](https://consensus.app/)
- [ScholarAI](https://scholarai.io/)
- [txyz](https://www.txyz.ai/)  
どれが特別優秀ということはないです。毎月のようにシステム面での改善が行われているので、自分が好きなインターフェースのものを使ったらいいのではないでしょうか。

## 10　検査の有効性に関する疑問
- [The closed eyes sign: an aid to diagnosing non-specific abdominal pain.](https://www.bmj.com/content/297/6652/837)
- [論文を読んで感度、特異度の計算:ChatGPTの履歴](https://chatgpt.com/share/08844cf9-2af4-40f8-a94f-0817ca090b5e)

## 11　検査の有効性に関する疑問の調べ方

## 12　割合，曝露に関する疑問と一次研究論文

## 13　予測指標の探し方と使い方
- 『診断研究の方法論 ー診断学のエビデンスの読み方・作り方ー』 [日本医事新報社](https://www.jmedj.co.jp/book/search/detail.php?id=2197) [Amazon](https://www.amazon.co.jp/dp/4784959580)　
- [TRIPOD+AI statement](https://www.bmj.com/content/385/bmj-2023-078378)
- [予測モデルワークシート](https://github.com/youkiti/search-book/blob/main/prediction-model-worksheet.txt)


### コラム1●予測指標の未来とAI

### コラム2●未来の系統的レビュー

## 14　適用する
- [Step 4 GPTs](https://chatgpt.com/g/g-QHd1qNInh-step-4-gpts)
  
## 15　振り返る
- [振り返りGPTs](https://chatgpt.com/g/g-eog0VWP6A-zhen-rifan-rigpts)
  
### コラム3●Google—based medicineの可能性

# 第2部　症例報告のための調べ方

## 1　症例報告をするために　「一つ新しい」ロジックを作る

## 2　「一つ新しい」を証明するための検索方法＝系統的検索

## 3　症例報告のための検索　実践編

# おわりに

# 謝辞

# 索引
