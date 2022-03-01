# 国内株式投資信託における非線形関係の可視化分析

## 研究概要
投資信託の資金流出入においては、運用パフォーマンスの良いファンドは資金が流出してしまうというような不思議な現象が度々確認されてきました。  
本研究の目的は大きく2つです。
1つは従来線形分析がメインだった投資信託の資金フロー分析に非線形分析を適用して精度を高めること。
もう１つは、今まで極めて曖昧だった関係を可視化することでどのような影響があるのかを明確にすることです。

## 入力データについて

本研究で最も標準的な国内株式投資信託を分析対象としています。  
使用した実際のファンドデータは規約により配布できないため、本レポジトリには含まれていません。

## 実行環境

macOSで開発していますが、windowsでも動作確認済みです。

## コードの概略

- Script/allterm/flow_lightgbm_allterm.ipynb: 全期間に渡って対象ファンドの特性が資金フローにどのように影響を与えているかをLightgbm+SHAPで可視化できます。 
資金流出/流入はmodeで切り替えることができます。　


- Script/eachterm/flow_lightgbm_term1.ipynb: 期間を指定して対象ファンドの特性が資金フローにどのように影響を与えているかをLightgbm+SHAPで可視化できます。期間をスライドしていくことで時系列推移を確認できます。資金流出/流入はmodeで切り替えることができます。  
(flow_lightgbm_term2.ipynb, flow_lightgbm_term3.ipynb,flow_lightgbm_term4.ipynb,flow_lightgbm_term5.ipynb, flow_lightgbm_term6.ipynbも同様)


- Script/target_funds/search&visualize_target_funds.ipynb: ファンドの運用方針に特定の単語が含まれるファンドを抽出し、それらファンド群を全体の中で強調表示することができます。　本研究ではESG関連ファンドを対象としていますが、テクノロジーや医療など様々な単語をキーワードに設定し、特定ファンドの特徴を視覚的に確認することができます。


## リンク

- 使用データの入手先: https://www.abic.co.jp/homepage/products/fundmonitor.html
