# このソフトウェアについて

平均律12音、純正律7音、ピタゴラス音律12音の構成音とコードを鳴らしてみた。

432,440,444Hzを基音として。

# 対象ファイル名

ファイル名|説明
----------|----
makeTemperamentAndChord.py|平均律12音、純正律7音、ピタゴラス音律12音の構成音とコードの音声ファイルを出力する
MusicTheory/temperament/JustIntonation.py|純正律により基音から7音を算出する
MusicTheory/temperament/EqualTemperament.py|平均律により基音から12音を算出する
MusicTheory/temperament/PythagoreanTuning.py|ピタゴラス音律により基音から12音を算出する

# 実行

```sh
$ python makeTemperamentAndChord.py 
---------- EqualTemperament ----------
BaseFrequency: 432 Hz
[432.0, 457.68805676321557, 484.90360486964914, 513.7374736811755, 544.2858935545852, 576.6508170014548, 610.9402589451771, 647.2686572107264, 685.7572544502622, 726.5345027792093, 769.7364924732532, 815.5074061569832]
BaseFrequency: 440 Hz
[440.0, 466.1637615180899, 493.8833012561241, 523.2511306011972, 554.3652619537442, 587.3295358348151, 622.2539674441618, 659.2551138257398, 698.4564628660078, 739.9888454232688, 783.9908719634985, 830.6093951598903]
BaseFrequency: 444 Hz
[444.0, 470.40161389552713, 498.3731494493616, 528.0079590612081, 559.4049461533237, 592.6688952514953, 627.9108216936543, 665.2483421332466, 704.8060670738805, 746.7160167452985, 791.1180617086213, 838.1603896613437]
---------- JustIntonation ----------
BaseFrequency: 432 Hz
[432, 486.0, 540.0, 576.0, 648.0, 720.0, 810.0]
BaseFrequency: 440 Hz
[440, 495.0, 550.0, 586.6666666666666, 660.0, 733.3333333333334, 825.0]
BaseFrequency: 444 Hz
[444, 499.5, 555.0, 592.0, 666.0, 740.0, 832.5]
---------- PythagoreanTuning ----------
BaseFrequency: 432 Hz
[432, 455.111111111111, 486.0, 511.9999999999999, 546.75, 576.0, 615.09375, 648.0, 682.6666666666665, 729.0, 768.0, 820.125]
BaseFrequency: 440 Hz
[440, 463.5390946502056, 495.0, 521.4814814814814, 556.875, 586.6666666666666, 626.484375, 660.0, 695.3086419753085, 742.5, 782.2222222222222, 835.3125]
BaseFrequency: 444 Hz
[444, 467.75308641975295, 499.5, 526.2222222222221, 561.9375, 592.0, 632.1796875, 666.0, 701.6296296296294, 749.25, 789.3333333333333, 842.90625]
```

音が再生される。また、`res/`配下に音声ファイルが出力される。

# 課題

* 純正律における中間の5音も算出したい。計算方法がよくわからない。C#とDbが別の音になるらしい。意味不明。
* 12平均律の和音を鳴らして比較したい

# 開発環境

* Linux Mint 17.3 MATE 32bit
* [libav](http://ytyaru.hatenablog.com/entry/2018/08/24/000000)
    * [各コーデック](http://ytyaru.hatenablog.com/entry/2018/08/23/000000)
* [pyenv](https://github.com/pylangstudy/201705/blob/master/27/Python%E5%AD%A6%E7%BF%92%E7%92%B0%E5%A2%83%E3%82%92%E7%94%A8%E6%84%8F%E3%81%99%E3%82%8B.md) 1.0.10
    * Python 3.6.1
        * [pydub](http://ytyaru.hatenablog.com/entry/2018/08/25/000000)
        * [PyAudio](http://ytyaru.hatenablog.com/entry/2018/07/27/000000) 0.2.11
            * [ALSA lib pcm_dmix.c:1022:(snd_pcm_dmix_open) unable to open slave](http://ytyaru.hatenablog.com/entry/2018/07/29/000000)
        * [matplotlib](http://ytyaru.hatenablog.com/entry/2018/07/22/000000)
            * [matplotlibでのグラフ表示を諦めた](http://ytyaru.hatenablog.com/entry/2018/08/05/000000)

# 参考

感謝。

## 440Hz, 432Hz

* http://tabi-labo.com/156689/music-a432

## 和音の生成

* http://ism1000ch.hatenablog.com/entry/2013/11/15/182442
* https://ja.wikipedia.org/wiki/%E4%B8%89%E5%92%8C%E9%9F%B3
* https://ja.wikipedia.org/wiki/%E3%83%91%E3%83%AF%E3%83%BC%E3%82%B3%E3%83%BC%E3%83%89

## 音名

* https://ja.wikipedia.org/wiki/%E9%9F%B3%E5%90%8D%E3%83%BB%E9%9A%8E%E5%90%8D%E8%A1%A8%E8%A8%98

## 音階

* https://ja.wikipedia.org/wiki/%E9%9F%B3%E9%9A%8E

### 五度圏

* http://dn-voice.info/music-theory/godoken/

## 音高の算出

* http://www.asahi-net.or.jp/~HB9T-KTD/music/Japan/Research/DTM/freq_map.html
* http://www.nihongo.com/aaa/chigaku/suugaku/pythagoras.htm

## サイン波のスピーカ再生

* http://www.non-fiction.jp/2015/08/17/sin_wave/
* http://aidiary.hatenablog.com/entry/20110607/1307449007
* http://ism1000ch.hatenablog.com/entry/2013/11/15/182442

# ライセンス

このソフトウェアはCC0ライセンスである。

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)

Library|License|Copyright
-------|-------|---------
[pydub](https://github.com/jiaaro/pydub)|[MIT](https://github.com/jiaaro/pydub/blob/master/LICENSE)|[Copyright (c) 2011 James Robert, http://jiaaro.com](https://github.com/jiaaro/pydub/blob/master/LICENSE)
[pygame](http://www.pygame.org/)|[LGPL](https://www.pygame.org/docs/)|[pygame](http://www.pygame.org/)

