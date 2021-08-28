---
description: En esta sección se describen las Windows control de cadenas de Shell. Los elementos de programación que se explican en esta documentación se exportan Shlwapi.dll y se definen en Shlwapi.h y Shlwapi.lib.
title: Funciones de control de cadenas de shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d11ad956b6eab11212243232dfaf8ef341d05544
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473321"
---
# <a name="shell-string-handling-functions"></a>Funciones de control de cadenas de shell

En esta sección se describen las Windows control de cadenas de Shell. Los elementos de programación que se explican en esta documentación se exportan Shlwapi.dll y se definen en Shlwapi.h y Shlwapi.lib.

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a><br /> | Realiza una comparación entre dos caracteres. La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a><br /> | Recupera una cadena que se usa con sitios web al especificar las preferencias de idioma.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a><br /> | Realiza una comparación que distingue mayúsculas de minúsculas de un número especificado de caracteres desde el principio de dos cadenas localizadas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a><br /> | Realiza una comparación sin diferenciar mayúsculas de minúsculas de un número especificado de caracteres desde el principio de dos cadenas localizadas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a><br /> | Compara un número especificado de caracteres desde el principio de dos cadenas localizadas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a><br /> | Determina si un carácter representa un espacio.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a><br /> | Extrae un recurso de texto especificado cuando se le asigna ese recurso en forma de cadena indirecta (una cadena que comienza con el símbolo '@').<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a><br /> | Realiza una copia de una cadena en la memoria recién asignada.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br /> | Anexa una cadena a otra. <br /><blockquote>[!Note]<br />No debe usarse. Vea Comentarios para funciones alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a><br /> | Copia y anexa caracteres de una cadena al final de otra. <br /><blockquote>[!Note]<br />No debe usarse. Vea Comentarios para funciones alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a><br /> | Concatena dos cadenas Unicode. Se usa cuando se requieren concatenaciones repetidas en el mismo búfer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br /> | Busca en una cadena la primera aparición de un carácter que coincida con el carácter especificado. La comparación distingue mayúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a><br /> | Busca en una cadena la primera aparición de un carácter que coincida con el carácter especificado. La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a><br /> | Busca en una cadena la primera aparición de un carácter especificado. La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a><br /> | Busca en una cadena la primera aparición de un carácter especificado. La comparación distingue mayúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a><br /> | Compara dos cadenas para determinar si son iguales. La comparación distingue mayúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a><br /> | Compara cadenas mediante reglas de intercalación en tiempo de ejecución de C (ASCII). La comparación distingue mayúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br /> | Compara dos cadenas para determinar si son iguales. La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a><br /> | Compara dos cadenas mediante reglas de intercalación en tiempo de ejecución de C (ASCII). La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a><br /> | Compara dos cadenas Unicode. Los dígitos de las cadenas se consideran contenido numérico en lugar de texto. Esta prueba no distingue mayúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a><br /> | Compara un número especificado de caracteres desde el principio de dos cadenas para determinar si son iguales. La comparación distingue mayúsculas de minúsculas. La <strong>macro StrNCmp</strong> difiere de esta función solo en el nombre.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a><br /> | Compara un número especificado de caracteres desde el principio de dos cadenas mediante reglas de intercalación en tiempo de ejecución de C (ASCII). La comparación distingue mayúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a><br /> | Compara un número especificado de caracteres desde el principio de dos cadenas para determinar si son iguales. La comparación no distingue entre mayúsculas y minúsculas. La <strong>macro StrNCmpI</strong> difiere de esta función solo en el nombre.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a><br /> | Compara un número especificado de caracteres desde el principio de dos cadenas mediante reglas de intercalación en tiempo de ejecución de C (ASCII). La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>Strcpy</strong></a><br /> | Copia una cadena en otra. <br /><blockquote>[!Note]<br />No debe usarse. Vea Comentarios para funciones alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a><br /> | Copia un número especificado de caracteres desde el principio de una cadena a otra.<br /><blockquote>[!Note]<br />No use esta función ni la macro <strong>StrNCpy.</strong> Vea Comentarios para funciones alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br /> | Busca en una cadena la primera aparición de cualquiera de los grupos de caracteres. El método de búsqueda distingue mayúsculas de minúsculas y el carácter <strong>NULL</strong> de terminación se incluye dentro de la coincidencia del patrón de búsqueda.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a><br /> | Busca en una cadena la primera aparición de cualquiera de los grupos de caracteres. El método de búsqueda no distingue mayúsculas de minúsculas y el carácter <strong>NULL</strong> de terminación se incluye dentro de la coincidencia del patrón de búsqueda.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br /> | Duplica una cadena.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br /> | Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en bytes, kilobytes, megabytes o gigabytes, según el tamaño.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a><br /> | Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en bytes, kilobytes, megabytes o gigabytes, según el tamaño. Difiere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW en</strong></a> un tipo de parámetro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a><br /> | Convierte un valor numérico en una cadena que representa el número en bytes, kilobytes, megabytes o gigabytes, según el tamaño. Extiende <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW al</strong></a> ofrecer la opción de redondear al dígito mostrado más cercano o descartar los dígitos no mostrados.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a><br /> | Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en bytes, kilobytes, megabytes o gigabytes, según el tamaño. Difiere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA en</strong></a> un tipo de parámetro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a><br /> | Convierte un valor numérico en una cadena que representa el número expresado como un valor de tamaño en kilobytes.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a><br /> | Convierte un intervalo de tiempo, especificado en milisegundos, en una cadena.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a><br /> | Compara un número especificado de caracteres desde el principio de dos cadenas para determinar si son iguales.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br /> | Anexa un número especificado de caracteres desde el principio de una cadena hasta el final de otra. <br /><blockquote>[!Note]<br />No use esta función ni la macro <strong>StrCatN.</strong> Vea Comentarios para ver funciones alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br /> | Busca en una cadena la primera aparición de un carácter contenido en un búfer especificado. Esta búsqueda no incluye el carácter nulo de terminación.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br /> | Busca en una cadena la última aparición de un carácter especificado. La comparación distingue mayúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a><br /> | Busca en una cadena la última aparición de un carácter especificado. La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a><br /> | Acepta una estructura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> que contiene o apunta a una cadena y devuelve esa cadena como <a href="/previous-versions/windows/desktop/automat/bstr"><strong>un BSTR</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a><br /> | Convierte una <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>estructura STRRET</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> en una cadena y coloca el resultado en un búfer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a><br /> | Toma una <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>estructura STRRET</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> y devuelve un puntero a una cadena asignada que contiene el nombre para mostrar.<br /> | 
| <a href="strrettostrn.md"><strong>StrRetToStrN</strong></a><br /> | Toma una <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>estructura STRRET</strong></a> devuelta por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf,</strong></a>la convierte en una cadena y coloca el resultado en un búfer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a><br /> | Busca la última aparición de una subcadena especificada dentro de una cadena. La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br /> | Obtiene la longitud de una subcadena dentro de una cadena que consta completamente de caracteres contenidos en un búfer especificado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a><br /> | Busca la primera aparición de una subcadena dentro de una cadena. La comparación distingue mayúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a><br /> | Busca la primera aparición de una subcadena dentro de una cadena. La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a><br /> | Convierte una cadena que representa un valor decimal en un entero. La <strong>macro StrToLong</strong> es idéntica a esta función.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br /> | Convierte una cadena que representa un valor decimal o hexadecimal en un entero de 64 bits.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a><br /> | Convierte una cadena que representa un número decimal o hexadecimal en un entero.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a><br /> | Quita los caracteres iniciales y finales especificados de una cadena.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br /> | Toma una lista de argumentos de longitud variable y devuelve los valores de los argumentos como una cadena con formato <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf-</strong></a>style. <br /><blockquote>[!Note]<br />No use esta función. Vea Comentarios para ver funciones alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br /> | Toma una lista de argumentos y devuelve los valores de los argumentos como una cadena con formato <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf-style.</strong></a> <br /><blockquote>[!Note]<br />No use esta función. Vea Comentarios para ver funciones alternativas.</blockquote><br /> | 




 

 

 
