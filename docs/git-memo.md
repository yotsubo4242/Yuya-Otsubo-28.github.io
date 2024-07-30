---
layout: page
title: "git memo"
permalink: /docs/git-memo
---

# ソフトウェア工学

## 講義内容

| 講義回       | 内容                   |
|:-------------|:---------------------:|
| 第１回~第３回 | [ソフトウェア工学概論](#1-ソフトウェア工学概論)    |
| 第４回~第７回 | [プロジェクトマネジメント](#2-プロジェクトマネジメント) |
| 第８回 　　　 | [UML](#3-uml)                    |
| 第９回 　　　 | [コーディング](#4-コーディング)            |
| 第10回~第14回 | [Git/GitHub](#5-git)             |

## 1. ソフトウェア工学概論

### 1-a. ソフトウェア工学とは？
#### ソフトウェア : 「情報を」扱うプロダクトそのもの、プロダクトを提供する手段。
	<ソフトウェアの定義>
	1. 実行されることによって必要な特性、機能、性能を提供する命令語群（コンピュータプログラム）。
	2. プログラムが適切に情報を扱うことを可能とするデータ構造。
	3. プログラムの操作や使用法を記述した情報。

#### ソフトウェア工学 : ソフトウェアの「品質」、「コスト」、「納期」の最適なバランスを実現するための手法・方法論。
	<ソフトウェア工学の必要性>
	1. 大規模化と複雑さ
	2. IT人材の不足
	3. 社会性と求められるミッション
	4. 不確実性の増大

### 1-b. ソフトウェアライフサイクル
#### ソフトウェアライフサイクル
1. ソフトウェアの誕生
	- ニーズの発生
	- ビジネス上あるいはシステム上の要求を具現化するための企画・計画を行う
	- 要件定義書をまとめる


2. ソフトウェアの開発・運用
	- ソフトウェアの開発
	- 実稼働
	- 保守運用


3. ソフトウェアの廃止
	- サービスの終了
	- 新規ソフトウェアへのリニューアル


## 2. プロジェクトマネジメント

### 2-a. プロジェクト
#### プロジェクトとは？
	有期性：ルーティンワークなどとは異なり、終わりが必ず存在する類の仕事。
	独自性：ソフトウェア開発などのように、独自の目的を達成する類の仕事。

#### フォアキャスティング・バックキャスティング
フォアキャスティング：学校の勉強のように、今の立ち位置から順に目標に進んでいく手法
```
目標に到達できない可能性や、目標から離れたところに到達する可能性がある。
```
バックキャスティングプロジェクト：定めた目標に向けて何が必要かを計画し達成に向かう手法
```
プロジェクトのように、定めた目標に向けて何が必要かを計画し達成に向かう手法。
目標を明確に設定する必要と、目標に向けての道筋を検討する必要がある。
プロジェクト業務はバックキャスティングである。
```

### 2-b. ソフトウェア分析
#### QCD
- QCD：品質（Quality）、コスト（Cost）、納期（Delivery）
- QCDの優先度
	- 品質優先：人命に影響があるようなシステム
	- 費用優先：公共関連システム
	- 納期優先：イベント行事関連システム

#### ソフトウェアの評価
1. コードの物量（ステップ数）：例えばC言語換算でのソースコード行数（総ステップ数）
2. コードの物量（オブジェクト容量）：組み込み型ソフトウェアはサイズが小さいほどよい
3. ファンクションポイント（FP）法：システム規模の概算
4. 使い勝手
	- 画面の視認性
	- 操作性
	- 入力補助
	- 互換性
	- ガイダンス など

### 2-c. 開発プロセス
#### ウォーターフォール型開発プロセス
	要件定義から総合テストの上流から下流までを一つの大きな流れとして行う開発手法。
	進捗管理が容易、成果物が明確といった利点があるが、後工程にしわ寄せが集中というリスクがある。

#### スパイラルモデル
	プログラム開発を小さなフェーズに分割する開発手法。
	フェーズごとにプロトタイプによるデモンストレーションを行い、その都度フィードバックを行う。
	プロトタイプ作成に想定外の作業量が発生するリスクがある。

#### 反復型開発プロセス
	ソフトウェアを機能分割し、これを「反復」と呼ぶ単位で管理する手法。
	メリットして、部品ごとに作成していくため顧客の要望が取り入れやすく、部分的な納品が可能である。
	デメリットとして、分割のため作業量が増えることや全体像が見えずらいことがあげられる。

#### アジャイルプロセス
	変化に対応して無駄を廃し、最適な手法で動くソフトウェアの提供を優先する開発手法。
	ウォーターフォール型開発プロセスでは想定されていなかった「できるだけ決定を遅らせる」、「できるだけ早く提供する」を実現する。
	計画を硬直的に守るよりも変化への対応をすることや、プロセスやツールよりも、個人や個人や相互作用を重視することが価値である。

※開発手法はどれも一長一短であり、ハイブリット型も多い。

### 2-d. WBS
#### wbsとは？
	プロジェクト目標を達成し、必要な要素成果物を生成するために、プロジェクトチームが実行する作業を、要素成果物を主体に階層的に要素分解したもの

#### wbsのメリット
- やることの範囲が明確になる（やらないことが明確になる）
- 作業を洗い出す（やるべき作業が明確になる）
- 全体管理と作業計画が明確化される
- プロジェクト実施時はWBSに則り実行するのみ

#### wbsの例
![wbsの例](../picture/wbs/gant-wbs_mv.jpg.webp "引用＜https://www.jooto.com/contents/wbs/＞")
引用＜jooto; https://www.jooto.com/contents/wbs/ ＞

## 3. UML
### 3.a UMLとは？
	万国共通の記法であり、オブジェクト指向プログラミングで書かれている。
	文章によるドキュメントに加えて開発・設計を図示化（モデル化）する。

### 3.b UMLの様々な図

- ユースケース図
	- アクター
	- ユースケース
	- 関連
	- システム境界
<br>![ユースケース図](../picture/uml/uml-usecase-diagram-online-shopping-system.png "引用＜wondershare; https://www.edrawsoft.com/jp/uml-usecase.html ＞")
<br>引用＜wondershare; https://www.edrawsoft.com/jp/uml-usecase.html ＞

- アクティビティ図
	- システム内部で行われていることを表現する
	- 各ユースケースをどのようなプロセスで実現するかを記載
	- アクションノード（タスクに相当）：角が丸い長方形
	- 矢印（制御フローの方向を示す）
	- 初期ノード（アクティビティの開始点）：黒丸
	- 最終ノード（アクティビティの終了点）
	- フォーク（非同期の分岐を表現）：黒の太線
	- ジョイン（条件分岐・統合など並行する制御フローを同期する）：菱形
<br>![アクティビティ図](../picture/uml/exampleofanactivitydiagram.png "引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/activitydiagram.html ＞")
<br>引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/activitydiagram.html ＞

- クラス図
	- オブジェクト指向モデル
	- 属性（クラスが持つ特性）
	- 操作（クラスが持つ処理）
<br>![クラス図](../picture/uml/class.png "引用＜cacoo; https://cacoo.com/ja/blog/how-to-write-class-diagram/ ＞")
<br>引用＜cacoo; https://cacoo.com/ja/blog/how-to-write-class-diagram/ ＞


- オブジェクト図
	- クラスに中身を入れた状態のもの（クラスの多重度を検証できる）
	- クラス図を作成するための中間生成物的な位置づけ
<br>![オブジェクト図](../picture/uml/exampleobjectdiagram.png "引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/objectdiagram.html ＞")
<br>引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/objectdiagram.html ＞

- シークエンス図
	- 時間の前後関係やタイミングを表現できる
<br>![シークエンス図](../picture/uml/example.png "引用＜東京大学; https://lecture.ecc.u-tokyo.ac.jp/hideo-t/references/uml/sequence-diagram/sequence-diagram.html ＞")
<br>引用＜東京大学; https://lecture.ecc.u-tokyo.ac.jp/hideo-t/references/uml/sequence-diagram/sequence-diagram.html ＞

- コミュニケーション図
	- シークエンス図を書き換えたもの
	- 通信リンクを使って接続形態やネットワーク構成が表現できる
<br>![コミュニケーション図](../picture/uml/uml-communication-diagram-example.png "引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/timingdiagram.html ＞")
<br>引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/timingdiagram.html ＞

- タイミング図
	- オブジェクト間の相互作用のタイミングと状態遷移を表現したもの
<br>![タイミング図](../picture/uml/example_of_a_timing_diagram.png "引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/timingdiagram.html ＞")
<br>引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/timingdiagram.html ＞

- 相互作用概要図（iod）
	- システムの鳥瞰図
	- sd: シークエンス図
	- cd: コミュニケーション図
	- td: タイミング図
	- これらの相互作用をアクションとするアクティビティ図
<br>![相互作用概要図](../picture/uml/exampleofaninteractionoverviewdiagram.png "引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/interactionoverviewdiagram.html ＞")
<br>引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/interactionoverviewdiagram.html ＞

- コンポーネント図
	- コンポーネント：複数のクラスで構成される処理に対して１つ以上のインターフェースを用意し、あたかも１つのクラスのように取り扱ったもの
	- カプセル化されたソフトウェアパーツの管理を目的とした図
	- 「コンポーネント」はタグ付アイコンで表現
<br>![コンポーネント図](../picture/uml/hyperlinkexample-9026.png "引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/componentdiagram.html ＞")
<br>引用＜Enterprise Architect; https://www.sparxsystems.jp/help/16.0/componentdiagram.html ＞

- パッケージ図
	- クラス図のうち”package”であるクラスを抽出
	- パッケージの依存関係を表現し管理
<br>![パッケージ図](../picture/uml/package-diagram-control-navigation-system.png "引用＜wondershare; https://www.edrawsoft.com/jp/what-is-uml-package-diagram.html ＞")
<br>引用＜wondershare; https://www.edrawsoft.com/jp/what-is-uml-package-diagram.html ＞

- 状態マシン図
	- トリガーによるオブジェクトの状態遷移を表現
<br>![状態マシン図の例](../picture/uml/jotaimashin.png "引用＜cacoo; https://cacoo.com/ja/blog/what-is-state-machine-diagram/ ＞")
<br>引用＜cacoo; https://cacoo.com/ja/blog/what-is-state-machine-diagram/ ＞

- 配置図
	- ハードウェアの構成を表現
<br>![配置図の例](../picture/uml/6-deployment-diagram%20.png "引用＜wondershare; https://www.edrawsoft.com/jp/uml-deployment-diagram-example.html ＞")
<br>引用＜wondershare; https://www.edrawsoft.com/jp/uml-deployment-diagram-example.html ＞

## 4. コーディング
- コードは書くよりも読まれることの方が多い
- ソフトウェア開発にあたり読みやすいコードを書くことは必須
	- 他人が読みやすいコード
	- 未来の自分が読みやすいコード
	- ルールが必要
- 言語ごとにコードを統一するためのコーディング規則が存在する（pythonのPEP3など）
- 読みやすいコメントや、わかりやすい命名規則などが大切


## 5. git
### 5.a バージョン管理
#### バージョン管理とは？
	ファイルを「誰が」、「いつ」、「どのように」変更したかを管理すること。
	これらの情報が管理されていれば、多数のメンバーとも共同でコード開発ができる。
	Subversionなどの「集中管理型」と、gitなどの「分散管理型」がある。

#### 集中管理型
	同時編集をするとコンフリクトが発生しやすく、同期に時間がかかる。
	リモートにあげられているものだけがバージョン管理される手法。

#### 分散管理型
	リモートリポジトリへのアクセス頻度が低く、障害に頑健。
	「集中管理型」とは異なり、ローカルでもバージョン管理を行う手法。
 
### 5.b git
#### gitとは？
	分散管理型のバージョン管理システムである。
	元々はオープンソースソフトウェア管理のためのソフトウェアであり、Linuxを作ったLinus Torvaldsに代表されるLinux開発コミュニティによって発案された。
	変更履歴が残る、変更した箇所に戻ることができる、他人と共同編集できるといった特徴がある。

#### コミット
	[ファイル作成／変更／削除]の記録であり、コミットメッセージを残すことができる。
	対象ファイルは一つでも複数でもよく、コミットの単位はユーザーが自由に決定する。

#### レポジトリ
	gitが管理するプロジェクトのフォルダ。
	個々のプロジェクト実行環境上の「ローカルレポジトリ」と、共有の管理場所であるリモートレポジトリがある。

#### ブランチ
	作業を枝分かれさせることができる。
	これによって、共同作業・並行作業が可能となる。
	ブランチの切り方の規則として、gitフローやgithubフローなどがある。

#### .gitignore
	ファイルのパスを記入しておくことで、gitに管理してほしくないファイルを指定するファイル。

### 5.c 主な git commands

1. `git init` : gitの初期化・設定開始

2. `git status` : ワークツリーのステータスを表示

3. `git config` : 設定周りの確認・変更

4. `git log` : ログを表示。`git log --oneline`で１行のみのコミットメッセージを表示。

5. `git diff` : ファイルの差分を表示。`git diff <コミットID>`で過去のコミットとの差分を表示。

6. `git add <ファイルパス>` : 変更したファイルをステージングエリアに追加。

7. `git commit` : コミットの実行。`git commit -m "メッセージ"`で簡単なコミットメッセージ追加。

8. `git commit --amend --no-edit` : コミットの修正。

9. `git checkout` : 削除されたファイルを復旧や過去コミットの復元やブランチの切り替え。

10. `git reset` : コミットのリセット。

11. `git revert` : コミットの変更を打ち消す」コミット。

12. `git rm` : ファイルとindex情報の削除。

13. `git clone` : レポジトリをコピー。

14. `git pull` : リモートレポジトリの同期。

15. `git push` : 変更（コミット）をアップロードする。

16. `git request-pull` : プルリクエスト（変更依頼）

17. `git remote` : リモートレポジトリの設定

18. `git branch` : ブランチの確認・作成。

19. `git merge` : ブランチの統合。

### 5.d github
#### githubとは？
	リモートレポジトリのホスティングサービスの一つ。
	オープンソースソフトウェアの主要なポータルサイト。
	マイクロソフト社の傘下であるGitHub社によって管理されている。

#### githubでのソフトウェア・エンジニアリング
1. `fork` : 他ユーザーのリモートレポジトリを自分のリモートレポジトリにコピーすることができる。

2. `template` : `fork`とは異なり、1つのレポジトリから複数作成できる。元となったリポジトリのコミット履歴を継承しない。

3. `issues` : レポジトリに関する問題・課題・バグ・機能追加や質問などを挙げるための機能。

4. `projects` : issuesなどを管理するためのテーブル・kanban。

### 5.e CI/CD
#### CI（Continuous Integration）
- コード変更を共有リポジトリに頻繁に統合するプロセス
- 自動テストとビルドを定期的に実行し、バグの早期発見と修正を可能に
- CIの自動化により開発のスムーズな進行を促進

#### CD（Continuous Delivery）
- コード変更をテスト環境や本番環境に自動的にデプロイするプロセス
- 自動デプロイメントを組み込み、手動操作によるデプロイの必要性を排除
- CDにより、ユーザーフィードバックを迅速に反映可能

#### CI/CDパイプラインの基本的なステップ
1. **ソース**：コード変更をトリガーにワークフローを起動

2. **ビルド**：ソースコードをコンパイル

3. **テスト**：自動テストを実行

4. **デプロイ**：テスト済みのコードを本番環境にデプロイ

5. **検証**：デプロイされたアプリケーションの動作確認

6. **モニタリング**：本番環境での継続的な監視

#### GitHub Actionsを使用したCI/CD
1. **ワークフローの定義**：YAMLファイルで定義し、 .github/workflows/ディレクトリに配置. イベント、ジョブ、ステップで構成

2. **トリガー**：プッシュ、プルリクエスト、スケジュールなど様々なイベントでワークフローを起動可能

3. **ジョブとステップ**：ジョブは並列実行が可能. ステップでは、シェルコマンドの実行やアクションの使用が可能

4. **アクション**：再利用可能なワークフローの構成要素。コミュニティが作成したアクションも利用可能

5. **ランナー**：GitHub提供のホステッドランナーまたはセルフホステッドランナーを使用可能