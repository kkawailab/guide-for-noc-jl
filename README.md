# Nature of Code をJuliaで学ぶためのガイド

[Nature of Code](https://natureofcode.com/) の内容をJuliaとJavaScript (p5.js) で実装した学習用ノートブック集です。

## 概要

このリポジトリは、Daniel Shiffmanの「Nature of Code」をベースに、自然界のシミュレーションに必要なプログラミング技術を日本語で解説しています。

## 目次

| 章 | タイトル | 言語 | 主な内容 |
|:--:|---------|:----:|---------|
| 0 | [Randomness（乱数と確率）](notebooks/00_randomness.ipynb) | JavaScript | ランダムウォーク、正規分布、パーリンノイズ |
| 1 | [Vectors（ベクトル）](notebooks/01_vectors.ipynb) | JavaScript | ベクトル演算、正規化、速度と加速度 |
| 2 | [Forces（力）](notebooks/02_forces.ipynb) | JavaScript | ニュートンの運動法則、重力、摩擦、万有引力 |
| 3 | [Oscillation（振動）](notebooks/03_oscillation.ipynb) | JavaScript | 三角関数、角運動、単振動、バネ、振り子 |
| 4 | [Particle Systems（パーティクルシステム）](notebooks/04_particle_systems.ipynb) | JavaScript | パーティクル、エミッター、継承、ポリモーフィズム |
| 5 | [Autonomous Agents（自律エージェント）](notebooks/05_autonomous_agents.ipynb) | Julia | ステアリング行動、フローフィールド、群れ行動（Boids） |
| 6 | [Physics Libraries（物理ライブラリ）](notebooks/06_physics_libraries.ipynb) | Julia | 剛体力学、衝突検出、拘束、Verlet積分 |
| 7 | [Cellular Automata（セル・オートマトン）](notebooks/07_cellular_automata.ipynb) | Julia | 1次元CA、Wolframルール、ライフゲーム |
| 8 | [Fractals（フラクタル）](notebooks/08_fractals.ipynb) | Julia | 再帰、コッホ曲線、L-System、マンデルブロ集合 |
| 9 | [Evolutionary Computing（進化的計算）](notebooks/09_evolutionary_computing.ipynb) | Julia | 遺伝的アルゴリズム、選択、交叉、突然変異 |
| 10 | [Neural Networks（ニューラルネットワーク）](notebooks/10_neural_networks.ipynb) | Julia | パーセプトロン、多層NN、バックプロパゲーション |

## 各章の詳細

### Chapter 0: Randomness（乱数と確率）
- ランダムウォーカーの実装
- 一様分布と正規分布（ガウス分布）
- パーリンノイズによる滑らかな乱数

### Chapter 1: Vectors（ベクトル）
- ベクトルの基本（加算、減算、乗算）
- 正規化と大きさの制限
- Moverクラスによる運動のカプセル化

### Chapter 2: Forces（力）
- ニュートンの3法則の実装
- 重力、摩擦、流体抵抗のシミュレーション
- 万有引力とN体問題

### Chapter 3: Oscillation（振動）
- 極座標とデカルト座標の変換
- 角速度と角加速度
- 単振動、波、バネ（フックの法則）、振り子

### Chapter 4: Particle Systems（パーティクルシステム）
- ライフスパンを持つパーティクル
- エミッターによる粒子の生成と管理
- クラスの継承とポリモーフィズム

### Chapter 5: Autonomous Agents（自律エージェント）
- ステアリング行動（Seek, Flee, Arrive, Wander）
- フローフィールドの追従
- 群れ行動（Separation, Alignment, Cohesion）

### Chapter 6: Physics Libraries（物理ライブラリ）
- 剛体と円形ボディの実装
- 衝突検出と応答（弾性衝突）
- 距離拘束とVerlet積分
- ロープと布のシミュレーション

### Chapter 7: Cellular Automata（セル・オートマトン）
- 1次元CA（Wolframルール）
- 2次元CA（Conway's Game of Life）
- グライダー、振動子、グライダー銃

### Chapter 8: Fractals（フラクタル）
- 再帰による自己相似構造
- カントール集合、コッホ曲線、シェルピンスキー三角形
- L-Systemによるフラクタル生成
- マンデルブロ集合とジュリア集合

### Chapter 9: Evolutionary Computing（進化的計算）
- 遺伝的アルゴリズムの基本構造
- シェイクスピア問題（文字列進化）
- Smart Rockets（ロケットの経路最適化）
- 生態系シミュレーション

### Chapter 10: Neural Networks（ニューラルネットワーク）
- パーセプトロンと線形分類
- 多層パーセプトロン（MLP）
- バックプロパゲーション
- XOR問題の解法
- 神経進化（Neuroevolution）

## 必要な環境

### JavaScript (Chapter 0-4)
- p5.js対応の環境（ブラウザ、p5.js Web Editor等）

### Julia (Chapter 5-10)
- Julia 1.6以上
- 必要なパッケージ:
  - LinearAlgebra（標準ライブラリ）
  - Plots
  - Statistics（標準ライブラリ）
  - Random（標準ライブラリ）

```julia
using Pkg
Pkg.add("Plots")
```

## 参考資料

- [Nature of Code](https://natureofcode.com/) - Daniel Shiffman
- [The Coding Train](https://thecodingtrain.com/) - YouTube チャンネル

## ライセンス

このリポジトリの内容は学習目的で作成されています。
オリジナルの「Nature of Code」はDaniel Shiffmanによるものです。
