# Forensicsについて
## ジャンル一覧
### 画像系（PNG,JPG,GIF)
- PNGは可逆圧縮、JPGは非可逆圧縮だからJPGは解析が難しい
- JPGはexifや別ファイルが埋め込まれている問題が多い
- PNGはexifや別ファイルが埋め込まれている問題と、LSBや画像修復(IHDR,IDAT,IEND)の問題が多い
- ファイル埋め込みはたいてい`binwalk`で抽出できる
- LSBは色情報がどう取り扱われているかを知れば簡単（PNG...RGB(A)方式  BMP=BGR(A)方式 GIF...index-Palett方式）
- LSBには文字を埋め込めたり、場合によってはQRコードを埋め込めたりもできる
  
### 音声系（WAV)
