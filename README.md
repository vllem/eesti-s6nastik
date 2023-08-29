# eesti-sõnastik
see on väga lihtne bash script, et luua .txt fail, milles on [eesti sõnastik](http://www.meso.ee/~jjpp/speller/). <br>
laadige alla ja chmod +x eesti_sõnastik <br>
sul on vaja: <br>
- [wget](https://en.wikipedia.org/wiki/Wget) (kasutame, et allalaadida .dic ja .aff fail)
- [iconv](https://en.wikipedia.org/wiki/Iconv) (kasutame, et viia ISO-8859-1 encoding üle UTF-8 encodinguks)
- [g++](https://gcc.gnu.org/) (kasutame, et kompileerida [unmunch](https://github.com/hunspell/hunspell/tree/master/src/tools) programm)
- [sed](https://en.wikipedia.org/wiki/Sed) (kastutame, et saada lahti lollidest tähtedest) <br>
## teatud probleemid
seda viga saab parandada avades faili oma text editoris ja minnes "asenda_lollid_t2hed" funktsiooni juurde ja uncommentides 2 liini koodi ja pannes kommenaaridesse 2 teist.
- linuxil töötab: sed -i -e 's/þ/ž/g' et_EE_sõnastik.txt && sed -i -e 's/ð/š/g' et_EE_sõnastik.txt
- macil töötab: sed -i '' 's/þ/ž/g' et_EE_sõnastik.txt && sed -i '' 's/ð/š/g' et_EE_sõnastik.txt
