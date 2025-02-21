# VS Code Cline Auto-continuation Extension
A VS Code extension that automates large-scale task execution in Cline. It provides functionality to automatically continue tasks when execution stops midway.

## Features
- Batch task loading from files
- Continuous task execution with auto-continuation mode
- Automatic recovery with timeout detection
- Simple operation

## Requirements
- Visual Studio Code 1.60.0 or higher
- Cline extension must be installed

## Installation
1. Download the latest `.vsix` file from the [releases page](./releases)
2. Open VS Code
3. Install using one of these methods:
   - Drag and drop the `.vsix` file into the VS Code window
   - Open the command palette (Ctrl+Shift+P), run `Extensions: Install from VSIX` and select the `.vsix` file
4. Restart VS Code

## Usage
### File Loading Mode
1. Open the command palette (Ctrl+Shift+P)
2. Select `Cline Auto: Start Tasks From File`
3. Choose a text file (.txt) containing prompts
   - Each line in the file will be executed as a separate prompt
   - Empty lines are automatically skipped

Example prompts file:
```text
Please explain the contents of Task 1
Please execute Task 2
Please complete the final task
```

### Auto-continuation Mode
1. Open the command palette (Ctrl+Shift+P)
2. Select `Cline Auto: Start Tasks With Auto Continue`
3. Enter the initial prompt
4. When a response wait state is detected, the prompt "Please proceed with the next tasks in sequence" will be automatically sent

## Settings
Settings can be modified in `settings.json`:
```json
{
  "cline-auto.responseTimeout": 5000,  // Time to detect response wait state (milliseconds)
  "cline-auto.autoContinueMessage": "Please proceed with the next tasks in sequence"  // Auto-continuation message
}
```

## Troubleshooting
### If Tasks Are Not Executing Correctly
- Verify that the Cline extension is properly installed
- Try restarting VS Code
- Check error messages in Developer Tools (Help > Toggle Developer Tools)

### If Files Cannot Be Loaded
- Verify that the file is encoded in UTF-8
- Check file permissions
- Verify that the file path doesn't contain special characters

## Feedback
Please report any issues or suggestions in the [Issues](./issues) section.

## License
MIT License - See the [LICENSE](./LICENSE) file for details.

------------

# VS Code Cline Auto-continuation Extension

Clineの大規模なタスク実行を自動化する VS Code 拡張機能です。タスクの実行が途中で停止した場合に自動的に継続する機能を提供します。

## 特徴

- ファイルからの一括タスク読み込み
- 自動継続モードによるタスクの連続実行
- タイムアウト検知による自動リカバリー
- シンプルな操作性

## 必要条件

- Visual Studio Code 1.60.0以上
- Cline拡張機能がインストールされていること

## インストール方法

1. [リリースページ](./releases)から最新の`.vsix`ファイルをダウンロード
2. VS Codeを開く
3. 以下のいずれかの方法でインストール：
   - `.vsix`ファイルをVS Codeウィンドウにドラッグ＆ドロップ
   - コマンドパレットを開き（Ctrl+Shift+P）、`Extensions: Install from VSIX`を実行して`.vsix`ファイルを選択
4. VS Codeを再起動

## 使用方法

### ファイル読み込みモード

1. コマンドパレットを開く（Ctrl+Shift+P）
2. `Cline Auto: Start Tasks From File`を選択
3. プロンプトが記載されたテキストファイル（.txt）を選択
   - ファイルの各行が個別のプロンプトとして実行されます
   - 空行は自動的にスキップされます

プロンプトファイルの例：
```text
タスク1の内容を説明してください
タスク2を実行してください
最後のタスクを完了させてください
```

### 自動継続モード

1. コマンドパレットを開く（Ctrl+Shift+P）
2. `Cline Auto: Start Tasks With Auto Continue`を選択
3. 最初のプロンプトを入力
4. 応答待ち状態が検知されると自動的に「次のタスクも順次進めてください」というプロンプトが送信されます

## 設定

設定は`settings.json`で変更可能です：

```json
{
  "cline-auto.responseTimeout": 5000,  // 応答待ち状態を検知する時間（ミリ秒）
  "cline-auto.autoContinueMessage": "次のタスクも順次進めてください"  // 自動継続時のメッセージ
}
```

## トラブルシューティング

### タスクが正しく実行されない場合

- Cline拡張機能が正しくインストールされているか確認してください
- VS Codeを再起動してみてください
- Developer Tools（Help > Toggle Developer Tools）でエラーメッセージを確認してください

### ファイルが読み込めない場合

- ファイルがUTF-8でエンコードされているか確認してください
- ファイルの権限設定を確認してください
- ファイルパスに特殊文字が含まれていないか確認してください

## フィードバック

問題や提案がありましたら、[Issue](./issues)に報告してください。

## ライセンス

MIT License - 詳細は[LICENSE](./LICENSE)ファイルを参照してください。
