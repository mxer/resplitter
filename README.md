resplitter
==========

Splits all silence from a wav file and rejoin the chunks

Copyright
=========

  (C) 2011 Todd A Fisher <todd.fisher@gmail.com> and Ramon Martinez <rampa@encomix.org>

usage
=====
 resplitter -i infile.wav  -t 300 -d 0.1 -o outfile.wav

-b: how large of a buffer will impact how many frames we look at for each root means. larger byte buffer more frames are compressed into a single root means square
-i: the input wave audio file to split up by silence break points
-o: the output wave audio file with silence stripped if not specified, the same as input
-v 1: be Verbose
-t: a wave magnitude threshold e.g. anything greater than this value will be considered sound
-d: if a chunk is created and it is shorter than this length in time it will be discarded as noise
-D: if a chunk is created and is greater in length than it will be reprocessed using an increased threshold(t) and decreased byte buffer(b).
-w: can be nice to see the wave curve useful when trying to understand the audio file... cat out.audiowave | ruby plot.viz.rb && open out.wave.png

