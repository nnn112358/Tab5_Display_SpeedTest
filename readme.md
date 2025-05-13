# 250514_M5unified_Tab5_draw_speed


## 概要
@lovyan03 氏のXより、setRotationで描画速度が変化するという報告があった。
Tab5にて、Spriteの大きさとsetRotationを変えて描画速度を検証した。

https://x.com/lovyan03/status/1922263342413959502

## プロジェクト構成
- `src/main.cpp`: メインソースファイル。
- `platformio.ini`: PlatformIO 設定ファイル。必要な依存関係とビルド設定を含みます。


## ビルド手順
1. PlatformIO でプロジェクトを開きます。
   - Visual Studio Code + PlatformIO 拡張機能を使用する場合：
     - VSCode で「ファイル」→「フォルダを開く」からプロジェクトフォルダを選択
     - PlatformIO のサイドバーからプロジェクトを開く

2. ビルドして M5Stack デバイスにアップロードします。
   - PlatformIO の「Upload」ボタンをクリック
   - または、ターミナルから `pio run -t upload` を実行


## パフォーマンス結果
![image](https://github.com/user-attachments/assets/cb77ca24-24a6-4fba-b63c-5531c3248dd3)

```
Size: 160x160
Rotation 0: 2.05 ms/frame
Rotation 1: 2.00 ms/frame
Rotation 2: 2.00 ms/frame
Rotation 3: 2.00 ms/frame
Size: 320x320
Rotation 0: 14.05 ms/frame
Rotation 1: 14.95 ms/frame
Rotation 2: 14.05 ms/frame
Rotation 3: 15.00 ms/frame
Size: 640x640
Rotation 0: 55.00 ms/frame
Rotation 1: 288.05 ms/frame
Rotation 2: 55.05 ms/frame
Rotation 3: 288.00 ms/frame
Size: 720x720
Rotation 0: 68.00 ms/frame
Rotation 1: 72.00 ms/frame
Rotation 2: 68.05 ms/frame
Rotation 3: 72.05 ms/frame
Size: 720x1280
Rotation 0: 120.00 ms/frame
Rotation 2: 120.60 ms/frame
Size: 1280x720
Rotation 1: 646.05 ms/frame
Rotation 3: 645.80 ms/frame
```

## 依存関係
- [M5Unified](https://github.com/m5stack/M5Unified) - M5Stackデバイス用の統合ライブラリ

