# Nature of Code をJuliaで学ぶためのガイド

[Nature of Code](https://natureofcode.com/) の内容をJuliaで実装した学習用ノートブック集です。

## 概要

このリポジトリは、Daniel Shiffmanの「Nature of Code」をベースに、自然界のシミュレーションに必要なプログラミング技術を日本語で解説しています。すべてのノートブックはJuliaで実装されており、実行結果（グラフ・可視化）も含まれています。

## 目次

| 章 | タイトル | 主な内容 |
|:--:|---------|---------|
| 0 | [Randomness（乱数と確率）](notebooks/00_randomness.ipynb) | ランダムウォーク、正規分布、パーリンノイズ |
| 1 | [Vectors（ベクトル）](notebooks/01_vectors.ipynb) | ベクトル演算、正規化、速度と加速度 |
| 2 | [Forces（力）](notebooks/02_forces.ipynb) | ニュートンの運動法則、重力、摩擦、万有引力 |
| 3 | [Oscillation（振動）](notebooks/03_oscillation.ipynb) | 三角関数、角運動、単振動、バネ、振り子、二重振り子 |
| 4 | [Particle Systems（パーティクルシステム）](notebooks/04_particle_systems.ipynb) | パーティクル、エミッター、抽象型、煙・爆発・花火エフェクト |
| 5 | [Autonomous Agents（自律エージェント）](notebooks/05_autonomous_agents.ipynb) | ステアリング行動、フローフィールド、群れ行動（Boids） |
| 6 | [Physics Libraries（物理ライブラリ）](notebooks/06_physics_libraries.ipynb) | 剛体力学、衝突検出、拘束、Verlet積分 |
| 7 | [Cellular Automata（セル・オートマトン）](notebooks/07_cellular_automata.ipynb) | 1次元CA、Wolframルール、ライフゲーム |
| 8 | [Fractals（フラクタル）](notebooks/08_fractals.ipynb) | 再帰、コッホ曲線、L-System、マンデルブロ集合 |
| 9 | [Evolutionary Computing（進化的計算）](notebooks/09_evolutionary_computing.ipynb) | 遺伝的アルゴリズム、選択、交叉、突然変異 |
| 10 | [Neural Networks（ニューラルネットワーク）](notebooks/10_neural_networks.ipynb) | パーセプトロン、多層NN、バックプロパゲーション |

## 各章の詳細

### Chapter 0: Randomness（乱数と確率）
- ランダムウォーカーの実装
- 一様分布と正規分布（ガウス分布）
- パーリンノイズによる滑らかな乱数
- ノイズを使った地形生成

### Chapter 1: Vectors（ベクトル）
- ベクトルの基本（加算、減算、乗算）
- 正規化と大きさの制限
- Moverクラスによる運動のカプセル化
- ターゲット追跡（Seeking）

### Chapter 2: Forces（力）
- ニュートンの3法則の実装
- 重力、摩擦、流体抵抗のシミュレーション
- 万有引力とN体問題
- 質量による運動の違い

### Chapter 3: Oscillation（振動）
- 極座標とデカルト座標の変換
- 角速度と角加速度
- 単振動、波、バネ（フックの法則）
- 振り子と二重振り子（カオス）
- リサージュ図形

### Chapter 4: Particle Systems（パーティクルシステム）
- ライフスパンを持つパーティクル
- エミッターによる粒子の生成と管理
- 抽象型と多重ディスパッチによるポリモーフィズム
- 煙、爆発、花火のエフェクト
- パーティクルの軌跡

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

### Julia
- Julia 1.9以上（推奨: 1.12）
- 必要なパッケージ:
  - LinearAlgebra（標準ライブラリ）
  - Plots
  - Statistics（標準ライブラリ）
  - Random（標準ライブラリ）

```julia
using Pkg
Pkg.add("Plots")
```

### Jupyter Notebook
ノートブックを実行するにはIJuliaが必要です：

```julia
using Pkg
Pkg.add("IJulia")
```

## 使い方

1. リポジトリをクローン：
```bash
git clone https://github.com/kkawailab/guide-for-noc-jl.git
cd guide-for-noc-jl
```

2. Juliaでパッケージをインストール：
```julia
using Pkg
Pkg.add(["Plots", "IJulia"])
```

3. Jupyter Notebookを起動：
```julia
using IJulia
notebook()
```

4. `notebooks/` フォルダ内のノートブックを開いて学習開始

## 参考資料

- [Nature of Code](https://natureofcode.com/) - Daniel Shiffman
- [The Coding Train](https://thecodingtrain.com/) - YouTube チャンネル
- [Julia Documentation](https://docs.julialang.org/)
- [Plots.jl Documentation](https://docs.juliaplots.org/)

## ライセンス

このリポジトリの内容は学習目的で作成されています。
オリジナルの「Nature of Code」はDaniel Shiffmanによるものです。
