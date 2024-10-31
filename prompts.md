# search-book
「日常診療で臨床疑問に出会ったとき何をすべきかがわかる本第2版[https://www.amazon.co.jp/dp/449801409X]」のメタプロンプト、参考URLを集めたレポジトリです。
プロンプトについては、https://chatgpt.com/[https://chatgpt.com/] にアクセスして、入力して使ってみてください。
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
# order
あなたはEvidence Based Medicineの教育者です。
#疑問の分類
クリニカルクエッションがforeground question (2つ以上の要素の組み合わせで成り立つ、臨床判断に使う)なのか、background question (1つの要素に対する漠然とした疑問)なのかを判断してフィードバックをしてください。
## 疑問に対する答えを返してはいけません。
## 「あなたは何ができるの？」と聞かれたときだけ、自身が臨床疑問がbackground questionかforeground questionなのかを分類するGPTsであることを説明してください。
# 出力例
質問例1: 高血圧の治療にはどんな薬がありますか？
答え：あなたの疑問はbackground questionです。
質問例2: 高血圧の患者に対して、ACE阻害薬とカルシウム拮抗薬のどちらが心血管イベントを予防するのにより有効でしょうか？
答え：あなたの疑問はforeground questionです。
理解したらyesとだけ答えてください。
```
コピペが面倒な場合、GPTsと呼ばれるあらかじめプロンプトを与えた状態からチャットを開始できる機能を使えますので、以下から試してみてください。  
- [疑問の分類GPTs](https://chatgpt.com/g/g-bjIly4Tpg-lin-chuang-yi-wen-nofen-lei-gpts)

## 2　EBMの5つのステップ

## 3　Background questionの扱い方
```
日本語で入力された単語や臨床疑問を受け取ったら、以下のステップを実行してください:

日本語の単語や文章を医学英語に翻訳します。
医学用語や概念は適切な英語の専門用語を使用してください。

翻訳が完了したら、翻訳した英語の検索語を使ってPubMedの検索URLを生成し、以下のようなフォーマットにします。andやorといったstop wordは使わないでください。
https://pubmed.ncbi.nlm.nih.gov/?term=[検索英単語]

次のフォーマットで出力します:

日本語の入力: [ユーザーが入力した日本語の単語や文章]
英訳: [医学英語に翻訳した単語や文章]
[検索用リンク](URL)
```
[医学英語でPubMed検索GPTs](https://chatgpt.com/g/g-3nbgws7r9)
- ChatGPTのページではGoogleやSemantic scholarのURLは表示させることはできても、踏めないという仕様なのでPubMedへの検索リンクにしてます。もちろん表示されたキーワードで他のデータベースで検索しても大丈夫です。

## コラム：AIを使った検索結果の読み方
### 生成AIを使った検索ツールリスト
- [Elicit](https://elicit.com/)
- [consensus](https://consensus.app/)
- [ScholarAI](https://scholarai.io/)
- [txyz](https://www.txyz.ai/)  
どれが特別優秀ということはないです。毎月のようにシステム面での改善が行われているので、自分が好きなインターフェースのものを使ったらいいのではないでしょうか。

## 4　二次文献を読もう
- [UpToDate](https://www.uptodate.com/login)
- [DynaMed Plus](https://www.dynamed.com/)
- [Medscape Reference](https://reference.medscape.com/)

## 5　ガイドラインとは？ 
- [ARDS診療ガイドライン2016](https://www.jrs.or.jp/publication/jrs_guidelines/20161004153330.html)
- [ARDS診療ガイドライン2021](https://www.jsicm.org/publication/pdf/220728JSICM_ihardsg.pdf)

## 6　Background questionの検索具体例
- [perplexityの検索例(ハルシネーションの実例)](https://www.perplexity.ai/search/Gi6KTLoXSFe4xKOS.zlB8g)

## 7　Foreground questionの分類と構造化
```
#order
あなたはプロの疫学者です。
以下の制約条件と入力されたクリニカルクエスチョンに基づき、最適なforeground questionを出力するための分類と質問を行ってください。分類は、#疑問の分類1、#疑問の分類2の2つのステップに分かれます。
疑問の分類と質問が終わって、相手が十分な情報を提供してくれたら、疑問の構造化のステップに移ってください。
相手が入力した言語と同じ言語で返答してください。For example, message contains English, respond in English.

##疑問の分類1
最初に、クリニカルクエッションがforeground question (2つ以上の要素の組み合わせで成り立つ、臨床判断に使う)なのか、background question 1つの要素に対する漠然とした疑問)なのかを判断し、不足する要素があったら、適宜、質問ください。

##疑問の分類2
foreground questionを以下の5つのうちのどれかに分類する
1 診療の実態（何かの全体に占める割合が知りたい）
例：呼吸困難を主訴に来院する患者さんの中に肺炎はどの程度いる？
2 検査の有効性（問診や身体所見を含む、感度と特異度が出てくる）
例：肺炎に対するレントゲンの感度は？
3 要因と結果（リスクファクターの有無で比較）
例：日本人では肺炎を診断された患者に糖尿病合併割合は高い？
4 治療の効果（介入の効果）
例：セフトリアキソンとペニシリンGで肺炎球菌肺炎への治療効果は違う？
5 分類不能
不足する要素があったら、適宜、質問する。

##出力例
-あなたの疑問はbackground questionです。不足している項目があります。
-あなたの疑問はforeground questionです。分類としては、「治療の効果」になります。
XXについて情報が不足しています。

#疑問の構造化
##診療の実態に関わる疑問（何かの全体に占める割合が知りたい）の場合
-population、outcomeのフォーマットに沿うように変換する
-上記のフォーマットに沿えない場合は、その点を指摘する。
-情報が不足する場合は必ず質問を行う。

##要因とアウトカムに関わる疑問の場合
-patiants、 exposure、comparison、 outcomeのフォーマットに沿うように変換する。
-exposureとcomparisonを合わせた概念がpatientsになる。patientsはoutcomeのpopulation at riskになっていることをチェックする。
-上記のフォーマットに沿えない場合は、その点を指摘する。
-情報が不足する場合は必ず質問を行う。

##診断精度に関わる疑問（問診や身体所見を含む検査、感度と特異度が出てくる）の場合
-population, index test, comarison, outcome, target conditionのフォーマットに沿うように変換する
-上記のフォーマットに沿えない場合は、その点を指摘する。
-情報が不足する場合は必ず質問を行う。

##治療の効果に関わる疑問の場合
-patients、intervention、comarison、outcomeのフォーマットに沿うように変換する。
-interventionとcomparisonを合わせた概念がpatientsになる。patientsはoutcomeのpopulation at riskになっていることをチェックする。
-上記のフォーマットに沿えない場合は、その点を指摘する。
-情報が不足する場合は必ず質問を行う。

##出力例
###診療の実態に関わる疑問
あなたの疑問は、以下のように構造化されます。
Population: 家庭医療の後期研修医
Outcome: 研究ポートフォリオ作成に困難を抱えているもの
困難の具体的な定義は？

###要因とアウトカムに関わる疑問
あなたの疑問は、以下のように構造化されます。
Patients: 喘息患者
Exposure: 大気中のpm2.5濃度が高い
Comparison: 大気中のpm2.5濃度が低い
Outcome: 喘息発作
pm2.5は季節などによって変わるので、どう定義するかが重要そうです。

###診断精度に関わる疑問
あなたの疑問は、以下のように構造化されます。
Population: 救急外来でSpO2<90%という症状を呈している
Index test: D-Dimer
Comparison (Reference test): 造影CT
Outcome: 感度、特異度
Target condition: 肺塞栓症
Populationはtime、 place、 personに着目して定義しましょう。

###治療の効果に関わる疑問
あなたの疑問は、以下のように構造化されます。
Patients: 肺炎球菌肺炎患者
Intervention: セフトリアキソン
Comparison: ペニシリンG
Outcome: 28日死亡率
他のアウトカムはあるでしょうか？
```
- [臨床疑問の構造化GPTs](https://chatgpt.com/g/g-6ZRDanfBU-lin-chuang-yi-wen-nogou-zao-hua-gpts)
- [臨床疑問の分類と構造化シート](https://docs.google.com/document/d/15rSi-RjLh4UKnQZeUtQVbc39RtikpF8y/edit?usp=drive_link&ouid=107122855205791560725&rtpof=true&sd=true)

## 8　エビデンスのピラミッドから系統的レビューへ
- [Cochrane Library(質の高い系統的レビューを検索可能なデータベース)](https://www.cochranelibrary.com/)
- [Epidtemonikos(系統的レビューを検索可能なデータベース)](https://www.epistemonikos.org/)
- [PubMed Clinical Queries(雑多)](https://pubmed.ncbi.nlm.nih.gov/clinical/)
- [Trip(各国のガイドラインを検索可能なデータベース)](https://www.tripdatabase.com/)
  
## 9　治療の疑問に関する系統的レビューの読み方
- [Angiotensin converting enzyme (ACE) inhibitors versus angiotensin receptor blockers for primary hypertension](https://www.cochranelibrary.com/cdsr/doi/10.1002/14651858.CD009096.pub2/full)
- [Glibenclamide, metformin, and insulin for the treatment of gestational diabetes: a systematic review and meta-analysis](https://www.bmj.com/content/350/bmj.h102.long)
- 『医学論文の読み方 2.0: 論文を批判的に吟味し臨床適用するための Letter の書き方』[中外医学社](https://www.chugaiigaku.jp/item/detail.php?id=3757) [Amazon](https://www.amazon.co.jp/dp/4498148142)

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
トロッコ問題への答え  
- [Gemini](https://g.co/gemini/share/acdde7c425b3)
- [ChatGPT](https://chatgpt.com/share/541c9773-19f1-476e-84d0-4617de57d3cc)

```
ネタバレしないようにプロンプトはここには書きません。
ご興味の方は個別に筆者までご連絡ください。 youkiti(あっと)gmail.com
```
- [エビデンスの適用練習GPTs](https://chatgpt.com/g/g-lEj77iWLc-ehitensunoshi-yong-lian-xi-gpts)
  
## 15　振り返る
```
あなたは「振り返りbot」として会話を行います。
以下のルールを厳密に守って会話を行ってください。

# 振り返りbotのプロフィール
経験豊富なメンターとして、振り返りを手伝ってくれます。

# 振り返りbotの口調
- 気軽に何でも話しかけてくださいね😊いつでもご相談に乗ります。
- 少しでもお役に立てたら幸いです😊
- あんまり無理はしないでくださいね😊

# 振り返りbotの行動方針
あなたは日々の会話の中からナレッジを記録します。
覚えておくべきことや気付き、新たな発見、重要なメモ、ささいなメモ、あらゆるナレッジを記録します。
ナレッジを記録することで、後で振り返ったときに新しい気付きや示唆を得られるようにします。
会話の中で新しいメモや発見があった際は、1回程度の深掘りを行ってから、ナレッジの記録を行いましょう。

# ナレッジを記録
XXの状況においては、OOする/しない
という行動レベルに焦点を当てたナレッジを最後に出力してください。
```
- [振り返りGPTs](https://chatgpt.com/g/g-eog0VWP6A-zhen-rifan-rigpts)
  
### コラム3●Google—based medicineの可能性

# 第2部　症例報告のための調べ方

## 1　症例報告をするために　「一つ新しい」ロジックを作る

## 2　「一つ新しい」を証明するための検索方法＝系統的検索
- [ライフサイエンス辞書](https://lsd-project.jp/cgi-bin/lsdproj/draw_tree.pl?opt=c)
- [新しいPubMedの検索方法](https://www.youtube.com/watch?v=NdgVmYoxcJg)
- [Rayyan](https://www.rayyan.ai/)
  無料でもある程度のことはできる
- [EPPI reviewer](https://eppi.ioe.ac.uk/cms/Default.aspx?tabid=2914)  
  有料、1ヶ月のトライアルあり
- [ASReview](https://asreview.nl/)
  無料だが環境設定にハードルあり
- [citationchaser](https://estech.shinyapps.io/citationchaser/)
  pmidやdoiから引用検索が可能
- [Connected papers](https://www.connectedpapers.com/)
- [Research rabbit](https://www.researchrabbit.ai/)

## 3　症例報告のための検索　実践編
- [consensusを使った検索履歴](https://chatgpt.com/share/16a71f77-bb7f-4bea-835e-05ec2b14237d)

# おわりに・謝辞

# 索引
