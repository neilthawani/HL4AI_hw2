# Homework 2

### Use Foma to construct an analysis of these data in terms of context- dependent rewrite rules. You should submit the following items:

## 1. A README file with the following items:

### (a) A list of the underlying representations you posit for each root

| Root | Surface forms | Underlying representations |
| --- | --- | --- |
| daar | daar,daarta,daaro,house | daar,daarta,daaro |
| gees | gees,geesta,geeso,side | gees, geesta, geeso |
| laf | laf,lafta,lafo,bone | laf, lafta, lafo |
| lug | lug,lugta,luɣo,leg | lug, lugta, lugo |
| naag | naag,naagta,naaɣo,woman | naag, naagta, naago |
| tib | tib,tibta,tiβo,pestle | tib, tibta, tibo |
| sab | sab,sabta,saβo,outcast | sab, sabta, sabo |
| bad | bad,bada,baðo,sea | bad, badta, bado |
| d͡ʒid | d͡ʒid,d͡ʒida,d͡ʒiðo,person | d͡ʒid, d͡ʒidta, d͡ʒido |
| feeɖ | feeɖ,feeɖa,feeʐo,rib | feeɖ, feeɖta, feeɖo |
| ʕiir | ʕiir,ʕiirta,ʕiiro,buttermilk | ʕiir, ʕiirta, ʕiiro |
| ʔul | ʔul,ʔuʃa,ʔulo,stick | ʔul, ʔulta, ʔulo |
| bil | bil,biʃa,bilo,month | bil, bilta, bilo |
| meel | meel,meeʃa,meelo,place | meel, meelta, meelo |
| kaliil | kaliil,kaliiʃa,kaliilo,summer | kaliil, kaliilta, kaliilo |
| najl | najl,najʃa,najlo,female lamb | najl, najlta, najlo |
| sum | sun,sunta,sumo,poison | sum, sumta, sumo |
| laam | laan,laanta,laamo,branch | laam, laamta, laamo |
| sim | sin,sinta,simo,hip | sim, simta, simo |
| dan | dan,danta,dano,affair | dan, danta, dano |
| daan | daan,daanta,daano,river bank | daan, daanta, daano |
| saan | saan,saanta,saano,hide | saan, saanta, saano |
| nirg | nirig,nirigta,nirgo,babj female camel | nirg, nirgta, nirgo |
| gabɖ | gaβaɖ,gaβaɖa,gabɖo,girl | gabɖ, gabɖta, gabɖo |
| hogl | hoɣol,hoɣoʃa,hoglo,downpour | hogl, hoglta, hoglo |
| bagl | baɣal,baɣaʃa,baglo,mule | bagl, baglta, baglo |
| wah̵ar | wah̵ar,wah̵arta,wah̵aro,female kid | wah̵ar, wah̵arta, wah̵aro |
| irbad | irbad,irbada,irbaðo,needle | irbad, irbadta, irbado |
| kefed | kefed,kefeda,kefeðo,pan | kefed, kefedta, kefedo |
| d͡ʒilin | d͡ʒilin,d͡ʒilinta,d͡ʒilino,female dwarf | d͡ʒilin, d͡ʒilinta, d͡ʒilino |
| bohol | bohol,bohoʃa,boholo,hole | bohol, boholta, boholo |
| jird | jirid,jirida,jirdo,trunk | jird, jirdta, jirdo |
| ʔaajad | ʔaajad,ʔaajada,ʔaajaðo,miracle | ʔaajad, ʔaajadta, ʔaajado |
| gaʕm | gaʕan,gaʕanta,gaʕmo,hand | gaʕm, gaʕmta, gaʕmo |
| ʔinan | ʔinan,ʔinanta,ʔinano,daughter | ʔinan, ʔinanta, ʔinano |
| sug | suɣaj,sugtaj,sugnaj,wait | sugaj, sugtaj, sugnaj |
| kab | kaβaj,kabtaj,kabnaj,fix | kabaj, kabtaj, kabnaj |
| sid | siðaj,sidaj,sidnaj,carry | sidaj, sidtaj, sidnaj |
| dil | dilaj,diʃaj,dillaj,kill | dilaj, diltaj, dilnaj |
| gan | ganaj,gantaj,gannaj,aim | ganaj, gantaj, gannaj |
| tum | tumaj,tuntaj,tunnaj,hammer | tumaj, tumtaj, tumnaj |
| arg | argaj,aragtaj,aragnaj,see | argaj, argtaj, argnaj |
| gud | gudbaj,guðubtaj,guðubnaj,cross a river | gudbaj, gudbtaj, gudbnaj |
| qosl | qoslaj,qosoʃaj,qosollaj,laugh | qoslaj, qosltaj, qoslnaj |
| hadl | hadlaj,haðaʃaj,haðallaj,talk | hadlaj, hadltaj, hadlnaj |

### (b) A list of the underlying representations for each suffix

| sg | sg def | pl | 3 sg masc | 3 sg fem | 1 pl past |
| --- | --- | --- | --- | --- | --- |
| 0 | ta | o | aj | taj | naj |

### (c) Any special notes necessary to understand your implementation

I started by noticing patterns in the data set - plosive/fricative alternations, nasal consonant transformations, lateral consonant assimilation, and vowel insertions or deletions. After some trial and error, I think I got the rule order correct.

Vowel insertion was counterintuitive in this data set, but eventually, I found some conditions for insertion AND deletion, and realized that consonant-vowel alternations were apparent in the surface forms of the nouns and verbs in this data set. When consonants appear adjacent to each other before a suffix that begins with a consonant, a vowel is inserted between the two initial consonants. This pattern proved to be the correct choice.

It made more sense for plosives to turn into fricatives between two vowels, and the remainder of the rules in the FST entailed smoothing nasals and assimilation of affixes.

## 2. A Foma script (somali.xsft) defining an FST that transduces between Somali underlying representations and surface representations (like those in the data tables)

See attached file.

## 3. Two lists of test-cases (1 test case per line):

### (a) Underlying representations to be transduced into surface representations.

nirg

nirgta

nirgo

gabɖ

gabɖta

gabɖo

bad

badta

bado

sum

sumta

sumo

gudbaj

gudbtaj

gudbnaj

najl

najlta

najlo

gaʕm

gaʕmta

gaʕmo

### (b) Surface representations to be transduced into underlying representations.

nirig

nirigta

nirgo

gaβaɖ

gaβaɖa

gabɖo

bad

bada

baðo

sun

sunta

sumo

gudbaj

guðubtaj

guðubnaj

najl

najʃa

najlo

gaʕan

gaʕanta

gaʕmo
