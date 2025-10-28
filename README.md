# ⏳ 履歴の最初に戻る (historyGoFirst) v4.3

このスクリプトは、ブラウザの「履歴」機能にアクセスし、**開いたページの中から一番最初のページまで一気に「戻る」操作**を実行するUserScriptです。

Webサイトを巡回して元のページに戻りたい時、ブラウザの「戻る」ボタンを何度も押す手間を解消します。

---

## 🚀 インストール方法

インストールは、**GreasyFork**から行うのが**最も簡単**です。

**下のリンクからインストールしてくださいね！**

**[✨ GreasyForkでインストールする ✨](https://greasyfork.org/ja/scripts/546323)**

### 拡張機能の準備

このスクリプトを使うには、UserScript管理のための拡張機能が必要です。

* **Tampermonkey**: 
    * [Chrome ウェブストア](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
    * [Firefox Add-ons](https://addons.mozilla.org/ja/firefox/addon/tampermonkey/)
* **Violentmonkey**: 
    * [Chrome ウェブストア](https://chrome.google.com/webstore/detail/violent-monkey/jinjaccalgkegednnccohejagnlnfdag)
    * [Firefox Add-ons](https://addons.mozilla.org/ja/firefox/addon/violentmonkey/)

---

## 🎀 機能紹介

* キーボードショートカットで、すぐに実行できます。（デフォルト: **Ctrl+Shift+H**）
* 右クリックメニュー（Tampermonkeyのメニュー）からも実行できます。
* ショートカットキーは、設定画面から好きなキーに変更できます。

---

## 💻 技術的な特徴

このスクリプトの真の価値は、ブラウザの履歴機能が持つ「**技術的な限界**」を解決した点にあります。

❌ **通常のブラウザ操作の限界**
* ブラウザの標準機能では、履歴の**途中のページから**正確に「最初」まで戻ろうとしても、失敗したことを知る**正攻法が存在しません**。
* 一般的な`history.go(1-history.length)`は、**最新のページから実行しないと機能しない**という限界があります。

💡 **知的で高度な解決ロジック**
* このスクリプトは、実行時、**現在表示しているページ**の履歴情報に`history.replaceState`で「**マーカー（目印）**」を設置します。
* 次に、`1-history.length`使って、**履歴の最初へ一気にジャンプ**を試みます。
* このジャンプは、**余計なページロードを一切発生させず**、**真の最初のページに移動できたときのみ**ページロードが発生し、移動先のページで**マーカーの有無をチェック**することで成功を正確に判定します。
* **中間ページのロードを完全にスキップ**し、最も効率的に履歴の最初に戻る**世界唯一（？）のロジック**を実現しています。

---

## 🛡️ ライセンスについて

このスクリプトは、ねおんが著作権を保有しています。

* **ライセンス**: **CC BY-NC 4.0** です。（**LICENSEファイル**をご参照ください。）
* **お願い**: 個人での利用や改変、非営利の範囲内での再配布はOKです。でも、**商用目的での利用はご遠慮ください**。

※ ご利用は自己責任でお願いします。（悪用できるようなものではないですが、念のため！）
