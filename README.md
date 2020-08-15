# OCRのOSSを試してみた。
その結果など ↓

## CRAFT
- GPU環境でないと、エラーで実行出来ない。
  - （できるようにする方法はあるっぽい）
    ```
    RuntimeError: Attempting to deserialize object on a CUDA device but torch.cuda.is_available() is False. If you are running on a CPU-only machine, please use torch.load with map_location=torch.device('cpu') to map your storages to the CPU.
    ```
- 実行
  - 学習済みモデルをダンロードする。
    - [LinkRefiner (CTW1500)](https://drive.google.com/file/d/1XSaFwBkOaFOdtk4Ane3DFyJGPRw6v5bO/view)  など。
    - 詳しくは、本家の README を参照。
  - `CRAFT-pytorch/models/` にコピーする。
  - スクリプトを実行。
    ```
    python3 test.py  --trained_model=models/craft_refiner_CTW1500.pth   --test_folder=datasets/myData/
    ```
- 結果
  - 前回試した時のデータを間違って消してしまった...ので、現在やり直し中...。
  - 新しい技術は出てきてるので、諦めて後回しにするかも...。

- 実行時間など(未)

## Tesseract 5 (未)


## OCR_Japanease (未)


___
___

# 使わせてもらったリポジトリなど
## 概要
- Git の submodule 機能を使って取り込んでいる。
- install
  ```
  $ git submodule update -i
  ```

## CRAFT
- 本家[GitHub](git@github.com:clovaai/CRAFT-pytorch.git)
- README : [CRAFT/README.md](CRAFT/README.md)

## Tesseract 5 (未)
- 本家[GitHub](https://github.com/tesseract-ocr/tesstrain)

## OCR_Japanease (未)
- 本家[GitHub](https://github.com/tanreinama/OCR_Japanease)
- 解説記事
  - [日本語OCRを作ったので解説してみる](https://qiita.com/tanreinama/items/8fc1c8af6554654aae00)



