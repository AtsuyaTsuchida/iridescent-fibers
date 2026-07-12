# Iridescent Fibers

[English](#english) | [日本語](#日本語)

---

## English

A Three.js reproduction (single HTML file) of a Pinterest reference: a bundle of **iridescent, rainbow-glowing fibers that undulate and swirl**.

### Run
```sh
cd ~/dev/iridescent-fibers
python3 -m http.server 8160
# → http://localhost:8160/
```
> Three.js is loaded from a CDN; vendor it locally for fully offline use.

### How it works
- The pulsing and swirling motion is done in a **vertex shader** (per-strand phase offsets drive the undulation and axial twist).
- The rainbow sheen comes from a thin-film / view-angle dependent color model.
- Additive blending gives the glow.

### Notes
Key tuning learned here: keep the additive glow under control to **avoid blowing out to white** — clamp emission and balance strand count vs. alpha. A Blender/Cycles version of the same motif lives in [iridescent-fibers-blender](https://github.com/AtsuyaTsuchida/iridescent-fibers-blender).

---

## 日本語

Pinterest 参照「**虹色に光る繊維束がうねる**」CG 映像を Three.js 単一 HTML で再現。

### 起動
```sh
cd ~/dev/iridescent-fibers
python3 -m http.server 8160
# → http://localhost:8160/
```
> Three.js は CDN 読み込み。完全オフライン運用時は vendor 化が必要。

### 仕組み
- 脈動・旋回は**頂点シェーダー**で実装（繊維ごとの位相オフセットでうねりと軸方向のねじれを駆動）。
- 虹色の光沢は薄膜／視線角依存のカラーモデル。
- 加算合成で発光感を出す。

### 勘所
ここでの肝は加算発光を抑えて**白飛びを回避**すること（発光をクランプし、繊維数と alpha のバランスを取る）。
同モチーフの Blender/Cycles 版は [iridescent-fibers-blender](https://github.com/AtsuyaTsuchida/iridescent-fibers-blender)。
