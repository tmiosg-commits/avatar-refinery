# Changelog

## 0.1.1 (2026-08 初回公開 / β)

初回公開版(Lite)。

- 診断: 環境 / VRChat 設定(Descriptor・視点位置・Viseme・Eye Look・Expressions・Write Defaults・Missing Script)/ マテリアル・テクスチャ / リグ / 描画 / パフォーマンス(PC・Quest)/ VRM 未変換状態
- 診断: 表情アニメーションとまばたき / 口パクの競合(半目・白目・口が動かない)。Tracking Control(Animation)付きのステートは除外
- 診断: Expression Menu の参照切れ(サブメニュー未設定・存在しないパラメータ・項目数超過)
- 診断: PhysBone の無効設定(Root がアバター外・揺れる対象なし・空参照・重なり)
- NDMF(Modular Avatar / AAO 等)使用時は「ビルド後の姿」で性能を算定。Expression Parameters 容量・Menu / Parameters 参照・Write Defaults 混在もビルド後の状態で判定
- NDMF のビルド時エラー・警告を診断結果に反映(NDMF コンソールは自動表示しない)
- 日本語の説明(症状 → 検出 → 原因 → 影響 → 対応)、初心者モード / 詳細モード
- Markdown レポート出力
- 読み取り専用(アバター・アセットを変更しない)

(0.1.0 は内部検証版。公開せず 0.1.1 に統合)
