---
description: En esta sección se describen las funciones de control de rutas del shell de Windows. Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.
title: Funciones de control de rutas de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997904"
---
# <a name="shell-path-handling-functions"></a>Funciones de control de rutas de Shell

En esta sección se describen las funciones de control de rutas del shell de Windows. Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.

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
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a><br/></td>
<td>Agrega una barra diagonal inversa al final de una cadena para crear la sintaxis correcta para una ruta de acceso. Si la ruta de acceso de origen ya tiene una barra diagonal inversa al final, no se agregará ninguna barra diagonal inversa. <br/>
<blockquote>
[!Note]<br />
El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> más segura en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a><br/></td>
<td>Agrega una extensión de nombre de archivo a una cadena de ruta de acceso.<br/>
<blockquote>
[!Note]<br />
El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> más segura en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a><br/></td>
<td>Anexa una ruta de acceso al final de otro. <br/>
<blockquote>
[!Note]<br />
El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> más segura en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a><br/></td>
<td>Crea una ruta de acceso raíz a partir de un número de unidad determinado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a><br/></td>
<td>Simplifica una ruta de acceso quitando elementos de navegación como &quot; . &quot; y &quot; .. &quot; para generar un trazado directo y con formato correcto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a><br/></td>
<td>Concatena dos cadenas que representan rutas de acceso con formato correcto en una ruta de acceso; también concatena cualquier elemento de ruta de acceso relativa. <br/>
<blockquote>
[!Note]<br />
El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> más segura en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a><br/></td>
<td>Compara dos rutas de acceso para determinar si comparten un prefijo común. Un prefijo es uno de estos tipos: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a><br/></td>
<td>Trunca una ruta de acceso de archivo para ajustarse a un ancho de píxel determinado reemplazando los componentes de la ruta de acceso con puntos suspensivos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a><br/></td>
<td>Trunca una ruta de acceso para ajustarse a un determinado número de caracteres reemplazando los componentes de la ruta de acceso con puntos suspensivos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a><br/></td>
<td>Convierte una dirección URL de archivo en una ruta de acceso de Microsoft MS-DOS.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a><br/></td>
<td>Crea una ruta de acceso a partir de una dirección URL de archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a><br/></td>
<td>Determina si una ruta de acceso a un objeto del sistema de archivos, como un archivo o una carpeta, es válida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a><br/></td>
<td>Busca una extensión en una ruta de acceso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a><br/></td>
<td>Busca un nombre de archivo en una ruta de acceso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a><br/></td>
<td>Analiza una ruta de acceso y devuelve la parte de esa ruta de acceso que sigue a la primera barra diagonal inversa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a><br/></td>
<td>Busca un archivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a><br/></td>
<td>Determina si un nombre de archivo determinado tiene una lista de sufijos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a><br/></td>
<td>Busca los argumentos de la línea de comandos en una ruta de acceso dada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a><br/></td>
<td>Determina el tipo de carácter en relación con una ruta de acceso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a><br/></td>
<td>Busca una letra de unidad en el intervalo de la "A" a la "Z" y devuelve el número de unidad correspondiente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a><br/></td>
<td>Determina si el tipo de contenido registrado de un archivo coincide con el tipo de contenido especificado. Esta función obtiene el tipo de contenido para el tipo de archivo especificado y lo compara con el valor de <em>pszContentType</em>. La comparación no distingue entre mayúsculas y minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a><br/></td>
<td>Comprueba que una ruta de acceso es un directorio válido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a><br/></td>
<td>Determina si una ruta de acceso especificada es un directorio vacío.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a><br/></td>
<td>Busca en una ruta de acceso todos los caracteres delimitadores de ruta de acceso (por ejemplo, ': ' o ' \' ). Si no hay caracteres que delimiten la ruta de acceso, la ruta de acceso se considera una ruta de acceso de especificación de archivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a><br/></td>
<td>Determina si un archivo es un archivo HTML. La determinación se realiza en función del tipo de contenido que se registra para la extensión del archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a><br/></td>
<td>Determina si un nombre de archivo está en formato largo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a><br/></td>
<td>Determina si una cadena de ruta de acceso representa un recurso de red.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a><br/></td>
<td>Busca una ruta de acceso para determinar si contiene un prefijo válido del tipo pasado por <em>pszPrefix</em>. Un prefijo es uno de estos tipos: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a><br/></td>
<td>Busca una ruta de acceso y determina si es relativa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a><br/></td>
<td>Determina si una cadena de ruta de acceso hace referencia a la raíz de un volumen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a><br/></td>
<td>Compara dos rutas de acceso para determinar si tienen un componente raíz común.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a><br/></td>
<td>Determina si una carpeta existente contiene los atributos que lo convierten en una carpeta del sistema. Como alternativa, esta función indica si ciertos atributos califican que una carpeta es una carpeta del sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a><br/></td>
<td>Determina si una cadena de ruta de acceso es una ruta de acceso UNC (Convención de nomenclatura universal) válida, en lugar de una ruta de acceso basada en una letra de unidad.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a><br/></td>
<td>Determina si una cadena es una UNC válida solo para una ruta de acceso de servidor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a><br/></td>
<td>Determina si una cadena es una ruta de acceso de recurso compartido UNC válida, un \\ <em></em> \ <em>recurso compartido</em>de servidor.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a><br/></td>
<td>Comprueba una cadena determinada para determinar si se ajusta a un formato de dirección URL válido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a><br/></td>
<td>Convierte una ruta de acceso todo en mayúsculas a todos los caracteres en minúsculas para dar una apariencia coherente a la ruta de acceso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a><br/></td>
<td>Proporciona a una carpeta existente los atributos adecuados para convertirse en una carpeta del sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a><br/></td>
<td>Busca una cadena mediante un tipo de coincidencia de caracteres comodín de MS-DOS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a><br/></td>
<td>Coincide con un nombre de archivo de una ruta de acceso con uno o más patrones de nombre de archivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a><br/></td>
<td>Analiza una cadena de ubicación de archivo que contiene una ubicación de archivo e índice de icono, y devuelve valores distintos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a><br/></td>
<td>Busca espacios en una ruta de acceso. Si se encuentran espacios, toda la ruta de acceso está entre comillas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a><br/></td>
<td>Crea una ruta de acceso relativa de un archivo o carpeta a otro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a><br/></td>
<td>Quita todos los argumentos de una ruta de acceso determinada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a><br/></td>
<td>Quita la barra diagonal inversa final de una ruta de acceso determinada.<br/>
<blockquote>
[!Note]<br />
Esta función es desusada. Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a><br/></td>
<td>Quita todos los espacios iniciales y finales de una cadena.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a><br/></td>
<td>Quita la extensión de nombre de archivo de una ruta de acceso, si está presente. <br/>
<blockquote>
[!Note]<br />
Esta función es desusada. Se recomienda el uso de <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a><br/></td>
<td>Quita el nombre de archivo final y la barra diagonal inversa de una ruta de acceso, si están presentes.<br/>
<blockquote>
[!Note]<br />
Esta función es desusada. Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a><br/></td>
<td>Reemplaza la extensión de un nombre de archivo por una nueva extensión. Si el nombre de archivo no contiene una extensión, la extensión se adjuntará al final de la cadena.<br/>
<blockquote>
[!Note]<br />
El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> más segura en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a><br/></td>
<td>Determina si una ruta de acceso dada tiene un formato correcto y completo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a><br/></td>
<td>Establece el texto de un control secundario en una ventana o un cuadro de diálogo, usando <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> para asegurarse de que la ruta de acceso quepa en el control.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a><br/></td>
<td>Recupera un puntero al primer carácter de una ruta de acceso después de los elementos de la letra de unidad o del servidor UNC/ruta de acceso del recurso compartido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a><br/></td>
<td>Quita la parte de la ruta de acceso de un archivo y una ruta de acceso completos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a><br/></td>
<td>Quita todos los elementos de archivo y directorio de una ruta de acceso excepto la información raíz.<br/>
<blockquote>
[!Note]<br />
El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> más segura en su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a><br/></td>
<td>Quita la decoración de una cadena de ruta de acceso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a><br/></td>
<td>Reemplaza algunos nombres de carpeta en una ruta de acceso completa con su cadena de entorno asociada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a><br/></td>
<td>Quita los atributos de una carpeta que lo convierten en una carpeta del sistema. Esta carpeta debe existir realmente en el sistema de archivos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a><br/></td>
<td>Quita las comillas del principio y el final de una ruta de acceso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a><br/></td>
<td>Comprueba un contexto de enlace para ver si es seguro enlazar a un objeto de componente determinado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a><br/></td>
<td>Determina un esquema para una cadena de dirección URL especificada y devuelve una cadena con un prefijo adecuado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a><br/></td>
<td>Convierte una cadena de dirección URL al formato canónico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a><br/></td>
<td>Cuando se proporciona con una dirección URL relativa y su base, devuelve una dirección URL en formato canónico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a><br/></td>
<td>Crea una comparación que distingue entre mayúsculas y minúsculas de dos cadenas URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a><br/></td>
<td>Convierte una ruta de acceso de MS-DOS en una dirección URL con formato canónico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a><br/></td>
<td>Convierte caracteres o pares suplentes en una dirección URL que podrían modificarse durante el transporte a través de Internet ( &quot; caracteres no seguros &quot; ) en sus secuencias de escape correspondientes. Los pares suplentes son caracteres entre U + 10000 y U + 10FFFF (en UTF-32) o entre DC00 y DFFF (en UTF-16). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a><br/></td>
<td>Macro que convierte los caracteres de espacio en la secuencia de escape correspondiente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a><br/></td>
<td>Recupera la ubicación de una dirección URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a><br/></td>
<td>Acepta una cadena de dirección URL y devuelve una parte especificada de esa dirección URL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a><br/></td>
<td>Aplica un algoritmo hash a una cadena de dirección URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a><br/></td>
<td>Comprueba si una dirección URL es un tipo especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a><br/></td>
<td>Prueba una dirección URL para determinar si es una dirección URL de archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a><br/></td>
<td>Devuelve si una dirección URL es una dirección URL que los exploradores no incluyen normalmente en el historial de navegación.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a><br/></td>
<td>Devuelve si una dirección URL es opaca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a><br/></td>
<td>Vuelve a convertir las secuencias de escape en caracteres ordinarios.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a><br/></td>
<td>Vuelve a convertir las secuencias de escape en caracteres ordinarios y sobrescribe la cadena original.<br/></td>
</tr>
</tbody>
</table>



 

 

 




