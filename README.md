# proximityOSC-Patches

#N canvas 40 23 1858 1003 10;
#X obj 24 63 gemhead;
#X obj 24 86 pix_video;
#X obj 24 108 pix_grey;
#X obj 24 580 pix_texture;
#X obj 24 640 rectangle 6 4;
#X floatatom 207 207 5 0 0 0 - - -;
#X floatatom 462 223 5 0 0 0 - - -;
#X floatatom 614 216 5 0 0 0 - - -;
#X obj 625 126 gemwin;
#X msg 625 91 create \, 1;
#X msg 696 91 0 \, destroy;
#X msg 778 93 dimen 320 240;
#X obj 24 133 pix_blob 4;
#X obj 570 457 osc~ 118.344;
#X obj 598 479 osc~ 119;
#X obj 4 87 tgl 15 0 empty empty empty 17 7 0 10 -262144 -1 -1 0 1
;
#X obj 490 299 vsl 15 128 -1000 1000 0 0 empty empty empty 0 -9 0 10
-262144 -1 -1 10795 1;
#X obj 231 297 hsl 128 15 -1000 1000 0 0 empty empty empty -2 -8 0
10 -262144 -1 -1 10160 1;
#X floatatom 227 266 5 0 0 0 - - -;
#X obj 227 241 * 100;
#X obj 490 255 * 100;
#X floatatom 490 276 5 0 0 0 - - -;
#X text 186 205 X;
#X text 443 221 Y;
#X text 579 216 SIZE;
#X floatatom 650 268 5 0 0 0 - - -;
#X obj 650 247 * 100;
#X obj 653 289 hsl 128 15 0 127 0 0 empty empty empty -2 -8 0 10 -262144
-1 -1 12700 1;
#X msg 36 179 gemList;
#X msg 93 108 <mode>;
#X msg 152 109 <color-weights>;
#X obj 168 439 osc~ 145.655;
#X obj 195 460 osc~ 146;
#X obj 401 450 osc~ 173.505;
#X obj 427 470 osc~ 174;
#X obj 588 248 * 10000;
#X msg 803 924 stop;
#X obj 464 664 *~ 0.5;
#X obj 240 711 equal_power_pan~;
#X obj 255 679 *~ 0.5;
#X obj 444 695 gogins_pan~;
#X obj 899 911 freeverb~;
#X msg 938 156 roomsize \$1;
#X msg 938 201 damping \$1;
#X msg 940 253 width \$1;
#X msg 940 297 wet \$1;
#X msg 940 341 dry \$1;
#X msg 1056 351 print;
#X msg 1051 267 freeze \$1;
#X msg 1052 318 bypass \$1;
#X obj 1052 299 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 0
1;
#X obj 1051 247 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 0
1;
#X obj 952 318 hsl 60 18 0 1 0 1 empty empty dry 2 9 1 12 -225271 -1
-1 900 0;
#X obj 952 274 hsl 60 18 0 1 0 1 empty empty wet 2 9 1 12 -225271 -1
-1 4000 0;
#X obj 950 222 hsl 60 18 0 1 0 1 empty empty width 2 9 1 12 -262131
-1 -1 3900 0;
#X obj 950 178 hsl 60 18 0 2 0 1 empty empty damping 2 9 1 12 -261689
-1 -1 1700 0;
#X obj 955 132 hsl 60 18 0.11 1.1 0 1 empty empty roomsize 2 9 1 12
-261689 -1 -1 4200 0;
#X floatatom 920 137 3 0 0 0 - - -;
#X floatatom 920 182 3 0 0 0 - - -;
#X floatatom 920 227 3 0 0 0 - - -;
#X floatatom 922 278 3 0 0 0 - - -;
#X floatatom 922 322 3 0 0 0 - - -;
#X obj 810 466 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X obj 883 467 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 810 531 freeze \$1;
#X obj 810 512 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 0
1;
#X msg 883 532 freeze \$1;
#X obj 883 513 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 0
1;
#X obj 810 490 metro 3500;
#X obj 883 489 metro 3500;
#X obj 957 465 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X obj 1030 466 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 957 530 freeze \$1;
#X obj 957 511 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 0
1;
#X msg 1030 531 freeze \$1;
#X obj 1030 512 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 0
1;
#X obj 957 489 metro 1500;
#X obj 1108 893 writesf~ 2;
#X msg 1375 873 start;
#X msg 1230 823 stop;
#X msg 1189 823 print;
#X text 1219 868 1;
#X text 1358 869 2;
#X obj 1030 488 metro 1500;
#X obj 774 558 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X obj 847 559 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 774 623 freeze \$1;
#X obj 774 604 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X msg 847 624 freeze \$1;
#X obj 847 605 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X obj 774 582 metro 5000;
#X obj 847 581 metro 5000;
#X obj 949 563 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X obj 1022 564 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 949 628 freeze \$1;
#X obj 949 609 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X msg 1022 629 freeze \$1;
#X obj 1022 610 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X obj 949 587 metro 1000;
#X obj 1022 586 metro 1000;
#X obj 1056 986 delread~ delayRight 1500;
#X obj 1058 1010 delread~ delayLeft 1000;
#X text 1228 843 CAMBIAR NOMBRE FICHERO CADA NUEVA REC.;
#X obj 1191 466 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 1191 531 freeze \$1;
#X obj 1191 512 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X obj 1183 564 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 1183 629 freeze \$1;
#X obj 1183 610 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X obj 1183 586 metro 1000;
#X obj 1121 468 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 1121 533 freeze \$1;
#X obj 1121 514 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X obj 1113 566 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 1113 631 freeze \$1;
#X obj 1113 612 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X obj 1113 588 metro 1000;
#X obj 1121 490 metro 5000;
#X obj 1191 488 metro 5000;
#X obj 1339 466 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 1339 531 freeze \$1;
#X obj 1339 512 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 0
1;
#X obj 1331 564 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 1331 629 freeze \$1;
#X obj 1331 610 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X obj 1331 586 metro 1000;
#X obj 1269 468 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 1269 533 freeze \$1;
#X obj 1269 514 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 0
1;
#X obj 1261 566 bng 15 250 50 0 empty empty empty 17 7 0 10 -262144
-1 -1;
#X msg 1261 631 freeze \$1;
#X obj 1261 612 tgl 15 0 empty empty empty 0 -6 0 8 -262144 -1 -1 1
1;
#X obj 1261 588 metro 1000;
#X obj 1269 490 metro 6000;
#X obj 1339 488 metro 6000;
#X obj 908 970 dac~ 1 2;
#X obj 1066 946 delwrite~ delayLeft 8000;
#X obj 1064 922 delwrite~ delayRight 8000;
#X obj 167 522 *~ 0.1;
#X obj 166 492 phasor~ 0.25;
#X obj 400 507 phasor~ 0.2;
#X obj 399 532 *~ 0.1;
#X obj 561 507 *~ 0.1;
#X obj 568 687 equal_power_pan~;
#X obj 600 656 *~ 0.5;
#X msg 1237 871 open LCE1.wav;
#X floatatom 86 295 5 0 0 0 - - -;
#X obj 168 247 * 1000;
#X obj 401 250 * 1000;
#X text 154 265 output;
#X text 155 418 input;
#X text 160 544 output;
#X text 215 694 input;
#X connect 0 0 1 0;
#X connect 1 0 2 0;
#X connect 2 0 12 0;
#X connect 3 0 4 0;
#X connect 5 0 19 0;
#X connect 5 0 147 0;
#X connect 6 0 20 0;
#X connect 6 0 148 0;
#X connect 7 0 26 0;
#X connect 7 0 35 0;
#X connect 9 0 8 0;
#X connect 10 0 8 0;
#X connect 11 0 8 0;
#X connect 12 0 3 0;
#X connect 12 0 28 0;
#X connect 12 1 5 0;
#X connect 12 2 6 0;
#X connect 12 3 7 0;
#X connect 13 0 142 0;
#X connect 14 0 142 0;
#X connect 15 0 2 0;
#X connect 16 0 40 1;
#X connect 17 0 38 1;
#X connect 18 0 17 0;
#X connect 19 0 18 0;
#X connect 20 0 21 0;
#X connect 21 0 16 0;
#X connect 25 0 27 0;
#X connect 26 0 25 0;
#X connect 27 0 62 0;
#X connect 27 0 63 0;
#X connect 27 0 70 0;
#X connect 27 0 71 0;
#X connect 27 0 110 0;
#X connect 27 0 103 0;
#X connect 27 0 126 0;
#X connect 27 0 119 0;
#X connect 29 0 12 1;
#X connect 30 0 12 2;
#X connect 31 0 139 0;
#X connect 32 0 139 0;
#X connect 33 0 140 0;
#X connect 34 0 140 0;
#X connect 35 0 13 0;
#X connect 36 0 41 0;
#X connect 37 0 40 0;
#X connect 38 0 41 0;
#X connect 38 1 41 1;
#X connect 39 0 38 0;
#X connect 40 0 41 0;
#X connect 40 1 41 1;
#X connect 41 0 77 0;
#X connect 41 0 135 0;
#X connect 41 0 136 0;
#X connect 41 1 77 1;
#X connect 41 1 135 1;
#X connect 41 1 137 0;
#X connect 42 0 41 0;
#X connect 43 0 41 0;
#X connect 44 0 41 0;
#X connect 45 0 41 0;
#X connect 46 0 41 0;
#X connect 47 0 41 0;
#X connect 48 0 41 0;
#X connect 49 0 41 0;
#X connect 50 0 49 0;
#X connect 51 0 48 0;
#X connect 52 0 46 0;
#X connect 52 0 61 0;
#X connect 53 0 45 0;
#X connect 53 0 60 0;
#X connect 54 0 44 0;
#X connect 54 0 59 0;
#X connect 55 0 43 0;
#X connect 55 0 58 0;
#X connect 56 0 42 0;
#X connect 56 0 57 0;
#X connect 62 0 68 0;
#X connect 62 0 84 0;
#X connect 63 0 69 0;
#X connect 63 0 85 0;
#X connect 64 0 41 0;
#X connect 65 0 64 0;
#X connect 66 0 41 0;
#X connect 67 0 66 0;
#X connect 68 0 65 0;
#X connect 69 0 67 0;
#X connect 70 0 76 0;
#X connect 70 0 92 0;
#X connect 71 0 83 0;
#X connect 71 0 93 0;
#X connect 72 0 41 0;
#X connect 73 0 72 0;
#X connect 74 0 41 0;
#X connect 75 0 74 0;
#X connect 76 0 73 0;
#X connect 78 0 77 0;
#X connect 79 0 77 0;
#X connect 80 0 77 0;
#X connect 83 0 75 0;
#X connect 84 0 90 0;
#X connect 85 0 91 0;
#X connect 86 0 41 0;
#X connect 87 0 86 0;
#X connect 88 0 41 0;
#X connect 89 0 88 0;
#X connect 90 0 87 0;
#X connect 91 0 89 0;
#X connect 92 0 98 0;
#X connect 93 0 99 0;
#X connect 94 0 41 0;
#X connect 95 0 94 0;
#X connect 96 0 41 0;
#X connect 97 0 96 0;
#X connect 98 0 95 0;
#X connect 99 0 97 0;
#X connect 100 0 77 1;
#X connect 100 0 135 1;
#X connect 101 0 77 0;
#X connect 101 0 135 0;
#X connect 103 0 106 0;
#X connect 103 0 118 0;
#X connect 105 0 104 0;
#X connect 106 0 109 0;
#X connect 107 0 41 0;
#X connect 108 0 107 0;
#X connect 109 0 108 0;
#X connect 110 0 113 0;
#X connect 110 0 117 0;
#X connect 112 0 111 0;
#X connect 113 0 116 0;
#X connect 114 0 41 0;
#X connect 115 0 114 0;
#X connect 116 0 115 0;
#X connect 117 0 112 0;
#X connect 118 0 105 0;
#X connect 119 0 122 0;
#X connect 119 0 134 0;
#X connect 121 0 120 0;
#X connect 122 0 125 0;
#X connect 123 0 41 0;
#X connect 124 0 123 0;
#X connect 125 0 124 0;
#X connect 126 0 129 0;
#X connect 126 0 133 0;
#X connect 128 0 127 0;
#X connect 129 0 132 0;
#X connect 130 0 41 0;
#X connect 131 0 130 0;
#X connect 132 0 131 0;
#X connect 133 0 128 0;
#X connect 134 0 121 0;
#X connect 138 0 38 0;
#X connect 139 0 138 0;
#X connect 140 0 141 0;
#X connect 141 0 40 0;
#X connect 142 0 143 0;
#X connect 143 0 41 0;
#X connect 143 1 41 1;
#X connect 144 0 143 0;
#X connect 145 0 77 0;
#X connect 147 0 31 0;
#X connect 148 0 33 0;
