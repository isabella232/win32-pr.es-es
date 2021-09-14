---
description: En la tabla siguiente se definen los identificadores de página de códigos disponibles.
ms.assetid: 5d6fc86a-f205-4d14-bb7c-ecd71682e0fe
title: Identificadores de página de códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb0482247313e8d61d61d7d3178906536ab9e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274788"
---
# <a name="code-page-identifiers"></a>Identificadores de página de códigos

En la tabla siguiente se definen los identificadores de página de códigos disponibles.

> [!Note]  
> Las páginas de códigos ANSI pueden ser diferentes en equipos diferentes o se pueden cambiar para un solo equipo, lo que provoca daños en los datos. Para obtener los resultados más coherentes, las aplicaciones deben usar Unicode, como UTF-8 o UTF-16, en lugar de una página de códigos específica.

 



| Identificador | Nombre de .NET               | Información adicional                                                                              |
|------------|-------------------------|-----------------------------------------------------------------------------------------------------|
| 037        | IBM037                  | IBM EBCDIC US-Canada                                                                                |
| 437        | IBM437                  | Estados Unidos OEM                                                                                   |
| 500        | IBM500                  | IBM EBCDIC International                                                                            |
| 708        | ASMO-708                | Árabe (ASMO 708)                                                                                   |
| 709        |                         | Árabe (ASMO-449+, BCON V4)                                                                         |
| 710        |                         | Árabe: árabe transparente                                                                         |
| 720        | DOS: 720                 | Árabe (ASMO transparente); Árabe (DOS)                                                             |
| 737        | ibm737                  | OEM griego (anteriormente 437G); Griego (DOS)                                                              |
| 775        | ibm775                  | Oem Oem; Trastos (DOS)                                                                            |
| 850        | ibm850                  | OEM Multilingüe Latino 1; Europa Occidental (DOS)                                                    |
| 852        | ibm852                  | OEM Latin 2; Centroeuropeo (DOS)                                                                 |
| 855        | IBM855                  | Cirílico de OEM (principalmente ruso)                                                                    |
| 857        | ibm857                  | OEM turco; Turco (DOS)                                                                          |
| 858        | IBM00858                | Símbolo multilingüe de OEM latino 1 + euro                                                              |
| 860        | IBM860                  | OEM portugués; Portugués (DOS)                                                                    |
| 861        | ibm861                  | OEM islandés; Islandés (DOS)                                                                      |
| 862        | DOS: 862                 | HEBREO DE OEM; Hebreo (DOS)                                                                            |
| 863        | IBM863                  | OEM francés canadiense; Francés canadiense (DOS)                                                          |
| 864        | IBM864                  | Árabe de OEM; Árabe (864)                                                                            |
| 865        | IBM865                  | Oem Oem Oem; Nórdicos (DOS)                                                                            |
| 866        | cp866                   | OEM ruso; Cirílico (DOS)                                                                         |
| 869        | ibm869                  | Griego moderno de OEM; Griego, moderno (DOS)                                                               |
| 870        | IBM870                  | IBM EBCDIC multilingüe/ROECE (latino 2); IBM EBCDIC Multilingüe Latino 2                            |
| 874        | Windows-874             | Tailandés (Windows)                                                         |
| 875        | cp875                   | IBM EBCDIC griego moderno                                                                             |
| 932        | shift \_ jis              | ANSI/OEM japonés; Japonés (Shift-JIS)                                                             |
| 936        | GB2312                  | CHINO simplificado ANSI/OEM (PRC, Singapur); Chino simplificado (GB2312)                           |
| 949        | ks \_ c \_ 5601-1987        | ANSI/OEM coreano (código Hangul unificado)                                                               |
| 950        | big5                    | Chino tradicional ANSI/OEM (Taiwán; RAE de Hong Kong, PRC); Chino tradicional (Big5)               |
| 1026       | IBM1026                 | IBM EBCDIC turco (latino 5)                                                                        |
| 1047       | IBM01047                | IBM EBCDIC Latin 1/Open System                                                                      |
| 1140       | IBM01140                | IBM EBCDIC US-Canada (símbolo 037 + Euro); IBM EBCDIC (EE. UU.-Canadá-Euro)                               |
| 1141       | IBM01141                | IBM EBCDIC Alemania (símbolo 20273 + Euro); IBM EBCDIC (Alemania-Euro)                                 |
| 1142       | IBM01142                | IBM EBCDIC Denmark-Norway (símbolo 20277 + Euro); IBM EBCDIC (Dinamarca-Noruega-Euro)                   |
| 1143       | IBM01143                | IBM EBCDIC Finland-Sweden (símbolo 20278 + Euro); IBM EBCDIC (Noruega-Noruega-Euro)                   |
| 1144       | IBM01144                | IBM EBCDIC Italia (símbolo 20280 + Euro); IBM EBCDIC (Italia-Euro)                                     |
| 1145       | IBM01145                | IBM EBCDIC Latin America-Spain (símbolo 20284 + Euro); IBM EBCDIC (España-Euro)                       |
| 1146       | IBM01146                | IBM EBCDIC Reino Unido (símbolo 20285 + Euro); IBM EBCDIC (Reino Unido-Euro)                               |
| 1147       | IBM01147                | IBM EBCDIC France (símbolo 20297 + Euro); IBM EBCDIC (Francia-Euro)                                   |
| 1148       | IBM01148                | IBM EBCDIC International (símbolo de 500 + Euro); IBM EBCDIC (Internacional-Euro)                       |
| 1149       | IBM01149                | IBM EBCDIC Islandés (símbolo 20871 + Euro); IBM EBCDIC (euro islandés)                             |
| 1200       | UTF-16                  | Unicode UTF-16, little endian orden de bytes (BMP de ISO 10646); disponible solo para aplicaciones administradas |
| 1201       | unicodeFFFE             | Unicode UTF-16, big endian orden de bytes; disponible solo para aplicaciones administradas                       |
| 1250       | Windows-1250            | ANSI Centroeuropeo; Europa central (Windows)                                                   |
| 1251       | Windows-1251            | ANSI cirílico; Cirílico (Windows)                                                                   |
| 1252       | windows-1252            | ANSI Latin 1; Europa Occidental (Windows)                                                            |
| 1253       | Windows-1253            | ANSI griego; Griego (Windows)                                                                         |
| 1254       | Windows-1254            | ANSI turco; Turco (Windows)                                                                     |
| 1255       | Windows-1255            | ANSI Hebreo; Hebreo (Windows)                                                                       |
| 1256       | Windows-1256            | ANSI Árabe; Árabe (Windows)                                                                       |
| 1257       | Windows-1257            | Ansi Desmáns; Semántica (Windows)                                                                       |
| 1258       | Windows-1258            | ANSI/OEM Oem Oem: Resono (Windows)                                                           |
| 1361       | Johab                   | Coreano (Johab)                                                                                      |
| 10000      | equipo               | MAC Román; Europa Occidental (Mac)                                                                   |
| 10001      | x-Mac-japonés          | Japonés (Mac)                                                                                      |
| 10002      | x-Mac-ChineseTrad       | Chino tradicional mac (Big5); Chino tradicional (Mac)                                           |
| 10003      | x-Mac-Coreano            | Coreano (Mac)                                                                                        |
| 10004      | x-Mac-Árabe            | Árabe (Mac)                                                                                        |
| 10005      | x-Mac-hebreo            | Hebreo (Mac)                                                                                        |
| 10006      | x-Mac-griego             | Griego (Mac)                                                                                         |
| 10007      | x-Mac-cirílico          | Cirílico (Mac)                                                                                      |
| 10008      | x-Mac-ChineseSimp       | Chino simplificado mac (GB 2312); Chino simplificado (Mac)                                          |
| 10010      | x-Mac-rumano          | Rumano (Mac)                                                                                      |
| 10017      | x-Mac-ucraniano         | Ucraniano (Mac)                                                                                     |
| 10021      | x-Mac-tailandés              | Tailandés (Mac)                                                                                          |
| 10029      | x-Mac-CE                | MAC Latin 2; Centroeuropeo (Mac)                                                                 |
| 10079      | x-Mac-islandés         | Islandés (Mac)                                                                                     |
| 10081      | x-Mac-Turco           | Turco (Mac)                                                                                       |
| 10082      | x-Mac-croata          | Croata (Mac)                                                                                      |
| 12000      | UTF-32                  | Unicode UTF-32, little endian orden de bytes; disponible solo para aplicaciones administradas                    |
| 12001      | UTF-32BE                | Unicode UTF-32, big endian orden de bytes; disponible solo para aplicaciones administradas                       |
| 20000      | CNS chino x \_          | CNS Taiwan; Chino tradicional (CNS)                                                               |
| 20001      | x-cp20001               | TCA Taiwán                                                                                          |
| 20002      | x \_ Chino-Eten         | Eten Taiwan; Chino tradicional (Eten)                                                             |
| 20003      | x-cp20003               | IBM5550 Taiwán                                                                                      |
| 20004      | x-cp20004               | Teletexto Taiwán                                                                                     |
| 20005      | x-cp20005               | Wang Taiwán                                                                                         |
| 20105      | x-IA5                   | IA5 (IRV International Alphabet No. 5, 7 bits); Europa Occidental (IA5)                               |
| 20106      | x-IA5-alemán            | IA5 Alemán (7 bits)                                                                                  |
| 20107      | x-IA5-sueco           | IA5 sueco (7 bits)                                                                                 |
| 20108      | x-IA5-noruego         | IA5 noruego (7 bits)                                                                               |
| 20127      | US-ASCII                | US-ASCII (7 bits)                                                                                    |
| 20261      | x-cp20261               | T. 61                                                                                                |
| 20269      | x-cp20269               | ISO 6937 Acento sin espacio                                                                         |
| 20273      | IBM273                  | IBM EBCDIC Alemania                                                                                  |
| 20277      | IBM277                  | IBM EBCDIC Denmark-Norway                                                                           |
| 20278      | IBM278                  | IBM EBCDIC Finland-Sweden                                                                           |
| 20280      | IBM280                  | IBM EBCDIC Italia                                                                                    |
| 20284      | IBM284                  | IBM EBCDIC Latin America-Spain                                                                      |
| 20285      | IBM285                  | IBM EBCDIC Reino Unido                                                                           |
| 20290      | IBM290                  | IBM EBCDIC Japanese Katakana Extended                                                               |
| 20297      | IBM297                  | IBM EBCDIC France                                                                                   |
| 20420      | IBM420                  | Ibm EBCDIC Árabe                                                                                   |
| 20423      | IBM423                  | IBM EBCDIC griego                                                                                    |
| 20424      | IBM424                  | IBM EBCDIC Hebreo                                                                                   |
| 20833      | x-EBCDIC-KoreanExtended | IBM EBCDIC Coreano extendido                                                                          |
| 20838      | IBM-tailandés                | IBM EBCDIC tailandés                                                                                     |
| 20866      | KOI8-r                  | Ruso (KOI8-R); Cirílico (KOI8-R)                                                                 |
| 20871      | IBM871                  | IBM EBCDIC Islandés                                                                                |
| 20880      | IBM880                  | IBM EBCDIC Cirílico ruso                                                                         |
| 20905      | IBM905                  | IBM EBCDIC turco                                                                                  |
| 20924      | IBM00924                | IBM EBCDIC Latin 1/Open System (símbolo 1047 + Euro)                                                 |
| 20932      | EUC-JP                  | Japonés (JIS 0208-1990 y 0212-1990)                                                              |
| 20936      | x-cp20936               | Chino simplificado (GB2312); Chino simplificado (GB2312-80)                                         |
| 20949      | x-cp20949               | Coreano Wansung                                                                                      |
| 21025      | cp1025                  | IBM EBCDIC Cyrillic Serbian-Bulgarian                                                               |
| 21027      |                         | (en desuso)                                                                                        |
| 21866      | KOI8-u                  | (KOI8-U); Cirílico (KOI8-U)                                                               |
| 28591      | ISO-8859-1              | ISO 8859-1 Latin 1; Europa Occidental (ISO)                                                          |
| 28592      | ISO-8859-2              | ISO 8859-2 Centroeuropeo; Europa central (ISO)                                                 |
| 28593      | ISO-8859-3              | ISO 8859-3 Latin 3                                                                                  |
| 28594      | ISO-8859-4              | Iso 8859-4(4)                                                                                   |
| 28595      | ISO-8859-5              | ISO 8859-5 Cirílico                                                                                 |
| 28596      | ISO-8859-6              | ISO 8859-6 Árabe                                                                                   |
| 28597      | ISO-8859-7              | ISO 8859-7 Griego                                                                                    |
| 28598      | ISO-8859-8              | ISO 8859-8 Hebreo; Hebreo (ISO-Visual)                                                              |
| 28599      | ISO-8859-9              | ISO 8859-9 Turco                                                                                  |
| 28603      | ISO-8859-13             | ISO 8859-13 Estonio                                                                                |
| 28605      | ISO-8859-15             | ISO 8859-15 Latin 9                                                                                 |
| 29001      | x-Europa                | Europa 3                                                                                            |
| 38598      | ISO-8859-8-i            | ISO 8859-8 Hebreo; Hebreo (iso lógico)                                                             |
| 50220      | ISO-2022-JP             | ISO 2022 Japonés sin katakana de medias giras; Japonés (JIS)                                        |
| 50221      | csISO2022JP             | ISO 2022 Japonés con katakana de medio adoba; Japonés (JIS-Permitir kana de 1 byte)                         |
| 50222      | ISO-2022-JP             | ISO 2022 Japanese JIS X 0201-1989; Japonés (JIS-Allow 1 byte Kana - SO/SI)                         |
| 50225      | ISO-2022-KR             | ISO 2022 Coreano                                                                                     |
| 50227      | x-cp50227               | ISO 2022 Chino simplificado; Chino simplificado (ISO 2022)                                          |
| 50229      |                         | Chino tradicional iso 2022                                                                        |
| 50930      |                         | EBCDIC Japonés (Katakana) Extendido                                                                 |
| 50931      |                         | EBCDIC US-Canada japonés                                                                       |
| 50933      |                         | EBCDIC Coreano extendido y coreano                                                                   |
| 50935      |                         | Chino simplificado de EBCDIC extendido y chino simplificado                                           |
| 50936      |                         | Chino simplificado EBCDIC                                                                           |
| 50937      |                         | EBCDIC US-Canada y chino tradicional                                                            |
| 50939      |                         | Japonés EBCDIC (latino) extendido y japonés                                                       |
| 51932      | EUC-JP                  | EUC japonés                                                                                        |
| 51936      | EUC-CN                  | EUC Chino simplificado; Chino simplificado (EUC)                                                    |
| 51949      | EUC-KR                  | EUC coreano                                                                                          |
| 51950      |                         | Chino tradicional de EUC                                                                             |
| 52936      | Hz-GB-2312              | HZ-GB2312 Chino simplificado; Chino simplificado (HZ)                                               |
| 54936      | GB18030                 | **Windows XP y versiones posteriores:** GB18030 Chino simplificado (4 bytes); Chino simplificado (GB18030)         |
| 57002      | x-ISCII-de              | ISCII Devanagari                                                                                    |
| 57003      | x-ISCII-ser              | ISCII Jadela                                                                                        |
| 57004      | x-ISCII-TA              | Tamil de ISCII                                                                                         |
| 57005      | x-ISCII-te              | ISCII Telugu                                                                                        |
| 57006      | x-ISCII-as              | Equivalente de ISCII                                                                                      |
| 57007      | x-ISCII-o              | ISCII Quería                                                                                          |
| 57008      | x-ISCII-Ka              | Kannada de ISCII                                                                                       |
| 57009      | x-ISCII-MA              | ISCII Malayalam                                                                                     |
| 57010      | x-ISCII-gu              | Gujarati (ISCII)                                                                                      |
| 57011      | x-ISCII-PA              | ISCII punyabí                                                                                       |
| 65000      | UTF-7                   | Unicode (UTF-7)                                                                                     |
| 65001      | utf-8                   | Unicode (UTF-8)                                                                                     |



 

 

 



