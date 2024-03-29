# FF7 キャラクターマッチング

## 紹介
FF7の世界観を背景に自分のキャラメイキングをして、作成したキャラクターがFF7の登場キャラクターの誰に一番近いタイプかを表示するマッチング機能を実装。

## 工夫したところ
データベースから取得したデータをPHP側で計算して配列をするところを工夫した。卒業制作で予定している実際のマッチングアプリもＡパラメーターとＢパラメーターを比較してマッチングをかけることを前提としているため、これはそのプロトタイプとなることをイメージ。現状のデータベースは小さいが、基本構造はほぼ同じとなる予定のため、サイズ感を大きくしてマッチングの理論を大規模データベース用にバージョンアップしていくイメージでいる。またデータベースＡ・Ｂともに全ての行について差分計算がかかる状態なので、これが大規模になったときにレスポンスに影響する可能性が高いことから、計算ロジックと計算領域の限定など課題感はある状況。

## 苦戦したところ
工夫した計算のところが最も苦戦した。実のところ、計算まではできているが、所定の条件に見合うキャラクター名を表示する部分が、どんな値でも同じキャラクターが表示されてしまう現象を解決できていない。この部分を解決できればプロトタイプとしては完成するが苦戦中。