---
description: Los campos de códigos de subconjuntos Unicode (USBs) se usan en las estructuras FONTSIGNATURE y LOCALESIGNATURE.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Campos de códigos de subconjunto Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fced251b1bf8e04dd4c0d7d7cb0dca15c8bdfa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652865"
---
# <a name="unicode-subset-bitfields"></a>Campos de códigos de subconjunto Unicode

Los campos de códigos de subconjuntos Unicode (USBs) se usan en las estructuras [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) y [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .



<table>
<thead>
<tr class="header">
<th>bit</th>
<th>Subintervalo Unicode</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>0000 - 007F</td>
<td>Latín básico</td>
</tr>
<tr class="even">
<td>1</td>
<td>0080 - 00FF</td>
<td>Suplemento Latín-1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>0100 - 017F</td>
<td>Latín extendido-A</td>
</tr>
<tr class="even">
<td>3</td>
<td>0180 - 024F</td>
<td>Latín extendido-B</td>
</tr>
<tr class="odd">
<td rowspan="3">4 $ {REMOVE} $<br />
</td>
<td>0250 - 02AF</td>
<td>Extensiones IPA</td>
</tr>
<tr class="even">
<td>1D00 - 1D7F</td>
<td>Extensiones fonéticas</td>

</tr>
<tr class="odd">
<td>1D80 - 1DBF</td>
<td>Suplemento de extensiones fonéticas</td>

</tr>
<tr class="even">
<td rowspan="2">5 $ {REMOVE} $<br />
</td>
<td>02B0 - 02FF</td>
<td>Letras modificadoras de espaciado</td>
</tr>
<tr class="odd">
<td>A700 - A71F</td>
<td>Letras de tono modificador</td>

</tr>
<tr class="even">
<td rowspan="2">6 $ {REMOVE} $<br />
</td>
<td>0300 - 036F</td>
<td>Combinación de marcas diacríticas</td>
</tr>
<tr class="odd">
<td>1DC0 - 1DFF</td>
<td>Suplemento de combinación de marcas diacríticas</td>

</tr>
<tr class="even">
<td>7</td>
<td>0370 - 03FF</td>
<td>Griego y cóptico</td>
</tr>
<tr class="odd">
<td>8</td>
<td>2C80 - 2CFF</td>
<td>Copto</td>
</tr>
<tr class="even">
<td rowspan="4">9 $ {REMOVE} $<br />
</td>
<td>0400 - 04FF</td>
<td>Cirílico</td>
</tr>
<tr class="odd">
<td>0500 - 052F</td>
<td>Suplemento cirílico</td>

</tr>
<tr class="even">
<td>2DE0 - 2DFF</td>
<td>Cirílico extendido-A</td>

</tr>
<tr class="odd">
<td>A640 - A69F</td>
<td>Cirílico extendido-B</td>

</tr>
<tr class="even">
<td>10</td>
<td>0530 - 058F</td>
<td>Armenio</td>
</tr>
<tr class="odd">
<td>11</td>
<td>0590 - 05FF</td>
<td>Hebreo</td>
</tr>
<tr class="even">
<td>12</td>
<td>A500 - A63F</td>
<td>Vai</td>
</tr>
<tr class="odd">
<td rowspan="2">13 $ {REMOVE} $<br />
</td>
<td>0600 - 06FF</td>
<td>Árabe</td>
</tr>
<tr class="even">
<td>0750-077F</td>
<td>Suplemento Árabe</td>

</tr>
<tr class="odd">
<td>14</td>
<td>07C0 - 07FF</td>
<td>Símbolo</td>
</tr>
<tr class="even">
<td>15</td>
<td>0900 - 097F</td>
<td>Devanagari</td>
</tr>
<tr class="odd">
<td>16</td>
<td>0980 - 09FF</td>
<td>Bengalí</td>
</tr>
<tr class="even">
<td>17</td>
<td>0A00 - 0A7F</td>
<td>Gurmukhi</td>
</tr>
<tr class="odd">
<td>18</td>
<td>0A80 - 0AFF</td>
<td>Gujarati</td>
</tr>
<tr class="even">
<td>19</td>
<td>0B00 - 0B7F</td>
<td>Odia</td>
</tr>
<tr class="odd">
<td>20</td>
<td>0B80 - 0BFF</td>
<td>Tamil</td>
</tr>
<tr class="even">
<td>21</td>
<td>0C00 - 0C7F</td>
<td>Telugu</td>
</tr>
<tr class="odd">
<td>22</td>
<td>0C80 - 0CFF</td>
<td>Canarés</td>
</tr>
<tr class="even">
<td>23</td>
<td>0D00 - 0D7F</td>
<td>Malayalam</td>
</tr>
<tr class="odd">
<td>24</td>
<td>0E00 - 0E7F</td>
<td>Tailandés</td>
</tr>
<tr class="even">
<td>25</td>
<td>0E80 - 0EFF</td>
<td>Lao</td>
</tr>
<tr class="odd">
<td rowspan="2">26 $ {REMOVE} $<br />
</td>
<td>10A0 - 10FF</td>
<td>Georgiano</td>
</tr>
<tr class="even">
<td>2D00 - 2D2F</td>
<td>Suplemento georgiano</td>

</tr>
<tr class="odd">
<td>27</td>
<td>1B00 - 1B7F</td>
<td>Balinés</td>
</tr>
<tr class="even">
<td>28</td>
<td>1100 - 11FF</td>
<td>Jamo hangul</td>
</tr>
<tr class="odd">
<td rowspan="3">29 $ {REMOVE} $<br />
</td>
<td>1E00 - 1EFF</td>
<td>Latín extendido adicional</td>
</tr>
<tr class="even">
<td>2C60 - 2C7F</td>
<td>Latín extendido-C</td>

</tr>
<tr class="odd">
<td>A720 - A7FF</td>
<td>Latín extendido-D</td>

</tr>
<tr class="even">
<td>30</td>
<td>1F00 - 1FFF</td>
<td>Griego extendido</td>
</tr>
<tr class="odd">
<td rowspan="2">31 $ {REMOVE} $<br />
</td>
<td>2000 - 206F</td>
<td>Puntuación general</td>
</tr>
<tr class="even">
<td>2E00 - 2E7F</td>
<td>Puntuación complementaria</td>

</tr>
<tr class="odd">
<td>32</td>
<td>2070 - 209F</td>
<td>Superíndices y subíndices</td>
</tr>
<tr class="even">
<td>33</td>
<td>20A0 - 20CF</td>
<td>Símbolos de moneda</td>
</tr>
<tr class="odd">
<td>34</td>
<td>20D0 - 20FF</td>
<td>Combinación de marcas diacríticas para símbolos</td>
</tr>
<tr class="even">
<td>35</td>
<td>2100 - 214F</td>
<td>Símbolos de Letterlike</td>
</tr>
<tr class="odd">
<td>36</td>
<td>2150 - 218F</td>
<td>Formatos numéricos</td>
</tr>
<tr class="even">
<td rowspan="4">37 $ {REMOVE} $<br />
</td>
<td>2190 - 21FF</td>
<td>Flechas</td>
</tr>
<tr class="odd">
<td>27F0 - 27FF</td>
<td>Flechas adicionales-A</td>

</tr>
<tr class="even">
<td>2900 - 297F</td>
<td>Flechas adicionales-B</td>

</tr>
<tr class="odd">
<td>2B00 - 2BFF</td>
<td>Símbolos y flechas varios</td>

</tr>
<tr class="even">
<td rowspan="4">38 $ {REMOVE} $<br />
</td>
<td>2200 - 22FF</td>
<td>Operadores matemáticos</td>
</tr>
<tr class="odd">
<td>27C0 - 27EF</td>
<td>Símbolos matemáticos varios: A</td>

</tr>
<tr class="even">
<td>2980 - 29FF</td>
<td>Símbolos matemáticos varios-B</td>

</tr>
<tr class="odd">
<td>2A00 - 2AFF</td>
<td>Operadores matemáticos adicionales</td>

</tr>
<tr class="even">
<td>39</td>
<td>2300 - 23FF</td>
<td>Aspectos técnicos diversos</td>
</tr>
<tr class="odd">
<td>40</td>
<td>2400 - 243F</td>
<td>Imágenes de control</td>
</tr>
<tr class="even">
<td>41</td>
<td>2440 - 245F</td>
<td>Reconocimiento óptico de caracteres</td>
</tr>
<tr class="odd">
<td>42</td>
<td>2460 - 24FF</td>
<td>Alfanuméricos delimitados</td>
</tr>
<tr class="even">
<td>43</td>
<td>2500 - 257F</td>
<td>Dibujo de caja</td>
</tr>
<tr class="odd">
<td>44</td>
<td>2580 - 259F</td>
<td>Elementos de bloque</td>
</tr>
<tr class="even">
<td>45</td>
<td>25A0 - 25FF</td>
<td>Formas geométricas</td>
</tr>
<tr class="odd">
<td>46</td>
<td>2600 - 26FF</td>
<td>Símbolos varios</td>
</tr>
<tr class="even">
<td>47</td>
<td>2700 - 27BF</td>
<td>Dingbats</td>
</tr>
<tr class="odd">
<td>48</td>
<td>3000 - 303F</td>
<td>Símbolos y puntuación CJK</td>
</tr>
<tr class="even">
<td>49</td>
<td>3040 - 309F</td>
<td>Hiragana</td>
</tr>
<tr class="odd">
<td rowspan="2">50 $ {REMOVE} $<br />
</td>
<td>30A0 - 30FF</td>
<td>Katakana</td>
</tr>
<tr class="even">
<td>31F0 - 31FF</td>
<td>Extensiones fonéticas katakana</td>

</tr>
<tr class="odd">
<td rowspan="2">51 $ {REMOVE} $<br />
</td>
<td>3100 - 312F</td>
<td>Bopomofo</td>
</tr>
<tr class="even">
<td>31A0 - 31BF</td>
<td>Bopomofo extendido</td>

</tr>
<tr class="odd">
<td>52</td>
<td>3130 - 318F</td>
<td>Compatibilidad con hangul Jamo</td>
</tr>
<tr class="even">
<td>53</td>
<td>A840 - A87F</td>
<td>Phags-pa</td>
</tr>
<tr class="odd">
<td>54</td>
<td>3200 - 32FF</td>
<td>Letras y meses CJK delimitados</td>
</tr>
<tr class="even">
<td>55</td>
<td>3300 - 33FF</td>
<td>Compatibilidad con CJK</td>
</tr>
<tr class="odd">
<td>56</td>
<td>AC00 - D7AF</td>
<td>Sílabas hangul</td>
</tr>
<tr class="even">
<td>57</td>
<td>D800-DFFF</td>
<td>No plano 0. Tenga en cuenta que establecer este bit implica que hay al menos un punto de código suplementario más allá del plano básico multilingüe (BMP) que es compatible con esta fuente. Vea <a href="surrogates-and-supplementary-characters.md">suplentes y caracteres adicionales</a>.</td>
</tr>
<tr class="odd">
<td>58</td>
<td>10900-1091F</td>
<td>Phoenician</td>
</tr>
<tr class="even">
<td rowspan="7">59 $ {REMOVE} $<br />
</td>
<td>2E80 - 2EFF</td>
<td>Suplemento de radicales CJK</td>
</tr>
<tr class="odd">
<td>2F00 - 2FDF</td>
<td>Radicales kangxi</td>

</tr>
<tr class="even">
<td>2FF0 - 2FFF</td>
<td>Caracteres de descripción ideográfica</td>

</tr>
<tr class="odd">
<td>3190 - 319F</td>
<td>Kanbun</td>

</tr>
<tr class="even">
<td>3400 - 4DBF</td>
<td>Extensión A de Ideogramas unificados CJK</td>

</tr>
<tr class="odd">
<td>4E00 - 9FFF</td>
<td>Ideogramas unificados CJK</td>

</tr>
<tr class="even">
<td>20000-2A6DF</td>
<td>Extensión de ideogramas unificadas CJK B</td>

</tr>
<tr class="odd">
<td>60</td>
<td>E000 - F8FF</td>
<td>Área de uso privado</td>
</tr>
<tr class="even">
<td rowspan="3">61 $ {REMOVE} $<br />
</td>
<td>31C0 - 31EF</td>
<td>Trazos CJK</td>
</tr>
<tr class="odd">
<td>F900 - FAFF</td>
<td>Ideogramas de compatibilidad CJK</td>

</tr>
<tr class="even">
<td>2F800 - 2FA1F</td>
<td>Suplemento de los ideogramas de compatibilidad CJK</td>

</tr>
<tr class="odd">
<td>62</td>
<td>FB00 - FB4F</td>
<td>Formularios de presentación alfabética</td>
</tr>
<tr class="even">
<td>63</td>
<td>FB50 - FDFF</td>
<td>Formularios de presentación árabe-A</td>
</tr>
<tr class="odd">
<td>64</td>
<td>FE20 - FE2F</td>
<td>Combinación de medias marcas</td>
</tr>
<tr class="even">
<td rowspan="2">65 $ {REMOVE} $<br />
</td>
<td>FE10 - FE1F</td>
<td>Formularios verticales</td>
</tr>
<tr class="odd">
<td>FE30 - FE4F</td>
<td>Formularios de compatibilidad CJK</td>

</tr>
<tr class="even">
<td>66</td>
<td>FE50 - FE6F</td>
<td>Variantes de formato pequeño</td>
</tr>
<tr class="odd">
<td>67</td>
<td>FE70 - FEFF</td>
<td>Formularios de presentación árabes-B</td>
</tr>
<tr class="even">
<td>68</td>
<td>FF00 - FFEF</td>
<td>Formatos de ancho de ancho y de ancho completo</td>
</tr>
<tr class="odd">
<td>69</td>
<td>FFF0 - FFFF</td>
<td>Especiales</td>
</tr>
<tr class="even">
<td>70</td>
<td>0F00 - 0FFF</td>
<td>Tibetano</td>
</tr>
<tr class="odd">
<td>71</td>
<td>0700 - 074F</td>
<td>Siríaco</td>
</tr>
<tr class="even">
<td>72</td>
<td>0780 - 07BF</td>
<td>Thaana</td>
</tr>
<tr class="odd">
<td>73</td>
<td>0D80 - 0DFF</td>
<td>Cingalés</td>
</tr>
<tr class="even">
<td>74</td>
<td>1000 - 109F</td>
<td>Myanmar</td>
</tr>
<tr class="odd">
<td rowspan="3">75 $ {REMOVE} $<br />
</td>
<td>1200 - 137F</td>
<td>Dígito</td>
</tr>
<tr class="even">
<td>1380-139F</td>
<td>Suplemento etíope</td>

</tr>
<tr class="odd">
<td>2D80 - 2DDF</td>
<td>Etíope extendido</td>

</tr>
<tr class="even">
<td>76</td>
<td>13A0 - 13FF</td>
<td>Cheroqui</td>
</tr>
<tr class="odd">
<td>77</td>
<td>1400 - 167F</td>
<td>Silábico indígena canadiense unificada</td>
</tr>
<tr class="even">
<td>78</td>
<td>1680 - 169F</td>
<td>Ogham</td>
</tr>
<tr class="odd">
<td>79</td>
<td>16A0 - 16FF</td>
<td>Rúnica</td>
</tr>
<tr class="even">
<td rowspan="2">80 $ {REMOVE} $<br />
</td>
<td>1780 - 17FF</td>
<td>Jemer</td>
</tr>
<tr class="odd">
<td>19E0 - 19FF</td>
<td>Símbolos Khmer</td>

</tr>
<tr class="even">
<td>81</td>
<td>1800 - 18AF</td>
<td>Mongol</td>
</tr>
<tr class="odd">
<td>82</td>
<td>2800 - 28FF</td>
<td>Patrones de Braille</td>
</tr>
<tr class="even">
<td rowspan="2">83 $ {REMOVE} $<br />
</td>
<td>A000 - A48F</td>
<td>Sílabas Yi</td>
</tr>
<tr class="odd">
<td>A490 - A4CF</td>
<td>Radicales Yi</td>

</tr>
<tr class="even">
<td rowspan="4">84 $ {REMOVE} $<br />
</td>
<td>1700 - 171F</td>
<td>Tagalo</td>
</tr>
<tr class="odd">
<td>1720 - 173F</td>
<td>Hanunno</td>

</tr>
<tr class="even">
<td>1740 - 175F</td>
<td>Buhid</td>

</tr>
<tr class="odd">
<td>1760 - 177F</td>
<td>Tagbanwa</td>

</tr>
<tr class="even">
<td>85</td>
<td>10300-1032F</td>
<td>Cursiva antigua</td>
</tr>
<tr class="odd">
<td>86</td>
<td>10330-1034F</td>
<td>Gótico</td>
</tr>
<tr class="even">
<td>87</td>
<td>10400-1044F</td>
<td>Deseret</td>
</tr>
<tr class="odd">
<td rowspan="3">88 $ {REMOVE} $<br />
</td>
<td>1D000 - 1D0FF</td>
<td>Símbolos musicales de Byzantine</td>
</tr>
<tr class="even">
<td>1D100 - 1D1FF</td>
<td>Símbolos musicales</td>

</tr>
<tr class="odd">
<td>1D200 - 1D24F</td>
<td>Notación musical griega antigua</td>

</tr>
<tr class="even">
<td>89</td>
<td>1D400 - 1D7FF</td>
<td>Símbolos alfanuméricos matemáticos</td>
</tr>
<tr class="odd">
<td rowspan="2">90 $ {REMOVE} $<br />
</td>
<td>FF000 - FFFFD</td>
<td>Uso privado (plano 15)</td>
</tr>
<tr class="even">
<td>100000-10FFFD</td>
<td>Uso privado (plano 16)</td>

</tr>
<tr class="odd">
<td rowspan="2">91 $ {REMOVE} $<br />
</td>
<td>FE00 - FE0F</td>
<td>Selectores de variación</td>
</tr>
<tr class="even">
<td>E0100 - E01EF</td>
<td>Suplemento de selectores de variación</td>

</tr>
<tr class="odd">
<td>92</td>
<td>E0000 - E007F</td>
<td>Etiquetas</td>
</tr>
<tr class="even">
<td>93</td>
<td>1900 - 194F</td>
<td>Limbu</td>
</tr>
<tr class="odd">
<td>94</td>
<td>1950 - 197F</td>
<td>Tai le</td>
</tr>
<tr class="even">
<td>95</td>
<td>1980-19DF</td>
<td>Nuevo tai lue moderno</td>
</tr>
<tr class="odd">
<td>96</td>
<td>1A00 - 1A1F</td>
<td>Buginés</td>
</tr>
<tr class="even">
<td>97</td>
<td>2C00 - 2C5F</td>
<td>Letra</td>
</tr>
<tr class="odd">
<td>98</td>
<td>2D30 - 2D7F</td>
<td>Tifinagh</td>
</tr>
<tr class="even">
<td>99</td>
<td>4DC0 - 4DFF</td>
<td>Símbolos de Yijing Hexagrama</td>
</tr>
<tr class="odd">
<td>100</td>
<td>A800 - A82F</td>
<td>Syloti Nagri</td>
</tr>
<tr class="even">
<td rowspan="3">101 $ {REMOVE} $<br />
</td>
<td>10000-1007F</td>
<td>Syllabary lineal B</td>
</tr>
<tr class="odd">
<td>10080-100FF</td>
<td>Ideogramas mostrados lineal B</td>

</tr>
<tr class="even">
<td>10100-1013F</td>
<td>Números Egeo</td>

</tr>
<tr class="odd">
<td>102</td>
<td>10140-1018F</td>
<td>Números griegos antiguos</td>
</tr>
<tr class="even">
<td>103</td>
<td>10380-1039F</td>
<td>Ugarítico</td>
</tr>
<tr class="odd">
<td>104</td>
<td>103A0 - 103DF</td>
<td>Persa antiguo</td>
</tr>
<tr class="even">
<td>105</td>
<td>10450-1047F</td>
<td>Shavian</td>
</tr>
<tr class="odd">
<td>106</td>
<td>10480-104AF</td>
<td>Osmanya</td>
</tr>
<tr class="even">
<td>107</td>
<td>10800-1083F</td>
<td>Cypriot Syllabary</td>
</tr>
<tr class="odd">
<td>108</td>
<td>10A00 - 10A5F</td>
<td>Kharoshthi</td>
</tr>
<tr class="even">
<td>109</td>
<td>1D300 - 1D35F</td>
<td>Símbolos de Jing Tai Xuan</td>
</tr>
<tr class="odd">
<td rowspan="2">110 $ {REMOVE} $<br />
</td>
<td>12000-123FF</td>
<td>Cuneiform</td>
</tr>
<tr class="even">
<td>12400-1247F</td>
<td>Cuneiform números y signos de puntuación</td>

</tr>
<tr class="odd">
<td>111</td>
<td>1D360 - 1D37F</td>
<td>Números de la varilla de recuento</td>
</tr>
<tr class="even">
<td>112</td>
<td>1B80 - 1BBF</td>
<td>Sundanés</td>
</tr>
<tr class="odd">
<td>113</td>
<td>1C00 - 1C4F</td>
<td>Lepcha</td>
</tr>
<tr class="even">
<td>114</td>
<td>1C50 - 1C7F</td>
<td>OL Chiki</td>
</tr>
<tr class="odd">
<td>115</td>
<td>A880 - A8DF</td>
<td>Saurashtra</td>
</tr>
<tr class="even">
<td>116</td>
<td>A900 - A92F</td>
<td>Kayah Li</td>
</tr>
<tr class="odd">
<td>117</td>
<td>A930 - A95F</td>
<td>Rejang</td>
</tr>
<tr class="even">
<td>118</td>
<td>AA00 - AA5F</td>
<td>Cham</td>
</tr>
<tr class="odd">
<td>119</td>
<td>10190-101CF</td>
<td>Antiguos símbolos</td>
</tr>
<tr class="even">
<td>120</td>
<td>101D0 - 101FF</td>
<td>Disco Phaistos</td>
</tr>
<tr class="odd">
<td rowspan="3">121 $ {REMOVE} $<br />
</td>
<td>10280-1029F</td>
<td>Licio</td>
</tr>
<tr class="even">
<td>102A0 - 102DF</td>
<td>Cario</td>

</tr>
<tr class="odd">
<td>10920-1093F</td>
<td>Lidio</td>

</tr>
<tr class="even">
<td rowspan="2">122 $ {REMOVE} $<br />
</td>
<td>1F000 - 1F02F</td>
<td>Mosaicos de Mahjong</td>
</tr>
<tr class="odd">
<td>1F030 - 1F09F</td>
<td>Iconos de Domino</td>

</tr>
<tr class="even">
<td>123</td>

<td><strong>Windows 2000 y versiones posteriores:</strong> Progreso del diseño, horizontal de derecha a izquierda</td>
</tr>
<tr class="odd">
<td>124</td>

<td><strong>Windows 2000 y versiones posteriores:</strong> Progreso de diseño, vertical delante de horizontal</td>
</tr>
<tr class="even">
<td>125</td>

<td><strong>Windows 2000 y versiones posteriores:</strong> Progreso de diseño, vertical de abajo arriba</td>
</tr>
<tr class="odd">
<td>126-127</td>

<td>Reservado para uso interno del proceso</td>
</tr>
</tbody>
</table>



 

 

 



