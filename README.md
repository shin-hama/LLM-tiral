# LLM お試し

日本語対応しているモデル一覧
具体的に GPU がどれだけ必要かわからないので、一個ずつ試してみる

- <https://huggingface.co/tokyotech-llm/Swallow-13b-instruct-hf>
  - [llam2](https://github.com/facebookresearch/llama/blob/main/LICENSE)
    - 月間7億アクティブユーザー以上の場合は有料
- <https://huggingface.co/pfnet/plamo-13b>
  - apache2.0
- <https://huggingface.co/elyza/ELYZA-japanese-Llama-2-13b-instruct>
  - [llam2](https://github.com/facebookresearch/llama/blob/main/LICENSE)

使ってみたら Swallow 以外まともに英訳してくれないので Swallow を使うことにする

## 日英変換の例があるモデル

- <https://huggingface.co/Helsinki-NLP/opus-mt-ja-en>
  - 日英変換特化のモデル
  - apache2.0
  - サンプルの結果はいい感じ
- <https://huggingface.co/CohereForAI/aya-101>
  - `Translate to English: {ja_text}`
  - 精度良い
  - 長文がやや苦手
  - モデルがかなりでかいので色々と時間がかかる
- <https://huggingface.co/SnypzZz/Llama2-13b-Language-translate>
  - 英語に翻訳されない
- <https://huggingface.co/facebook/m2m100_1.2B>
  - 精度良い
  - 処理が早い
  - html タグが残るが不完全なのでいっそ無視したほうがいいかもしれない
  - [12B model](https://huggingface.co/facebook/m2m100-12B-avg-5-ckpt) も存在するが、動かすのにメモリ 90 GB 以上必要とのことなので、こちらはスキップ
    - 量子化すれば使えるかも
- <https://huggingface.co/webbigdata/ALMA-7B-Ja-V2>
  - llama2
  - 日英の相互変換が可能なモデル
  - サンプル: <https://colab.research.google.com/github/webbigdata-jp/python_sample/blob/main/ALMA_7B_Ja_V2_Free_Colab_sample.ipynb>
- <https://huggingface.co/facebook/mbart-large-50-many-to-many-mmt>
  - m2m100_1.2B と同じくらいの精度･速度

## text generation の設定について

以下が参考になりそう

- [Transformers の generate()のテキスト生成戦略](https://note.com/npaka/n/n9a8c85f2ef7a)
- [Huggingface Transformers 入門 (6) - テキスト生成](https://note.com/npaka/n/n5d296d8ae26d)
