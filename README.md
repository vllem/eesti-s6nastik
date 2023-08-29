# eesti_sõnastik

see on väga lihtne bash script, et luua .txt fail, milles on [eesti sõnastik](http://www.meso.ee/~jjpp/speller/). <br>
sul on vaja: <br>
- [wget](https://en.wikipedia.org/wiki/Wget) 
- [iconv](https://en.wikipedia.org/wiki/Iconv) 
- [g++](https://gcc.gnu.org/)
- [sed](https://en.wikipedia.org/wiki/Sed) 
kui sul on unix süsteem siis sul peaks juba paljud need programmid olemas olema.
- **wget-i** kasutame, et allalaadida .dic ja .aff failid.
- **iconv-i** kasutame, et viia ISO-8859-1 encoding üle UTF-8 encodinguks.
- **g++** kasutame, et kompileerida [unmunch](https://github.com/hunspell/hunspell/tree/master/src/tools) programm.
- **sed-i** kastutame, et saada lahti lollidest tähtedest.
## teatud probleemid
macil peab kasutama sed-i teisti. macil peab olema 
> sed -i -e 's/þ/ž/g' et_EE_sõnastik.txt && sed -i -e 's/ð/š/g' et_EE_sõnastik.txt
asemel 
> sed -i '' 's/þ/ž/g' et_EE_sõnastik.txt && sed -i '' 's/ð/š/g' et_EE_sõnastik.txt
seda viga saab parandada avades faili oma text editoris ja minnes "asenda_lollid_t2hed" funktsiooni juurde ja uncommentides 2 liini koodi ja pannes kommenaaridesse 2 teist.
