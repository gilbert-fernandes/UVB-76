# UVB-76
Tools to run a number-station

This project contains three components :

- Codegroup
- OTPgen^XOR
- CG2Ruski

   [clear text]  ->
   [compression] -> [OTPgen^XOR]
-> [Codegroup]   -> [CG2Ruski]
.......................................................................
Clear text will be compressed, then XORed with random OTP data from a
radio-active/secure random source, using Vigenère/One-time pad
encryption.

Resulting encryption is encoded into 5-letter groups, then translated
into Russian spelling alphabet and radio-transmitted the same way the
current number-stattions are by the Служба внешней разведки Российской
Федерации to communicate with its spies on the AM-band :-)

I won't go as far as using 4625/6998 KHz as my transmitter frequency,
as I prefer to order my Earl Grey tea with brown-sugar in place of the
albeit tastier polonium-210.

1/3 - Codegroup

  This is a rewrite, in Java, of the program CODEGROUP written in 2008
  by John Walker (www.fourmilab.ch).

  CODEGROUP is a program (originally in C) that encodes and decodes
  arbitrary data into five-letter groups, which has been the traditional
  encoding for spies when transmitting messages (itself coming from the
  telegraphic use of grouping letters by five to ease writing them down
  when transmitted by Morse code).

  This rewrite uses the same console parameters, and encodes/decodes
  files as the original program did with the same 16-bit CRC.

  This program is dedicated to John Walker, whom I consider to be the
  author of the first computer virus, which was born the same as I did
  in 1974 : the ANIMAL virus that self-replicated on the UNIVAC 1100
  machines (he became famous afterwards for co-founding an obscure
  company called AutoDesk which published a confidential program called
  AutoCAD that you may have heard of...)

  [this will be coded first]

2/3 - OTPgen^XOR

  Not ready for ingestion yet. This program will have to parts :
  a hardware-based random source ; ideally from something radio-active
  but I will probably settle with a reverse-biased semiconductor junction,
  and data will be fed into a program that will check for quality of bits
  using FIPS-140-2.

[this will be coded last]

3/3 - CG2Ruski

  This program will read codegroup files and produce a sound-phonetic
  version of it, using the Russian spelling alphabet. With output to
  either sound or sound-file.

  [this will be coded second]
