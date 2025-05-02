# Godot 4.x 用 プロジェクト初期化プラグイン

[![Godot Engine 4.x](https://img.shields.io/badge/Godot%20Engine-4.x-blue)](https://godotengine.org/)
[![MIT license](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Godot 4.x プロジェクトを素早く整理された状態で始めるための初期設定プラグインです。プロジェクト構造の自動セットアップと基本設定の最適化をワンクリックで行います。

---

## 📋 特徴

- ✅ **フォルダ構造の自動生成**: 整理された基本フォルダ構造を作成
- ✅ **プロジェクト設定の最適化**: 画面解像度やアスペクト比などを自動調整
- ✅ **簡単操作**: エディタのツールバーからワンクリックで実行
- ✅ **確認ダイアログ**: 実行前に変更内容を確認可能
- ✅ **完了通知**: 設定完了時に通知ダイアログを表示

## 🔧 インストール方法

1. このリポジトリをクローンまたはダウンロードします
2. ファイルを Godot プロジェクトの `res://addons/project_setup/` に配置します
3. Godot エディタの「プロジェクト」→「プロジェクト設定」→「プラグイン」タブを開きます
4. リストから「Project Setup」を見つけ、「有効」にチェックを入れます

## 🚀 使用方法

1. Godot エディタのツールバーに追加された「プロジェクト初期設定」ボタンをクリックします
2. 確認ダイアログが表示され、実行される設定内容が表示されます
3. 「OK」をクリックすると設定が実行されます
4. 完了すると通知ダイアログが表示されます
5. 「プロジェクト」→「現在のプロジェクトを再読み込み」するとファイルシステムが更新されます

## 📁 作成されるフォルダ構造

```
res://
  ├── assets/
  │   ├── sprites/
  │   │   ├── characters/
  │   │   ├── items/
  │   │   ├── ui/
  │   │   ├── effects/
  │   │   ├── backgrounds/
  │   │   └── tilesets/
  │   ├── audio/
  │   │   ├── music/
  │   │   ├── sfx/
  │   │   └── voice/
  │   ├── fonts/
  │   └── data/
  ├── scenes/
  │   ├── levels/
  │   ├── ui/
  │   ├── characters/
  │   ├── items/
  │   └── components/
  ├── src/
  │   ├── autoload/
  │   └── utils/
  ├── addons/
  └── _debug/
```

## 📄 フォルダ構造の詳細

| フォルダ | 内容 |
|---------|------|
| **assets/sprites/characters/** | プレイヤーキャラクターやNPCなどのスプライト |
| **assets/sprites/items/** | アイテム、武器、収集物などのスプライト |
| **assets/sprites/ui/** | UIパーツ、ボタン、アイコンなどの画像 |
| **assets/sprites/effects/** | 視覚エフェクト（パーティクルなど）用の画像 |
| **assets/sprites/backgrounds/** | 背景画像やパララックス背景 |
| **assets/sprites/tilesets/** | タイルマップで使用するタイルセット |
| **assets/audio/music/** | BGMや背景音楽 |
| **assets/audio/sfx/** | 効果音 |
| **assets/audio/voice/** | ボイスやナレーション |
| **assets/fonts/** | フォントファイル |
| **assets/data/** | JSONやCSVなどのデータファイル |
| **scenes/levels/** | ゲームレベルやステージのシーン |
| **scenes/ui/** | メニュー、HUD、ダイアログなどのUIシーン |
| **scenes/characters/** | プレイヤーやNPCのキャラクターシーン |
| **scenes/items/** | アイテムやオブジェクトのシーン |
| **scenes/components/** | 再利用可能なシーンコンポーネント |
| **src/autoload/** | シングルトンとして使用するグローバルスクリプト |
| **src/utils/** | ユーティリティや汎用機能のスクリプト |
| **addons/** | サードパーティや自作のプラグイン |
| **_debug/** | テスト用シーンやスクリプト、デバッグツール |

## ⚙️ 適用されるプロジェクト設定

| 項目 | 設定値 |
|-----|--------|
| ウィンドウサイズ | 1280x720 |
| ストレッチモード | canvas_items |
| アスペクト比 | keep |
| 物理演算ティック | 60 fps |

## 🛠️ カスタマイズ

プラグインスクリプト内の以下の変数を編集することで、作成されるフォルダ構造やプロジェクト設定をカスタマイズできます：

```gdscript
# フォルダ構造の定義
var folders = [
    "res://assets",
    "res://assets/sprites",
    # ... 他のフォルダ
]

# プロジェクト設定の定義
var project_settings = {
    "display/window/size/viewport_width": 1280,
    "display/window/size/viewport_height": 720,
    # ... 他の設定
}
```

## 📋 動作要件

- Godot 4.4.1

## 📝 ライセンス

MIT ライセンス

## 👏 謝辞

- [Godot Engine](https://godotengine.org/)
