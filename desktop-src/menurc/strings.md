---
title: Cadenas
description: En esta sección se describen las funciones de cadena.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- recursos, cadenas
- cadenas
- funciones de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795225"
---
# <a name="strings"></a>Cadenas

En esta sección se describen las funciones de cadena y se explica cómo usarlas en las aplicaciones.

### <a name="in-this-section"></a>En esta sección



| Nombre                                     | Descripción                                             |
|------------------------------------------|---------------------------------------------------------|
| [Acerca de las cadenas](about-strings.md)       | Describe las funciones de cadena.<br/>              |
| [Acerca de strsafe. h](strsafe-ovw.md)       | Describe las funciones de cadena en strsafe. h.<br/> |
| [Referencia de cadena](string-reference.md) | Contiene la referencia de la API.<br/>                  |



 

### <a name="string-functions"></a>Funciones de cadena



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></td>
<td>Convierte una cadena de caracteres o un carácter individual en minúsculas. Si el operando es una cadena de caracteres, la función convierte los caracteres en su lugar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></td>
<td>Convierte los caracteres en mayúsculas de un búfer en caracteres en minúsculas. La función convierte los caracteres en su lugar. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></td>
<td>Recupera un puntero al siguiente carácter de una cadena. Esta función puede controlar cadenas que se componen de caracteres de un solo byte o de varios bytes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></td>
<td>Recupera el puntero al siguiente carácter de una cadena. Esta función puede controlar cadenas que se componen de caracteres de un solo byte o de varios bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></td>
<td>Recupera un puntero al carácter anterior en una cadena. Esta función puede controlar cadenas que se componen de caracteres de un solo byte o de varios bytes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></td>
<td>Recupera el puntero al carácter anterior en una cadena. Esta función puede controlar cadenas que se componen de caracteres de un solo byte o de varios bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></td>
<td>Convierte una cadena en el juego de caracteres definido por el OEM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></td>
<td>Convierte un número especificado de caracteres de una cadena en el juego de caracteres definido por el OEM.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></td>
<td>Convierte una cadena de caracteres o un carácter individual en mayúsculas. Si el operando es una cadena de caracteres, la función convierte los caracteres en su lugar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></td>
<td>Convierte los caracteres en minúsculas de un búfer en caracteres en mayúsculas. La función convierte los caracteres en su lugar. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></td>
<td>Compara dos cadenas de caracteres con la configuración regional especificada.
<blockquote>
[!Note]<br />
Para ofrecer compatibilidad con Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> o la versión Unicode de <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></td>
<td>Compara dos cadenas Unicode (caracteres anchos) con la configuración regional especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></td>
<td>Asigna una cadena a otra, realizando una opción de transformación especificada. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></td>
<td>Recupera información de tipo de carácter de los caracteres de la cadena de origen especificada. Para cada carácter de la cadena, la función establece uno o varios bits en el elemento de 16 bits correspondiente de la matriz de salida. Cada bit identifica un tipo de carácter determinado, como si el carácter es una letra, un dígito o ninguno de los dos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></td>
<td>Recupera información de tipo de carácter de los caracteres de la cadena de origen especificada. Para cada carácter de la cadena, la función establece uno o varios bits en el elemento de 16 bits correspondiente de la matriz de salida. Cada bit identifica un tipo de carácter determinado, como si el carácter es una letra, un dígito o ninguno de los dos. <br/> A diferencia de sus parientes cercanos <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> y <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exhibe un comportamiento estándar mediante el uso del modificador de <strong> # definición de Unicode</strong> . Es la función recomendada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></td>
<td>Recupera información de tipo de carácter de los caracteres de la cadena de origen especificada. Para cada carácter de la cadena, la función establece uno o varios bits en el elemento de 16 bits correspondiente de la matriz de salida. Cada bit identifica un tipo de carácter determinado, como si el carácter es una letra, un dígito o ninguno de los dos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></td>
<td>Determina si un carácter es un carácter alfabético. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></td>
<td>Determina si un carácter es un carácter alfabético o numérico. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></td>
<td>Determina si un carácter está en minúsculas. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></td>
<td>Determina si un carácter está en mayúsculas. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través del panel de control. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>Fall</strong></a></td>
<td>Carga un recurso de cadena desde el archivo ejecutable asociado a un módulo especificado, copia la cadena en un búfer y anexa un carácter nulo de terminación.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></td>
<td>Anexa una cadena a otra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></td>
<td>Compara dos cadenas de caracteres. La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></td>
<td>Compara dos cadenas de caracteres. La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></td>
<td>Copia una cadena en un búfer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></td>
<td>Copia un número especificado de caracteres de una cadena de origen en un búfer. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></td>
<td>Determina la longitud de la cadena especificada (sin incluir el carácter nulo de terminación).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></td>
<td>Convierte una cadena del juego de caracteres definido por el OEM en una cadena ANSI o de caracteres anchos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></td>
<td>Convierte un número especificado de caracteres de una cadena del juego de caracteres definido por el OEM en una cadena ANSI o de caracteres anchos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></td>
<td>Escribe datos con formato en el búfer especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></td>
<td>Escribe datos con formato en el búfer especificado mediante un puntero a una lista de argumentos.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a>Funciones strsafe



| Nombre                                             | Descripción                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | Concatena una cadena en otra cadena.<br/>                                            |
| [**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | Concatena una cadena en otra cadena.<br/>                                            |
| [**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | Concatena el número especificado de bytes de una cadena a otra.<br/>         |
| [**StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | Concatena el número especificado de bytes de una cadena a otra.<br/>         |
| [**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | Copia una cadena en otra.<br/>                                                         |
| [**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | Copia una cadena en otra.<br/>                                                         |
| [**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | Copia el número especificado de bytes de una cadena a otra.<br/>                      |
| [**StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | Copia el número especificado de bytes de una cadena a otra.<br/>                      |
| [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | Obtiene una línea de texto de stdin, hasta el carácter de nueva línea (' \\ n ') y lo incluye.<br/>  |
| [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | Obtiene una línea de texto de stdin, hasta el carácter de nueva línea (' \\ n ') y lo incluye.<br/>  |
| [**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | Determina si una cadena supera la longitud especificada, en bytes.<br/>                   |
| [**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | Escribe datos con formato en la cadena especificada.<br/>                                        |
| [**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | Escribe datos con formato en la cadena especificada.<br/>                                        |
| [**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | Escribe datos con formato en la cadena especificada utilizando un puntero a una lista de argumentos.<br/> |
| [**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | Escribe datos con formato en la cadena especificada utilizando un puntero a una lista de argumentos.<br/> |
| [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | Concatena una cadena en otra cadena.<br/>                                            |
| [**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | Concatena una cadena en otra cadena.<br/>                                            |
| [**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | Concatena el número especificado de caracteres de una cadena a otra.<br/>    |
| [**StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | Concatena el número especificado de caracteres de una cadena a otra.<br/>    |
| [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | Copia una cadena en otra.<br/>                                                         |
| [**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | Copia una cadena en otra.<br/>                                                         |
| [**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | Copia el número especificado de caracteres de una cadena a otra.<br/>                 |
| [**StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | Copia el número especificado de caracteres de una cadena a otra.<br/>                 |
| [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | Obtiene una línea de texto de stdin, hasta el carácter de nueva línea (' \\ n ') y lo incluye.<br/>  |
| [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | Obtiene una línea de texto de stdin, hasta el carácter de nueva línea (' \\ n ') y lo incluye.<br/>  |
| [**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | Determina si una cadena supera la longitud especificada, en caracteres.<br/>              |
| [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | Escribe datos con formato en la cadena especificada.<br/>                                        |
| [**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | Escribe datos con formato en la cadena especificada.<br/>                                        |
| [**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | Escribe datos con formato en la cadena especificada utilizando un puntero a una lista de argumentos.<br/> |
| [**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | Escribe datos con formato en la cadena especificada utilizando un puntero a una lista de argumentos.<br/> |



 

 

