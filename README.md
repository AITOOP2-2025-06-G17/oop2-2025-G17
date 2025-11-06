# oop2-2025-G17
授業内課題
アプリ起動時にMDReportMakerApp が生成されると同時に以下のビュー要素が初期化される。
### データ作成：
アプリ起動時（MDReportMakerApp.__init__）に report_model を生成。
モデルの get_body() を呼び出して MDTextEdit に初期表示。

### データ更新：
各 InputButton 押下で編集ダイアログを開く。

表示時：get_text_by_key() でモデルの現在値を取得。

入力変更時：set_text_by_key() でモデルの値を更新。

更新後：update_text_edit() で get_body() を再呼び出し、右側のビューを再描画。

### 永続化：
SaveButton 押下時にビューが
save_file() または save_file_without_history() を呼び出し、
モデルがMarkdownファイルと status.json（履歴）を保存。