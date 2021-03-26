---
description: En esta sección se describen las funciones de control de cadenas de Shell de Windows. Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.
title: Funciones de control de cadenas de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002798"
---
# <a name="shell-string-handling-functions"></a>Funciones de control de cadenas de Shell

En esta sección se describen las funciones de control de cadenas de Shell de Windows. Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a><br/></td>
<td>Realiza una comparación entre dos caracteres. La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a><br/></td>
<td>Recupera una cadena que se usa con websites al especificar las preferencias de idioma.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a><br/></td>
<td>Realiza una comparación con distinción entre mayúsculas y minúsculas de un número especificado de caracteres desde el principio de dos cadenas localizadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a><br/></td>
<td>Realiza una comparación sin distinción entre mayúsculas y minúsculas de un número especificado de caracteres desde el principio de dos cadenas localizadas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a><br/></td>
<td>Compara un número especificado de caracteres desde el principio de dos cadenas localizadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a><br/></td>
<td>Determina si un carácter representa un espacio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a><br/></td>
<td>Extrae un recurso de texto especificado cuando se proporciona ese recurso en forma de cadena indirecta (una cadena que comienza con el símbolo "@").<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a><br/></td>
<td>Realiza una copia de una cadena en la memoria recién asignada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br/></td>
<td>Anexa una cadena a otra. <br/>
<blockquote>
[!Note]<br />
No debe usarse. Vea la sección Comentarios para ver otras funciones.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a><br/></td>
<td>Copia y anexa caracteres de una cadena al final de otro. <br/>
<blockquote>
[!Note]<br />
No debe usarse. Vea la sección Comentarios para ver otras funciones.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a><br/></td>
<td>Concatena dos cadenas Unicode. Se usa cuando se requieren concatenaciones repetidas en el mismo búfer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br/></td>
<td>Busca en una cadena la primera aparición de un carácter que coincida con el carácter especificado. La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a><br/></td>
<td>Busca en una cadena la primera aparición de un carácter que coincida con el carácter especificado. La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a><br/></td>
<td>Busca en una cadena la primera aparición de un carácter especificado. La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a><br/></td>
<td>Busca en una cadena la primera aparición de un carácter especificado. La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a><br/></td>
<td>Compara dos cadenas para determinar si son iguales. La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a><br/></td>
<td>Compara cadenas mediante las reglas de intercalación de C en tiempo de ejecución (ASCII). La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br/></td>
<td>Compara dos cadenas para determinar si son iguales. La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a><br/></td>
<td>Compara dos cadenas mediante las reglas de intercalación en tiempo de ejecución de C (ASCII). La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a><br/></td>
<td>Compara dos cadenas Unicode. Los dígitos de las cadenas se consideran como contenido numérico en lugar de texto. Esta prueba no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a><br/></td>
<td>Compara un número especificado de caracteres desde el principio de dos cadenas para determinar si son iguales. La comparación distingue entre mayúsculas y minúsculas. La macro <strong>StrNCmp</strong> difiere de esta función solo en Name.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a><br/></td>
<td>Compara un número especificado de caracteres desde el principio de dos cadenas mediante las reglas de intercalación de C en tiempo de ejecución (ASCII). La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a><br/></td>
<td>Compara un número especificado de caracteres desde el principio de dos cadenas para determinar si son iguales. La comparación no distingue entre mayúsculas y minúsculas. La macro <strong>StrNCmpI</strong> difiere de esta función solo en Name.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a><br/></td>
<td>Compara un número especificado de caracteres desde el principio de dos cadenas mediante las reglas de intercalación de C en tiempo de ejecución (ASCII). La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a><br/></td>
<td>Copia una cadena en otra. <br/>
<blockquote>
[!Note]<br />
No debe usarse. Vea la sección Comentarios para ver otras funciones.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a><br/></td>
<td>Copia un número especificado de caracteres desde el principio de una cadena a otra.<br/>
<blockquote>
[!Note]<br />
No use esta función ni la macro <strong>StrNCpy</strong> . Vea la sección Comentarios para ver otras funciones.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br/></td>
<td>Busca en una cadena la primera aparición de cualquiera de los grupos de caracteres. El método de búsqueda distingue entre mayúsculas y minúsculas y el carácter <strong>nulo</strong> final se incluye en la coincidencia del patrón de búsqueda.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a><br/></td>
<td>Busca en una cadena la primera aparición de cualquiera de los grupos de caracteres. El método de búsqueda no distingue entre mayúsculas y minúsculas y el carácter <strong>nulo</strong> final se incluye en la coincidencia del patrón de búsqueda.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br/></td>
<td>Duplica una cadena.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br/></td>
<td>Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en bytes, kilobytes, megabytes o gigabytes, dependiendo del tamaño.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a><br/></td>
<td>Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en bytes, kilobytes, megabytes o gigabytes, dependiendo del tamaño. Difiere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> en un tipo de parámetro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a><br/></td>
<td>Convierte un valor numérico en una cadena que representa el número en bytes, kilobytes, megabytes o gigabytes, dependiendo del tamaño. Extiende <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> ofreciendo la opción de redondear al dígito mostrado más próximo o descartar los dígitos no mostrados.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a><br/></td>
<td>Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en bytes, kilobytes, megabytes o gigabytes, dependiendo del tamaño. Difiere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> en un tipo de parámetro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a><br/></td>
<td>Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en kilobytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a><br/></td>
<td>Convierte un intervalo de tiempo, especificado en milisegundos, en una cadena.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a><br/></td>
<td>Compara un número especificado de caracteres desde el principio de dos cadenas para determinar si son iguales.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br/></td>
<td>Anexa un número especificado de caracteres desde el principio de una cadena hasta el final de otro. <br/>
<blockquote>
[!Note]<br />
No use esta función ni la macro <strong>StrCatN</strong> . Vea la sección Comentarios para ver otras funciones.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br/></td>
<td>Busca en una cadena la primera aparición de un carácter incluido en un búfer especificado. Esta búsqueda no incluye el carácter nulo de terminación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br/></td>
<td>Busca en una cadena la última aparición de un carácter especificado. La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a><br/></td>
<td>Busca en una cadena la última aparición de un carácter especificado. La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a><br/></td>
<td>Acepta una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> que contiene o apunta a una cadena y devuelve esa cadena como <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a><br/></td>
<td>Convierte una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> en una cadena y coloca el resultado en un búfer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a><br/></td>
<td>Toma una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> y devuelve un puntero a una cadena asignada que contiene el nombre para mostrar.<br/></td>
</tr>
<tr class="even">
<td><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a><br/></td>
<td>Toma una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a>, la convierte en una cadena y coloca el resultado en un búfer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a><br/></td>
<td>Busca la última aparición de una subcadena especificada en una cadena. La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br/></td>
<td>Obtiene la longitud de una subcadena dentro de una cadena que se compone íntegramente de caracteres contenidos en un búfer especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a><br/></td>
<td>Busca la primera aparición de una subcadena en una cadena. La comparación distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a><br/></td>
<td>Busca la primera aparición de una subcadena en una cadena. La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a><br/></td>
<td>Convierte una cadena que representa un valor decimal en un entero. La macro <strong>StrToLong</strong> es idéntica a esta función.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br/></td>
<td>Convierte una cadena que representa un valor decimal o hexadecimal en un entero de 64 bits.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a><br/></td>
<td>Convierte una cadena que representa un número decimal o hexadecimal en un entero.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a><br/></td>
<td>Quita los caracteres inicial y final especificados de una cadena.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br/></td>
<td>Toma una lista de argumentos de longitud variable y devuelve los valores de los argumentos como una cadena con formato de estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br/>
<blockquote>
[!Note]<br />
No utilice esta función. Vea la sección Comentarios para ver otras funciones.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br/></td>
<td>Toma una lista de argumentos y devuelve los valores de los argumentos como una cadena con formato de estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br/>
<blockquote>
[!Note]<br />
No utilice esta función. Vea la sección Comentarios para ver otras funciones.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
