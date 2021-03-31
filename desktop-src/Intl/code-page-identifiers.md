---
description: En la tabla siguiente se definen los identificadores de página de códigos disponibles.
ms.assetid: 5d6fc86a-f205-4d14-bb7c-ecd71682e0fe
title: Identificadores de páginas de códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb0482247313e8d61d61d7d3178906536ab9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154154"
---
# <a name="code-page-identifiers"></a>Identificadores de páginas de códigos

En la tabla siguiente se definen los identificadores de página de códigos disponibles.

> [!Note]  
> Las páginas de códigos ANSI pueden ser diferentes en distintos equipos o se pueden cambiar para un único equipo, lo que provoca daños en los datos. Para obtener los resultados más coherentes, las aplicaciones deben usar Unicode, como UTF-8 o UTF-16, en lugar de una página de códigos específica.

 



| Identificador | Nombre de .NET               | Información adicional                                                                              |
|------------|-------------------------|-----------------------------------------------------------------------------------------------------|
| 037        | IBM037                  | US-Canada IBM EBCDIC                                                                                |
| 437        | IBM437                  | Estados Unidos OEM                                                                                   |
| 500        | IBM500                  | IBM EBCDIC International                                                                            |
| 708        | ASMO-708                | Árabe (ASMO 708)                                                                                   |
| 709        |                         | Árabe (ASMO-449 +, BCON v4)                                                                         |
| 710        |                         | Árabe transparente Árabe                                                                         |
| 720        | DOS: 720                 | Árabe (transparente ASMO); Árabe (DOS)                                                             |
| 737        | ibm737                  | OEM griego (anteriormente 437G); Griego (DOS)                                                              |
| 775        | ibm775                  | OEM Báltico; Báltico (DOS)                                                                            |
| 850        | ibm850                  | Latin multilingüe de OEM 1; Europeo occidental (DOS)                                                    |
| 852        | ibm852                  | OEM latín 2; Centroeuropeo (DOS)                                                                 |
| 855        | IBM855                  | OEM cirílico (principalmente ruso)                                                                    |
| 857        | ibm857                  | OEM Turco; Turco (DOS)                                                                          |
| 858        | IBM00858                | Símbolo Latino multilingüe de OEM 1 + euro                                                              |
| 860        | IBM860                  | Portugués de OEM; Portugués (DOS)                                                                    |
| 861        | ibm861                  | Islandés OEM; Islandés (DOS)                                                                      |
| 862        | DOS: 862                 | Hebreo del OEM; Hebreo (DOS)                                                                            |
| 863        | IBM863                  | OEM francés canadiense; Canadiense francés (DOS)                                                          |
| 864        | IBM864                  | OEM Árabe; Árabe (864)                                                                            |
| 865        | IBM865                  | OEM Nordic; Nordic (DOS)                                                                            |
| 866        | cp866                   | Ruso de OEM; Cirílico (DOS)                                                                         |
| 869        | ibm869                  | Griego moderno OEM; Griego, moderno (DOS)                                                               |
| 870        | IBM870                  | IBM EBCDIC Multilingual/ROECE (Latín 2); IBM EBCDIC multilingüe latín 2                            |
| 874        | Windows-874             | Tailandés (Windows)                                                         |
| 875        | cp875                   | IBM EBCDIC griego moderno                                                                             |
| 932        | Shift \_ JIS              | ANSI/OEM japonés; Japonés (Shift-JIS)                                                             |
| 936        | GB2312                  | Chino simplificado de ANSI/OEM (PRC, Singapur); Chino simplificado (GB2312)                           |
| 949        | KS \_ c \_ 5601-1987        | ANSI/OEM Coreano (código hangul unificado)                                                               |
| 950        | big5                    | Chino tradicional de ANSI/OEM (Taiwán; RAE de Hong Kong, PRC); Chino tradicional (Big5)               |
| 1026       | IBM1026                 | IBM EBCDIC Turco (Latín 5)                                                                        |
| 1047       | IBM01047                | IBM EBCDIC Latín 1/sistema abierto                                                                      |
| 1140       | IBM01140                | US-Canada IBM EBCDIC (símbolo 037 + euro); IBM EBCDIC (EE. UU.-Canadá-euro)                               |
| 1141       | IBM01141                | IBM EBCDIC Germany (símbolo 20273 + euro); IBM EBCDIC (Alemania-Euro)                                 |
| 1142       | IBM01142                | Denmark-Norway IBM EBCDIC (símbolo 20277 + euro); IBM EBCDIC (Dinamarca-Noruega-euro)                   |
| 1143       | IBM01143                | Finland-Sweden IBM EBCDIC (símbolo 20278 + euro); IBM EBCDIC (Finlandia-Suecia-euro)                   |
| 1144       | IBM01144                | IBM EBCDIC Italia (símbolo 20280 + euro); IBM EBCDIC (Italia-euro)                                     |
| 1145       | IBM01145                | IBM EBCDIC latín America-Spain (símbolo 20284 + euro); IBM EBCDIC (España-Euro)                       |
| 1146       | IBM01146                | IBM EBCDIC Reino Unido (símbolo 20285 + euro); IBM EBCDIC (RU-euro)                               |
| 1147       | IBM01147                | IBM EBCDIC Francia (símbolo 20297 + euro); IBM EBCDIC (Francia-Euro)                                   |
| 1148       | IBM01148                | IBM EBCDIC International (símbolo 500 + euro); IBM EBCDIC (internacional-euro)                       |
| 1149       | IBM01149                | IBM EBCDIC islandés (símbolo 20871 + euro); IBM EBCDIC (islandés-euro)                             |
| 1200       | UTF-16                  | Unicode UTF-16, little endian orden de bytes (BMP de ISO 10646); disponible solo para aplicaciones administradas |
| 1201       | unicodeFFFE             | Unicode UTF-16, big endian el orden de los bytes; disponible solo para aplicaciones administradas                       |
| 1250       | Windows-1250            | Europeo central de ANSI; Centroeuropeo (Windows)                                                   |
| 1251       | Windows-1251            | ANSI cirílico; Cirílico (Windows)                                                                   |
| 1252       | Windows-1252            | ANSI Latín 1; Europeo occidental (Windows)                                                            |
| 1253       | Windows-1253            | ANSI griego; Griego (Windows)                                                                         |
| 1254       | Windows-1254            | ANSI Turco; Turco (Windows)                                                                     |
| 1255       | Windows-1255            | Hebreo ANSI; Hebreo (Windows)                                                                       |
| 1256       | Windows-1256            | ANSI Árabe; Árabe (Windows)                                                                       |
| 1257       | Windows-1257            | ANSI Báltico; Báltico (Windows)                                                                       |
| 1258       | Windows-1258            | ANSI/OEM vietnamita; Vietnamita (Windows)                                                           |
| 1361       | Johab                   | Coreano (Johab)                                                                                      |
| 10000      | equipo               | MAC Roman; Europa occidental (Mac)                                                                   |
| 10001      | x-Mac-japonés          | Japonés (Mac)                                                                                      |
| 10002      | x-Mac-ChineseTrad       | Chino tradicional (Big5); Chino tradicional (Mac)                                           |
| 10003      | x-Mac-Coreano            | Coreano (Mac)                                                                                        |
| 10004      | x-Mac-Árabe            | Árabe (Mac)                                                                                        |
| 10005      | x-Mac-hebreo            | Hebreo (Mac)                                                                                        |
| 10006      | x-Mac-griego             | Griego (Mac)                                                                                         |
| 10007      | x-Mac-cirílico          | Cirílico (Mac)                                                                                      |
| 10008      | x-Mac-ChineseSimp       | Chino simplificado de MAC (GB 2312); Chino simplificado (Mac)                                          |
| 10010      | x-Mac-rumano          | Rumano (Mac)                                                                                      |
| 10017      | x-Mac-ucraniano         | Ucraniano (Mac)                                                                                     |
| 10021      | x-Mac-tailandés              | Tailandés (Mac)                                                                                          |
| 10029      | x-Mac-CE                | MAC latín 2; Centroeuropeo (Mac)                                                                 |
| 10079      | x-Mac-islandés         | Islandés (Mac)                                                                                     |
| 10081      | x-Mac-Turco           | Turco (Mac)                                                                                       |
| 10082      | x-Mac-croata          | Croata (Mac)                                                                                      |
| 12000      | UTF-32                  | Unicode UTF-32, little endian el orden de los bytes; disponible solo para aplicaciones administradas                    |
| 12001      | UTF-32BE                | Unicode UTF-32, big endian el orden de los bytes; disponible solo para aplicaciones administradas                       |
| 20000      | CNS de x-chino \_          | CNS Taiwán; Chino tradicional (CNS)                                                               |
| 20001      | x-cp20001               | TCA Taiwán                                                                                          |
| 20002      | x \_ chino-Eten         | Eten Taiwán; Chino tradicional (Eten)                                                             |
| 20003      | x-cp20003               | IBM5550 Taiwán                                                                                      |
| 20004      | x-cp20004               | Teletexto Taiwán                                                                                     |
| 20005      | x-cp20005               | Wang Taiwán                                                                                         |
| 20105      | x-IA5                   | IA5 (IRV alfabeto internacional no. 5, 7 bits); Europeo occidental (IA5)                               |
| 20106      | x-IA5-alemán            | IA5 alemán (7 bits)                                                                                  |
| 20107      | x-IA5-sueco           | IA5 sueco (7 bits)                                                                                 |
| 20108      | x-IA5-noruego         | IA5 noruego (7 bits)                                                                               |
| 20127      | US-ASCII                | US-ASCII (7 bits)                                                                                    |
| 20261      | x-cp20261               | T. 61                                                                                                |
| 20269      | x-cp20269               | ISO 6937 Acento sin espacio                                                                         |
| 20273      | IBM273                  | IBM EBCDIC Germany                                                                                  |
| 20277      | IBM277                  | Denmark-Norway IBM EBCDIC                                                                           |
| 20278      | IBM278                  | Finland-Sweden IBM EBCDIC                                                                           |
| 20280      | IBM280                  | IBM EBCDIC Italia                                                                                    |
| 20284      | IBM284                  | America-Spain IBM EBCDIC latín                                                                      |
| 20285      | IBM285                  | Reino Unido IBM EBCDIC                                                                           |
| 20290      | IBM290                  | Katakana japonés de IBM EBCDIC extendido                                                               |
| 20297      | IBM297                  | IBM EBCDIC Francia                                                                                   |
| 20420      | IBM420                  | IBM EBCDIC Árabe                                                                                   |
| 20423      | IBM423                  | IBM EBCDIC griego                                                                                    |
| 20424      | IBM424                  | Hebreo de IBM EBCDIC                                                                                   |
| 20833      | x-EBCDIC-KoreanExtended | IBM EBCDIC Coreano extendido                                                                          |
| 20838      | IBM-tailandés                | IBM EBCDIC tailandés                                                                                     |
| 20866      | KOI8-r                  | Ruso (KOI8-R); Cirílico (KOI8-R)                                                                 |
| 20871      | IBM871                  | IBM EBCDIC islandés                                                                                |
| 20880      | IBM880                  | IBM EBCDIC cirílico Ruso                                                                         |
| 20905      | IBM905                  | IBM EBCDIC Turco                                                                                  |
| 20924      | IBM00924                | IBM EBCDIC Latín 1/sistema abierto (símbolo 1047 + euro)                                                 |
| 20932      | EUC-JP                  | Japonés (JIS 0208-1990 y 0212-1990)                                                              |
| 20936      | x-cp20936               | Chino simplificado (GB2312); Chino simplificado (GB2312-80)                                         |
| 20949      | x-cp20949               | Coreano Wansung                                                                                      |
| 21025      | cp1025                  | Serbian-Bulgarian cirílico de IBM EBCDIC                                                               |
| 21027      |                         | en desuso                                                                                        |
| 21866      | KOI8-u                  | Ucraniano (KOI8-U); Cirílico (KOI8-U)                                                               |
| 28591      | ISO-8859-1              | ISO 8859-1 Latín 1; Europeo occidental (ISO)                                                          |
| 28592      | ISO-8859-2              | ISO 8859-2 central europea; Centroeuropeo (ISO)                                                 |
| 28593      | ISO-8859-3              | ISO 8859-3 latín 3                                                                                  |
| 28594      | ISO-8859-4              | ISO 8859-4 Báltico                                                                                   |
| 28595      | ISO-8859-5              | ISO 8859-5 Cirílico                                                                                 |
| 28596      | ISO-8859-6              | ISO 8859-6 Árabe                                                                                   |
| 28597      | ISO-8859-7              | ISO 8859-7 Griego                                                                                    |
| 28598      | ISO-8859-8              | ISO 8859-8 hebreo; Hebreo (ISO-visual)                                                              |
| 28599      | ISO-8859-9              | ISO 8859-9 Turco                                                                                  |
| 28603      | ISO-8859-13             | ISO 8859-13 estonio                                                                                |
| 28605      | ISO-8859-15             | ISO 8859-15 latín 9                                                                                 |
| 29001      | x-Europa                | Europa 3                                                                                            |
| 38598      | ISO-8859-8-i            | ISO 8859-8 hebreo; Hebreo (ISO-Logical)                                                             |
| 50220      | ISO-2022-JP             | ISO 2022 japonés sin katakana de ancho medio; Japonés (JIS)                                        |
| 50221      | csISO2022JP             | ISO 2022 japonés con katakana de ancho medio; Japonés (JIS-permitir Kana de 1 bytes)                         |
| 50222      | ISO-2022-JP             | ISO 2022 japonés JIS X 0201-1989; Japonés (JIS-permitir Kana de 1 bytes-SO/SI)                         |
| 50225      | ISO-2022-KR             | ISO 2022 Coreano                                                                                     |
| 50227      | x-cp50227               | ISO 2022 chino simplificado; Chino simplificado (ISO 2022)                                          |
| 50229      |                         | ISO 2022 chino tradicional                                                                        |
| 50930      |                         | EBCDIC japonés (Katakana) extendido                                                                 |
| 50931      |                         | US-Canada EBCDIC y japonés                                                                       |
| 50933      |                         | EBCDIC Coreano extendido y Coreano                                                                   |
| 50935      |                         | Chino simplificado de EBCDIC simplificado y chino simplificado                                           |
| 50936      |                         | Chino simplificado de EBCDIC                                                                           |
| 50937      |                         | US-Canada EBCDIC y chino tradicional                                                            |
| 50939      |                         | EBCDIC japonés (Latín) extendido y japonés                                                       |
| 51932      | EUC-JP                  | EUC japonés                                                                                        |
| 51936      | EUC-CN                  | Chino simplificado de EUC; Chino simplificado (EUC)                                                    |
| 51949      | EUC-KR                  | EUC Coreano                                                                                          |
| 51950      |                         | EUC chino tradicional                                                                             |
| 52936      | Hz-GB-2312              | HZ-GB2312 chino simplificado; Chino simplificado (HZ)                                               |
| 54936      | GB18030                 | **Windows XP y versiones posteriores:** GB18030 chino simplificado (4 bytes); Chino simplificado (GB18030)         |
| 57002      | x-ISCII-de              | ISCII Devanagari                                                                                    |
| 57003      | x-ISCII-ser              | ISCII Bangla                                                                                        |
| 57004      | x-ISCII-TA              | Tamil de ISCII                                                                                         |
| 57005      | x-ISCII-te              | ISCII Telugu                                                                                        |
| 57006      | x-ISCII-as              | Equivalente de ISCII                                                                                      |
| 57007      | x-ISCII-o              | Odia de ISCII                                                                                          |
| 57008      | x-ISCII-Ka              | Kannada de ISCII                                                                                       |
| 57009      | x-ISCII-MA              | ISCII Malayalam                                                                                     |
| 57010      | x-ISCII-gu              | Gujarati (ISCII)                                                                                      |
| 57011      | x-ISCII-PA              | ISCII punyabí                                                                                       |
| 65000      | UTF-7                   | Unicode (UTF-7)                                                                                     |
| 65001      | utf-8                   | Unicode (UTF-8)                                                                                     |



 

 

 



