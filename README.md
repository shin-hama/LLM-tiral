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
- <https://huggingface.co/SnypzZz/Llama2-13b-Language-translate>
- <https://huggingface.co/facebook/m2m100_1.2B>
- <https://huggingface.co/webbigdata/ALMA-7B-Ja-V2>
  - llama2
  - 日英の相互変換が可能なモデル
  - サンプル: <https://colab.research.google.com/github/webbigdata-jp/python_sample/blob/main/ALMA_7B_Ja_V2_Free_Colab_sample.ipynb>
- <https://huggingface.co/facebook/mbart-large-50-many-to-many-mmt>
