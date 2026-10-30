# 芳賀人名辞典データセット

Haga Jinmei Dictionary Dataset

芳賀矢一編『日本人名辞典』（大倉書店、1914年）をもとにしたデータセットです。作成者（Creator）は人間文化研究機構（National Institutes for the Humanities, NIHU）です。

本リポジトリには、公開が承認されたデータと付属文書を収録しています。本データセットの説明文書は日本語を正本とします。必要に応じて機械翻訳等をご利用ください。ライセンスの法的条件は英語の [LICENSE](LICENSE) が参照するCC0 1.0に従います。

## 収録ファイル

- [data/haga_jinmei_records.csv](data/haga_jinmei_records.csv)：辞典の1項目を1行とするUTF-8 CSV。全6列の意味は[データ辞書](DATA_DICTIONARY.md)に記載しています。
- [data/release_manifest.json](data/release_manifest.json)：列一覧、件数、SHA-256ハッシュ等の検証情報。
- [schema/public_record.schema.json](schema/public_record.schema.json)：公開レコードの構造を定義したJSON Schema。
- [RIGHTS.md](RIGHTS.md)、[LICENSE](LICENSE)：権利・利用条件と引用のお願い。
- [CITATION.cff](CITATION.cff)：引用用メタデータ。
- [CHANGELOG.md](CHANGELOG.md)：更新履歴。

公開CSVには、辞典本文の全文を含む `description` と、人名・見出し等の6列を収録しています。これらの公開はNIHUとして承認済みです。内部メモ、業者納品データ、元ワークブックの非公開列、LLM出力は含みません。

## 収録範囲と留意点

収録数は54,558項目です。このうち、準備段階で参照項目に類すると分類されたものが8,559項目あります。分類用の内部フラグは公開CSVには含めていません。

項目数は人物数を意味しません。複数人を記述する項目も1行のまま収録しています。詳細は[複数人物を含む項目の扱い](MULTI_PERSON_ENTRIES.md)をご覧ください。`entry_no` は、本版の行順に付けた6桁の番号です。

`full_name` が空欄の項目が2件、`description` が空欄の項目が3件あり、未校訂の文字も含まれます。本データセットは提供されたワークブックを変換したもので、原典との完全な校合を経た校訂版ではありません。

## 利用条件と公開状況

データセットはCC0 1.0で公開します。引用は学術上のお願いであり、再利用の条件ではありません。詳細は[権利と引用について](RIGHTS.md)をご覧ください。

公開準備の状況は[公開チェックリスト](RELEASE_CHECKLIST.md)、訂正と更新は[更新履歴](CHANGELOG.md)に記録します。

## 訂正・問い合わせ

[GitHubのIssues](https://github.com/NIHU-jp/haga-jinmei-dataset/issues)へお寄せください。特定の行に関するご連絡では、対象の行が分かる情報を添えてください。
