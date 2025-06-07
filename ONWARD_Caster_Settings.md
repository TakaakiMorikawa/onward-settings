# ONWARD キャスター参加設定まとめ

**最終更新日：2025-06-07**

---

## ✅ 起動オプションと操作

```
-novr -force-d3d11
```

- HMDなしでも起動可能に
- `Alt + Enter` で強制ウィンドウ化し、見えないウィンドウをモニター上に表示

---

## ✅ MSI Afterburner による軽いOC（オーバークロック）

| 項目            | 推奨設定値              |
|-----------------|------------------------|
| Power Limit     | 110%（最大）            |
| Core Clock      | +75〜+100 MHz           |
| Memory Clock    | +250〜+400 MHz          |
| Fan Curve       | 70℃〜から冷却強化         |

- Heaven BenchmarkやONWARD起動で安定性を確認

---

## ✅ OBSや描画競合の対策

| ツール             | 設定                     |
|--------------------|--------------------------|
| OBS                | OK（NVENC＋フルRGB）     |
| ShadowPlay         | 無効推奨                  |
| Discord Overlay    | 無効推奨                  |

---

## ✅ NVIDIA コントロールパネル設定

### ● 3D 設定
- 最大パフォーマンス優先
- スレッド最適化オン
- G-Sync 無効化（不要なら）

### ● ディスプレイ・ビデオ設定
- 解像度：1920×1080（ネイティブ）
- GPUスケーリングを使用
- ビデオカラー設定：NVIDIA制御 / フルRGB
- ビデオイメージ設定：ノイズ除去・補正 OFF

---

## ✅ Null HMD の設定（仮想HMDによるSteamVR起動）

`C:\Program Files (x86)\Steam\config\steamvr.vrsettings` に以下を追加：

```json
"steamvr": {
  "activateMultipleDrivers": true,
  "forcedDriver": "null",
  "requireHmd": false
}
```

→ SteamVRを仮想HMDモードで起動でき、ONWARDが描画されるようになる。

---

## ✅ 最終チェックリスト

- [x] 起動オプション：`-novr -force-d3d11`
- [x] `Alt + Enter` 操作で表示
- [x] Null HMD設定済み（必要に応じて）
- [x] GPU OC済み（安定性確認済）
- [x] OBS設定確認済み
- [x] ShadowPlay/Overlay 無効化
- [x] NVIDIA描画設定最適化

---

以上が、ONWARDをHMDなしでキャスター参加するための設定完全ガイドです。
