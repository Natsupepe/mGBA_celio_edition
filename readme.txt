mGBA celio edition（64MB ROM 対応版）
==================================================

これは何か
----------
GBA エミュレーター mGBA の改造版「mGBA celio edition 2.0.0」に、
64MB（64MiB）の ROM を読めるようにする変更を加えたものです。

  - ちょうど 64MB の ROM を読み込むと、ROM の後ろ半分（32MB）が
    0x0A000000〜0x0BFFFFFF に見えます。
    0x08000000〜0x09FFFFFF と 0x0C000000〜0x0DFFFFFF は、これまでどおり前半の 32MB です。
  - 32MB 以下の ROM は、これまでの mGBA と同じように動きます。
  - celio edition の通信機能（Celio-mGBA-Link のスクリプト）は、2.0.0 と同じように使えます。

使い方
------
  1. このフォルダを、英数字だけのパスの場所に置いてください
     （例: C:\mGBA-rom64）。日本語の入ったパスだと通信機能がうまく動かないことがあります。
  2. mGBA.exe を起動し、ROM を開きます。
  3. フォルダの中の DLL やフォルダ（platforms など）は消さないでください。起動に必要です。

ROM・ゲームのデータは入っていません。

注意
----
  - 64MB の ROM の後ろ半分を使うゲームは、この mGBA でしか正しく動きません。
    ほかのエミュレーターや実機では、後ろ半分は読めません。
  - 動作の保証はありません。セーブデータは各自でバックアップしてください。

ソースコードとライセンス
------------------------
mGBA は Mozilla Public License 2.0（MPL-2.0）で公開されています。
この版のソースコード（変更を含む）は次の場所にあります。

  変更を加えたソース（rom64 ブランチ）:
    https://github.com/onikoro334274-cell/mGBA_celio_edition/tree/rom64
  元にした mGBA celio edition:
    https://github.com/Exormeter/mGBA_celio_edition
  mGBA 本家:
    https://mgba.io/
    https://github.com/mgba-emu/mgba

mGBA の著作権は Jeffrey Pfau ほか mGBA の開発者の皆さんにあります。
同梱の DLL（Qt・SDL・Lua など）は、それぞれのライセンスに従います。
