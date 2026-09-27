# Opus 5.5 に入れる公式プラグイン — 仕事で効く4つ

📊 [スライド資料はこちら（slides.html）](https://chaaaaarin.github.io/claudecode-channel-20260927-159/slides.html) | 📋 [1枚まとめ資料はこちら（onepager.html）](https://chaaaaarin.github.io/claudecode-channel-20260927-159/onepager.html) | 🎁 [プレゼントはこちら](https://chaaaaarin.github.io/gift-library/cc/ep/159/)

2026年9月22日に Anthropic（アンスロピック）が Claude Opus 5.5（クロード オーパス ごーてんご）を公開し、その翌日には Claude に足せる道具を1か所で探せる「Claude Marketplace（クロード・マーケットプレイス）」も公開しました。Pro・Max・Team プランのアプリでは Opus 5.5 が最初から既定のモデルです。この資料では、その Opus 5.5 に「プラグイン」を入れると何ができるかを初心者向けに噛み砕き、Anthropic が作った4つのプラグイン（Productivity・Marketing・Data・Sales）を、同じ1つの例で試せる形にまとめています。

## TL;DR（まず3行で）

1. **Opus 5.5 は、Opus 5 より速くて安く、実務の評価で Claude の中でいちばん上**。有料プランでは使える量が25%増え、アプリの既定モデルにもなった。
2. **プラグインは、手順書（スキル）・外のサービスとつなぐ口（コネクター）・コマンド・専門の係（エージェント）の詰め合わせ**。有料プランなら追加ボタン1回で入り、入力欄で「/」を打つと使える。チャットや Cowork（コワーク）で使えるのは37個。
3. **最初の1つは、困っている仕事で選ぶ**。前提の説明なら Productivity、告知文なら Marketing、売上の振り返りなら Data、商談のあとなら Sales。Opus 5.5 の強み（書き方のルールを守る・数字をでっち上げにくい 等）がそれぞれ効く。

## 目次

- [そもそも：Opus 5.5 で何が変わった？](#そもそもopus-55-で何が変わった)
- [そもそも：プラグインって何？どう入れる？](#そもそもプラグインって何どう入れる)
- [章1 Productivity：仕事を覚えさせる](#章1-productivity仕事を覚えさせる)
- [章2 Marketing：告知文を書かせる](#章2-marketing告知文を書かせる)
- [章3 Data：売上を分析させる](#章3-data売上を分析させる)
- [章4 Sales：商談をまとめさせる](#章4-sales商談をまとめさせる)
- [章5 自分の仕事に合わせて作り変える](#章5-自分の仕事に合わせて作り変える)
- [章6 入れる前に知っておくこと](#章6-入れる前に知っておくこと)
- [今日からやること（始めるならこの順番）](#今日からやること始めるならこの順番)
- [まとめ：困っている仕事から1つだけ](#まとめ困っている仕事から1つだけ)
- [プレゼント（キットの中身と受け取り方）](#プレゼントキットの中身と受け取り方)
- [動画内で補足する用語](#動画内で補足する用語)

> この資料では、全部の章を同じ例で説明します：**小さな雑貨の会社が、新商品「木のマグカップ」を出した週**。取引先は **カフェ山下様**（都内に2店舗あるカフェのオーナー）です。例はすべて架空です。

---

## そもそも：Opus 5.5 で何が変わった？

- ✅ 2026年9月22日（米国時間）、Claude 公式Xが Opus 5.5 を発表。2026-09-28時点で **2,727万回表示・いいね9.6万**。「ほとんどの仕事で最上位の Fable 5.1 並み、Opus 5 より動かすコストが4割安い」。（[公式X投稿](https://x.com/claudeai/status/2102435511222890900)／[Anthropic「Introducing Claude Opus 5.5」](https://www.anthropic.com/claude-opus-5-5)）
- ✅ Opus 5 と比べて、速い・答えが短く分かりやすい。開発者向けの料金も1トークン（AIが扱う文字のかたまり）あたり20%安く、1つの作業では約40%安い。**Pro・Max・Team プランでは使える量が25%増える**。（[Claude 公式 YouTube「Using Claude Opus 5.5 as your daily driver」](https://www.youtube.com/watch?v=jKRl_CSVxyI)）
- ✅ **Pro・Max・Team プランでは、Claude アプリ（Cowork を含む）と Claude Code の既定モデルが Opus 5.5 に**。（[cat（Anthropic・Claude Code と Cowork 担当）のX投稿](https://x.com/_catwu/status/2102437713781944397)）
- ✅ 44の職種の実務でどれだけ良い仕事をするかの評価（GDPval-AA）で **1846点**。Opus 5 は1708、Fable 5.1 は1735、GPT-6 Astra は1542。（[公式X投稿のベンチマーク表](https://x.com/claudeai/status/2102435517165912464)）
- ⚠️ 業務の流れを自動で回すテスト（AutomationBench）は GPT-6 Astra が少し上（41.4% と 40.0%）。公式も「この水準では点数の差は実際の差の目安になりにくい」と書いています。（[Anthropic「Introducing Claude Opus 5.5」](https://www.anthropic.com/claude-opus-5-5)）
- タイトルの「100倍」は公式の数字ではありません。反応の数も注目度の数字です。

## そもそも：プラグインって何？どう入れる？

- ✅ 起点は Claude 公式X（2026-09-23・米国時間）。2026-09-28時点で **83万回表示・いいね5,647**。反応の数は注目度で、効果の大きさを示す数字ではありません。（[公式X投稿](https://x.com/claudeai/status/2102840851538080172)）
- ✅ マーケットプレイスの棚は3つ：①コネクターとプラグイン ②エージェントと製品（会社が Anthropic と結んだ契約の予算で買うソフト）③サービスパートナー（導入を手伝う会社）。この資料は①の話です。（[Claude Marketplace（日本語）](https://claude.com/ja/marketplace)／[公式ブログ](https://claude.com/blog/claude-marketplace)）

### プラグインは4つの部品の詰め合わせ

| 部品 | 何か | チャット | Cowork・Claude Code |
|---|---|---|---|
| スキル | 仕事の手順書。合う作業のときに Claude が読む | 使える | 使える |
| コマンド | 「/」で呼ぶ、名前の付いた決まった仕事 | 使える | 使える |
| コネクター | Gmail や Slack など、外のサービスとつなぐ口 | 使える | 使える |
| エージェント（係）・フック | 仕事の一部を任せる係／決まったタイミングで動く仕掛け | **動かない** | 使える |

- ✅ プラグインは、スキル・コネクター・サブエージェントを1つにまとめたもの。1つずつ設定しなくても、最初の会話から使える状態になる。（[Claude ヘルプ](https://support.claude.com/en/articles/13837440-use-plugins-in-claude)）
- ✅ 部品ごとに、チャット・Cowork・Claude Code のどこで動くかが違う。（[Claude ドキュメント「Plugin feature support」](https://claude.com/docs/plugins/platform-support)）

### いくつある？

- ✅ 公式ブログは「コネクターとプラグインを合わせて2,000以上」。（[公式ブログ](https://claude.com/blog/claude-marketplace)）
- ✅ プラグイン一覧を「Claude」で絞ると **37個**（全340個。残りはプログラミング用の Claude Code 向け。2026-09-27時点）。（[プラグイン一覧](https://claude.com/ja/marketplace/plugins?works_with=claude)）
- ⚠️ 一覧ページの表示（コネクター850・プラグイン340）と「2,000以上」は数え方がそろっていません。
- ✅ 「公式推奨」の見分け方は、名前の横の「Anthropic認定済み」マーク。Anthropic 製のプラグインは中身が GitHub で公開されています（スター2.5万・2026-09-27）。（[anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins)）

### 対象プランと入れ方

- ✅ **有料プラン（Pro・Max・Team・Enterprise）なら全員使える**。無料プランは対象外。入れたものはアカウントに保存され、チャット・Cowork・Claude Code で使える。（[Claude ヘルプ](https://support.claude.com/en/articles/13837440-use-plugins-in-claude)）
- ✅ 料金は Pro が月20ドル（年払いなら月17ドル相当）、Max が月100ドルから。（[Claude 料金](https://claude.com/pricing)）
- ✅ スマホのチャットでも、入れたプラグインのスキル・コマンド・コネクターが使える。エージェントとフックは Cowork と Claude Code だけで動く。（[Claude ドキュメント「Plugins」](https://claude.com/docs/plugins/overview)）
- ✅ 9月16日から、チャットと Cowork は1つの画面に順次まとまっています。アプリに「Cowork」の切り替えが見当たらない人は、いつものチャット画面で進めてください。（[Claude 公式 YouTube「Claude Cowork and chat are now one Claude」](https://www.youtube.com/watch?v=qMUf-jwSpMo)）

画面の名前は英語で表示されることがあるので、括弧内の英語も目印にしてください。

1. 左のメニューで「カスタマイズ（Customize）」
2. 「プラグイン（Plugins）」のタブを開く
3. 「見つける（Discover）」で一覧を見る
4. 選んで「追加（Add）」を押す

使うときは、入力欄で「/」を打つか「＋」を押すと、プラグインのコマンドが出ます。

| 今週やること | 使うプラグイン |
|---|---|
| 今週やることを、抜けなく並べたい | Productivity（章1） |
| 告知の投稿とメルマガを書きたい | Marketing（章2） |
| 8週分の売上を振り返りたい | Data（章3） |
| カフェ山下様との商談をまとめて返事したい | Sales（章4） |

---

## 章1 Productivity：仕事を覚えさせる

- ✅ Productivity（プロダクティビティ）は、やることリスト・仕事の記憶・一覧の画面で、Claude に仕事を覚えさせるプラグイン。関係者・案件・社内の言葉を覚えて「チャットボットではなく同僚のように」動く、と公式が説明しています。（[Claude Marketplace「Productivity」](https://claude.com/ja/marketplace/plugins/productivity)）

| 打つコマンド | 何が起きるか | いつ使う |
|---|---|---|
| `/start` | やることリスト・記憶・一覧の画面を用意する | 入れた直後に1回 |
| `/update` | 止まっているタスクを洗い出し、覚えていない言葉を確かめる | 毎朝など |
| `/update --comprehensive` | メール・予定・チャットを深く見て、見落としたタスクを探す | 週に1回（つないでいる人向け） |

**Opus 5.5 だと**：作業中の途中経過も、終わったときのまとめも「何をしたか・何が分かったか・何をしてほしいか」をはっきり書く、と公式ガイドにあります。朝の `/update` の報告が読みやすくなります。（[Claude ドキュメント「Prompting Claude Opus 5.5」](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-5-5)）

**メリット**：「山下様の件」だけで何の話か通じる／止まっているタスクを Claude の方から挙げてくる／朝の段取りが `/update` 1回でそろう。

**増える手間・向かない場面**：最初に関係者や案件を教える手間がかかる／メール・予定まで見させるならコネクターを自分でつなぐ／公式ページでは入れる先が Cowork になっていて、チャットでは一部の部品が動かない。

**試し方**：`/start` を打ち、今週やること（新商品の告知・8週分の売上の振り返り・カフェ山下様へのフォロー）と関係者を書いたメモを貼って「これを覚えて」と送る。新しい会話で「山下様の件、どうなってる？」と聞いて通じるか見る。

---

## 章2 Marketing：告知文を書かせる

- ✅ Marketing（マーケティング）は、ブログ・SNS・メルマガ・LP（商品の紹介ページ）・プレスリリースの下書き、キャンペーンの計画、競合の整理、SEO（検索に出やすくする工夫）の点検までを持つプラグイン。（[Claude Marketplace「Marketing」](https://claude.com/ja/marketplace/plugins/marketing)）

| コマンド | 何をする |
|---|---|
| `/draft-content` | 投稿・メルマガ・LPの下書き |
| `/campaign-plan` | キャンペーンの計画と日程 |
| `/brand-review` | 文体のルールに合うか点検 |
| `/competitive-brief` | 競合との違いをまとめる |
| `/performance-report` | 成果のレポート |
| `/seo-audit` | 検索に出やすいか点検 |
| `/email-sequence` | 数回に分けて送るメール |

**Opus 5.5 だと**：✅ 渡した書き方のルールを守り、大事なことを先に書く（公式X・290万回表示）。下の依頼文の【守ること】がそのまま効きます。（[公式X投稿](https://x.com/claudeai/status/2102435529044250670)）

### コピペで使える依頼文

```text
/draft-content
新商品「木のマグカップ」の告知を作ってください。

【材料】
・2,800円（税込）／9月14日発売
・職人が1つずつ削った山桜。食洗機は使えない
・自社サイトと Instagram で販売

【ほしいもの】
1. Instagram の投稿文を3案（それぞれ120字以内）
2. メルマガ1本（件名3案と、本文400字）

【守ること】
・日本語の「です・ます」で書く。絵文字は使わない
・「最高」「日本一」のような、言い切れない言葉は使わない
```

**メリット**：投稿3案とメルマガが1回の依頼でそろう／`/brand-review` で文体のずれを点検できる／計画・下書き・成果レポートを同じ場所で回せる。

**増える手間・向かない場面**：自社の文体を教えないとありきたりな文になりやすい／価格・発売日など事実の確認は自分でやる／コマンド名や例は英語が元なので、日本の媒体に合わせる指示が要る。

---

## 章3 Data：売上を分析させる

- ✅ Data（データ）は、データの中身の確認・分析・グラフ・ダッシュボード（絞り込めるグラフの画面）・人に出す前の点検までを持つプラグイン。会社のデータベース（Snowflake・BigQuery など）につなげば直接集計し、つながなくても表を貼るか CSV・Excel を渡せば分析できる。（[Claude Marketplace「Data」](https://claude.com/ja/marketplace/plugins/data)）
- ✅ Claude 公式の動画では、`/explore-data` で頼むと、進め方の一覧を作って順に片づけ、最後に Excel の表を作る様子が見られます（0:17〜0:41）。（[Claude 公式 YouTube「Cowork and Plugins」](https://www.youtube.com/watch?v=v5IOHK5xFlc)）

| 順番 | コマンド | 何をする |
|---|---|---|
| 1 | `/explore-data` | データの中身と、欠けている所を調べる |
| 2 | `/analyze` | 質問に答える（「落ちている商品は？」） |
| 3 | `/build-dashboard` | 絞り込めるグラフの画面を作る |
| 4 | `/validate` | 人に見せる前に、集計のまちがいや偏った見方を点検 |

**Opus 5.5 だと**：✅ 架空の2社の合併を分析させた公式のテストで、Excel の財務モデルから役員向けの資料までを **Opus 5 の93分 → 63分**、費用は半分で仕上げた（Anthropic の社内テスト1件）。✅ 細かいグラフの数字も、Opus 5 より正確に読む。（[Anthropic「Introducing Claude Opus 5.5」](https://www.anthropic.com/claude-opus-5-5)／[公式ガイド](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-5-5)）

**メリット**：並べ替えやグラフ作りを言葉で頼める／共有できるグラフの画面まで作る／`/validate` で報告の前にまちがいを見つけられる。

**増える手間・向かない場面**：列の意味（どの列が売上か等）は最初に説明が要る／大量のデータは会社のデータベースにつなぐ準備が要る／出た数字は元の表と一度は見比べる／社外秘の表を渡す前に、会社のルールを確認する。

**試し方**：架空の売上表（8週分）を添付し、`/analyze`「新商品の出だしと、落ちている商品を教えて」→ `/build-dashboard`。

---

## 章4 Sales：商談をまとめさせる

- ✅ Sales（セールス）は、どのコマンドも Web 検索と自分が渡した情報だけで動く。顧客管理（CRM）やメールとつなぐと、さらに強くなる。（[Claude Marketplace「Sales」](https://claude.com/ja/marketplace/plugins/sales)）

| コマンド | 何をする |
|---|---|
| `/call-summary` | 商談メモを、やること付きのまとめとお礼メールの下書きにする |
| `/forecast` | 案件の一覧から、良い・普通・悪いの3通りで売上を見込む |
| `/pipeline-review` | 止まっている案件を見つけて、今週やることを出す |

**例（架空）**：「カフェ山下様。1店舗30個くらい／食洗機に入れられるか気にしている／1個2,000円以下なら検討／ロゴの焼き印は？／10月中旬に3店舗目／来週中に見積もりを送る約束」というメモを `/call-summary` に貼ると、まとめ・やること（見積もり・焼き印の確認・サンプル発送）・お礼メールの下書きがそろう、という使い方です。

**Opus 5.5 だと**：✅ Web の写しだけで会社の決算レポートを書かせ、数字と引用を1つずつ照らした公式のテストで、**Opus 5.5 は18回中16回合格**。Fable 5.1 と Opus 5 は1回も合格しなかった（1つでも作り話があれば不合格）。相手の会社を調べる場面で効きます。ただしゼロではないので、約束する数字は自分で確かめます。（[Anthropic「Introducing Claude Opus 5.5」](https://www.anthropic.com/claude-opus-5-5)）

**メリット**：まとめとメールが一度に出る／期限と担当が並ぶので約束の抜けが減る／顧客管理がなくても始められる。

**増える手間・向かない場面**：値段や納期など約束する内容は自分で確かめてから送る／お客さんの名前や内容を渡すので会社のルールを先に確認する／CRM を使う会社はつなぐ設定が別に要る。

---

## 章5 自分の仕事に合わせて作り変える

- ✅ Cowork で、入れたプラグインを開いて右上の「Customize」を押すと、作り変え用の作業が開き、Claude と会話しながらスキルやコネクターを自分のやり方に合わせられる。（[Claude ヘルプ](https://support.claude.com/en/articles/13837440-use-plugins-in-claude)）
- ✅ Cowork で `/setup-claude` を打つと、自分に合うプラグインをすすめてくれる。自作は、繰り返す作業を1つスキルにするところから。（[Claude Academy「Plugins」](https://academy.claude.com/courses/introduction-to-claude-cowork/plugins-cowork-as-a-specialist)）
- ✅ ゼロから作るなら「カスタマイズ → プラグイン → 追加 → Create with Claude」。（[Claude ドキュメント「Plugins」](https://claude.com/docs/plugins/overview)）

### Opus 5.5 の公式のコツ：つないだら、先に見て回らせる

- ✅ Opus 5.5 はすぐ作業に取りかかる。メール・資料・表・顧客の記録をつないでいて、頼み方がざっくりしているときは、手を動かす前に関係する情報を見させる一文を入れると、公式のテストで正解が目に見えて増えた。（[Claude ドキュメント「Prompting Claude Opus 5.5」](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-5-5)）

公式の文（英語）を日本語に直したもの。公式はシステムプロンプト（前提の指示）用として紹介しているので、Customize で覚えさせるか、依頼の最初に書きます。

```text
作業を始める前に、つないでいるアプリの中で
関係しそうなメール・資料・表のタブ・記録を
一覧にして開き、見つけたことを使ってください。
依頼に書いていないものも含めて探してください。
```

**試し方**：Marketing を開いて「Customize」→「です・ます、絵文字なし、1文40字まで」と上の一文を伝える → 章2の依頼文をもう一度送り、口調がそろったか見比べる。

---

## 章6 入れる前に知っておくこと

### 中身は米国の仕事が前提

今日の4つ以外の公式プラグインを例に見ます。

- ✅ 小さな会社向けの Small Business（スモールビジネス）には43の仕事の流れが入っていて、承認するまで送信・投稿・支払いはしない（承認モード）。（[Claude Marketplace「Small Business」](https://claude.com/ja/marketplace/plugins/small-business)）
- ✅ ただし、つなげるのは米国で広く使われる会計・給与のサービスが中心で、freee・マネーフォワードは公式の接続先の一覧にありません。（[GitHub の接続先一覧](https://github.com/anthropics/knowledge-work-plugins/blob/main/small-business/.mcp.json)）
- コマンド名は英語です。「/」で一覧から選べば迷いません。

### どこから入れるか

- ✅ 公式の一覧（ディレクトリ）に載るプラグインは、毎回の版で自動の検査と安全スキャンを受け、新しく載るものは人も審査する。自分で URL やファイルから足したものは審査の対象外なので、信頼できる相手のものだけにする。（[Claude ドキュメント「Plugins」](https://claude.com/docs/plugins/overview)）
- ✅ パソコンの中で動く部品（ローカルのMCPサーバー）は、他のアプリと同じ権限で動く（Cowork・Claude Code のとき）。（[Claude ヘルプ](https://support.claude.com/en/articles/13837440-use-plugins-in-claude)）

### Opus 5.5 でも、送る・払うの前は人が見る

- ✅ Opus 5.5 は、取り返しのつかない操作や任された範囲の外の行動をしにくく、外から紛れ込む指示（プロンプトインジェクション）にも Opus 5 より強い。（[Anthropic「Introducing Claude Opus 5.5」](https://www.anthropic.com/claude-opus-5-5)）
- ✅ それでも、元に戻せない操作や危ない操作は自分で確認する手順を残す。先に見て回らせるなら、信用できない文書は探す場所に入れない、と公式ガイドにあります。（[公式ガイド](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-5-5)）

### 入れただけでは、外のサービスにつながらない

- ✅ プラグインを開いて「Connectors」のタブを見ると、つなぐ先が「Connected（つながっている）」「Not connected（ログインが要る）」「Not added（まだ入っていない）」のどれかで表示される。つなぐ先のサービスに別の有料プランが要ることもある。（[Claude ドキュメント「Plugins」](https://claude.com/docs/plugins/overview)）

### 合わなければ、止めて外す

- ✅ 入れたら実際の仕事で1回試し、役に立たなければ「Disable plugin」でオフ、メニューの「Remove」で外せる。（[Claude ドキュメント「Plugins」](https://claude.com/docs/plugins/overview)）

---

## 今日からやること（始めるならこの順番）

1. 有料プランか確かめる（無料プランは対象外）。送信ボタンの横のモデルが「Opus 5.5」になっているかも見る
2. 「カスタマイズ → プラグイン → 見つける」で、名前の横の「Anthropic認定済み」マークを見る
3. 今いちばん困っている仕事のプラグインを1つだけ追加する
4. 入力欄で「/」を打ち、最初のコマンドを1回試す（下の表）
5. 合えば「Customize」で自分の文体・社内の言葉を教える。合わなければオフにする

## まとめ：困っている仕事から1つだけ

| 困っていること | 入れるもの | 最初に打つ一言 | Opus 5.5 の強み |
|---|---|---|---|
| 毎回、前提を説明している | Productivity | `/start` | 報告がひと目で分かる |
| 告知やメルマガに時間がかかる | Marketing | `/draft-content` | 書き方のルールを守る |
| 売上の振り返りが後回し | Data | `/analyze` | Excel と資料が早い |
| 商談のあとのメールが遅れる | Sales | `/call-summary` | 数字をでっち上げにくい |
| 自分のやり方に合わない | 入れたもの | 右上の「Customize」 | 先に見て回る一文 |

有料プランなら、Opus 5.5 は最初から使えます。まずは困っている1行から。

## プレゼント（キットの中身と受け取り方）

この動画を見てくださった方に、次の3つをお配りしています。

1. **神プラグイン4つを1回で入れて、今日から Opus 5.5 に仕事を任せられる導入ファイル**：Claude Code に渡すだけで4つが入る導入文と、アプリで入れる人向けのチェックリスト
2. **公式プラグイン4つが入れたその日から仕事で回り出す、実務プロンプト20選**：Productivity・Marketing・Data・Sales に5本ずつ、そのまま貼れる依頼文
3. **AI学習アプリ「HIROGERU」視聴者クーポン**：ダウンロード手順つき

受け取りは [プレゼント図書館のこの回のページ](https://chaaaaarin.github.io/gift-library/cc/ep/159/) から。コピーまたはダウンロードでそのまま使えます。

## 動画内で補足する用語

| 用語 | 読み | ひとことで |
|---|---|---|
| Anthropic | アンスロピック | Claude を作っている会社 |
| Opus 5.5 | オーパス ごーてんご | 2026年9月22日に出た Claude のモデル。Pro・Max・Team のアプリの既定 |
| Fable 5.1 | フェイブル ごーてんいち | Claude の最上位のモデル |
| GDPval-AA | ジーディーピーバル | 44の職種の実務の出来を比べる評価 |
| エフォート | — | 答える前にどれだけ考えるかの設定。Opus 5.5 の既定は Medium |
| Claude Marketplace | クロード・マーケットプレイス | Claude に足せる道具を探せる公式の場所（2026年9月23日公開） |
| プラグイン | — | スキル・コネクター・コマンド・エージェントの詰め合わせ |
| スキル | — | 仕事の手順書。合う作業のときに Claude が読む |
| コネクター | — | Gmail や Slack など、外のサービスとつなぐ口 |
| MCP | エムシーピー | AI と外のサービスをつなぐ共通の決まり。コネクターの中身 |
| エージェント（サブエージェント） | — | 仕事の一部を任せる専門の係 |
| フック | — | 決まったタイミングで自動で動く仕掛け |
| Cowork | コワーク | Claude のデスクトップアプリで、作業を任せるモード |
| Claude Code | クロードコード | プログラミング向けの Claude |
| Productivity | プロダクティビティ | 仕事の記憶とやることリストのプラグイン |
| ダッシュボード | — | 絞り込めるグラフの画面 |
| CRM | シーアールエム | 顧客管理のサービス |
| SEO | エスイーオー | 検索に出やすくする工夫 |
| LP | エルピー | 商品の紹介ページ（ランディングページ） |
