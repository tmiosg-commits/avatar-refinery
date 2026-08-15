# Avatar Refinery(アバターリファイナリー)

**VRChatアバターを、アップロード前にまとめて健康診断。**
「何が問題で・なぜ問題で・どう直すか」を日本語で表示する Unity エディタ拡張です。診断は読み取り専用で、アバターやアセットは一切変更しません。

- 現在の版: **Avatar Refinery Lite v0.1.1(無料・β)**
- 対応: Unity 2022.3.22f1 / VRChat SDK Avatars 3.7〜3.10 / Modular Avatar・NDMF・AAO 使用時は「ビルド後の姿」で性能を算定
- 配布: [BOOTH](#) ／ VCC・ALCOM(下記)／ [GitHub Releases](https://github.com/tmiosg-commits/avatar-refinery/releases)

## インストール

### VCC / ALCOM で入れる(更新が自動で届きます)

1. 下のリンクを押す(VCC または ALCOM が開きます)
   **[Add to VCC / ALCOM](vcc://vpm/addRepo?url=https%3A%2F%2Ftmiosg-commits.github.io%2Favatar-refinery%2Fvpm.json)**
2. 「Avatar Refinery」リポジトリを追加 → プロジェクトの Manage Packages で **Avatar Refinery** を Install

リンクが開かない場合は、VCC の Settings > Packages > Add Repository に次の URL を貼ってください:
`https://tmiosg-commits.github.io/avatar-refinery/vpm.json`

### unitypackage で入れる

[BOOTH](#) または [Releases](https://github.com/tmiosg-commits/avatar-refinery/releases) から `AvatarRefinery_Lite_x.y.z.unitypackage` をダウンロードし、プロジェクトを開いた状態でインポート(`Packages/com.avatarrefinery.core` に入ります)。

## 使い方

1. `Tools > Avatar Refinery > Avatar Refinery を開く`
2. Hierarchy でアバターのルートを選ぶ(自動で欄に入ります)
3. **診断する** を押す

Hierarchy のアバターを右クリック → `Avatar Refinery > このアバターを診断` でも起動できます。
結果は「⛔ アップロードを止める / ⚠ 見た目・動作が壊れる / 📉 ランクを下げている / ℹ 情報」の4段階に分かれ、各項目に **症状 → 検出 → 対応(手順)** が付きます。「詳細モード」で原因・影響・参考ページも表示。「レポート保存」で Markdown に書き出せます(質問・依頼の添付にどうぞ)。

## 診断項目(Lite v0.1.1)

| 分類 | 項目 |
|---|---|
| 環境 | Unity バージョン / VRChat SDK バージョン / 旧 Dynamic Bone の残存 |
| VRChat 設定 | Avatar Descriptor の有無 / 視点位置 / 口パク(Viseme)/ Eye Look / Expression Parameters 容量・参照 / Expression Menu の参照切れ / FX の Write Defaults 混在 / 表情とまばたき・口パクの競合 / PhysBone の無効設定 / Missing Script |
| マテリアル・テクスチャ | シェーダー欠落(ピンク)/ 空スロット / 非圧縮テクスチャ / Streaming Mip Maps / 4K 以上のテクスチャ |
| リグ | Animator・Humanoid / 必須ボーン / 指ボーン |
| 描画 | Anchor Override の不統一 / Bounds 異常 / メッシュ参照切れ |
| パフォーマンス | PC・Quest 両方のランクと、各項目の「次のランクまであといくつ」 |
| 非破壊ツール | NDMF(Modular Avatar / AAO 等)のビルド時エラー・警告。Expressions・Write Defaults はビルド後の状態で判定 |
| VRM | VRM(VRoid 等)読み込み直後で VRChat 向け変換がまだの状態 |

## 注意

- 表示されるランクはローカルでの推定です。最終的な値は VRChat のサーバー側で決まります。
- 診断はアバターを変更しません。修正は表示された手順に沿って手動で行ってください(自動修正は製品版で提供予定)。
- MMD 由来モデルなど、利用規約上 VRChat で使えないモデルの利用を推奨するものではありません。

## サポート

- 不具合報告・要望: **X(旧Twitter)の DM** → [@runsol_ai](https://x.com/runsol_ai)
- 対象は本ツールの不具合と使い方です。個別アバターの改変相談・他ツールの不具合は対象外です。
- 「レポート保存」で出力した Markdown を添えていただくと、状況把握が早くなります。

## ライセンス・更新履歴

- 利用規約: [LICENSE.md](LICENSE.md)(再配布禁止・改変私用可)
- 更新履歴: [CHANGELOG.md](CHANGELOG.md)
