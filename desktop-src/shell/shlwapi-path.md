---
description: En esta sección se describen las funciones Windows control de rutas de acceso de Shell. Los elementos de programación que se explican en esta documentación se exportan Shlwapi.dll y se definen en Shlwapi.h y Shlwapi.lib.
title: Funciones de control de rutas de acceso de shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 90937e4aa3c93c14957ec0db7f081c1cb598989e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481971"
---
# <a name="shell-path-handling-functions"></a>Funciones de control de rutas de acceso de shell

En esta sección se describen las funciones Windows control de rutas de acceso de Shell. Los elementos de programación que se explican en esta documentación se exportan Shlwapi.dll y se definen en Shlwapi.h y Shlwapi.lib.

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a><br /> | Agrega una barra diagonal inversa al final de una cadena para crear la sintaxis correcta para una ruta de acceso. Si la ruta de acceso de origen ya tiene una barra diagonal inversa final, no se agregará ninguna barra diagonal inversa. <br /><blockquote>[!Note]<br />El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda usar la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> más segura en su lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a><br /> | Agrega una extensión de nombre de archivo a una cadena de ruta de acceso.<br /><blockquote>[!Note]<br />El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda usar la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> más segura en su lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a><br /> | Anexa una ruta de acceso al final de otra. <br /><blockquote>[!Note]<br />El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda usar la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> más segura en su lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a><br /> | Crea una ruta de acceso raíz a partir de un número de unidad determinado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathÓniconicalize</strong></a><br /> | Simplifica una ruta de acceso mediante la eliminación de elementos de navegación como "." y ".." para generar una ruta de acceso directa y bien formada.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a><br /> | Concatena dos cadenas que representan rutas de acceso formadas correctamente en una ruta de acceso; también concatena los elementos de ruta de acceso relativos. <br /><blockquote>[!Note]<br />El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda usar la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> más segura en su lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a><br /> | Compara dos rutas de acceso para determinar si comparten un prefijo común. Un prefijo es uno de estos tipos: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a><br /> | Trunca una ruta de acceso de archivo para ajustarla a un ancho de píxel determinado reemplazando los componentes de ruta de acceso por puntos suspensivos.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a><br /> | Trunca una ruta de acceso que cabe dentro de un determinado número de caracteres reemplazando los componentes de ruta de acceso por puntos suspensivos.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a><br /> | Convierte una dirección URL de archivo en una ruta de acceso de Microsoft MS-DOS.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a><br /> | Crea una ruta de acceso a partir de una dirección URL de archivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a><br /> | Determina si una ruta de acceso a un objeto del sistema de archivos, como un archivo o una carpeta, es válida.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a><br /> | Busca una extensión en una ruta de acceso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a><br /> | Busca un nombre de archivo en una ruta de acceso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a><br /> | Analiza una ruta de acceso y devuelve la parte de esa ruta de acceso que sigue a la primera barra diagonal inversa.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a><br /> | Busca un archivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a><br /> | Determina si un nombre de archivo determinado tiene uno de una lista de sufijos.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a><br /> | Busca los argumentos de la línea de comandos dentro de una ruta de acceso determinada.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a><br /> | Determina el tipo de carácter en relación con una ruta de acceso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a><br /> | Busca una ruta de acceso para una letra de unidad dentro del intervalo de "A" a "Z" y devuelve el número de unidad correspondiente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a><br /> | Determina si el tipo de contenido registrado de un archivo coincide con el tipo de contenido especificado. Esta función obtiene el tipo de contenido para el tipo de archivo especificado y compara esa cadena con <em>pszContentType</em>. La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a><br /> | Comprueba que una ruta de acceso es un directorio válido.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a><br /> | Determina si una ruta de acceso especificada es un directorio vacío.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a><br /> | Busca en una ruta de acceso los caracteres que delimitan la ruta de acceso (por ejemplo, ':' o \' '). Si no hay caracteres delimitadores de ruta de acceso, la ruta de acceso se considera una ruta de acceso de especificación de archivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a><br /> | Determina si un archivo es un archivo HTML. La determinación se realiza en función del tipo de contenido registrado para la extensión del archivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a><br /> | Determina si un nombre de archivo tiene un formato largo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a><br /> | Determina si una cadena de ruta de acceso representa un recurso de red.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a><br /> | Busca en una ruta de acceso para determinar si contiene un prefijo válido del tipo pasado por <em>pszPrefix.</em> Un prefijo es uno de estos tipos: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a><br /> | Busca una ruta de acceso y determina si es relativa.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a><br /> | Determina si una cadena de ruta de acceso hace referencia a la raíz de un volumen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a><br /> | Compara dos rutas de acceso para determinar si tienen un componente raíz común.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a><br /> | Determina si una carpeta existente contiene los atributos que la convierten en una carpeta del sistema. Como alternativa, esta función indica si determinados atributos califican una carpeta para ser una carpeta del sistema.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a><br /> | Determina si una cadena de ruta de acceso es una ruta de acceso UNC (Convención de nomenclatura universal) válida, en lugar de una ruta de acceso basada en una letra de unidad.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a><br /> | Determina si una cadena es un UNC válido solo para una ruta de acceso de servidor.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a><br /> | Determina si una cadena es una ruta de acceso de recurso compartido UNC válida, \\ <em>recurso compartido de</em>servidor \<em> </em> .<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a><br /> | Prueba una cadena determinada para determinar si se ajusta a un formato de dirección URL válido.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a><br /> | Convierte una ruta de acceso en mayúsculas a todos los caracteres en minúsculas para dar a la ruta de acceso una apariencia coherente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a><br /> | Proporciona a una carpeta existente los atributos adecuados para convertirse en una carpeta del sistema.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a><br /> | Busca una cadena con un tipo de coincidencia de caracteres comodín MS-DOS.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a><br /> | Coincide con un nombre de archivo de una ruta de acceso con uno o varios patrones de nombre de archivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a><br /> | Analiza una cadena de ubicación de archivo que contiene una ubicación de archivo y un índice de iconos, y devuelve valores independientes.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a><br /> | Busca espacios en una ruta de acceso. Si se encuentran espacios, toda la ruta de acceso se incluye entre comillas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a><br /> | Crea una ruta de acceso relativa de un archivo o carpeta a otro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a><br /> | Quita los argumentos de una ruta de acceso determinada.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a><br /> | Quita la barra diagonal inversa final de una ruta de acceso determinada.<br /><blockquote>[!Note]<br />Esta función es desusada. Se recomienda usar la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> en su lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a><br /> | Quita todos los espacios iniciales y finales de una cadena.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a><br /> | Quita la extensión de nombre de archivo de una ruta de acceso, si hay una. <br /><blockquote>[!Note]<br />Esta función es desusada. Se recomienda el uso de <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> en su lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a><br /> | Quita el nombre de archivo final y la barra diagonal inversa de una ruta de acceso, si están presentes.<br /><blockquote>[!Note]<br />Esta función es desusada. Se recomienda el uso de la <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>función PathCchRemoveFileSpec</strong></a> en su lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a><br /> | Reemplaza la extensión de un nombre de archivo por una nueva extensión. Si el nombre de archivo no contiene una extensión, la extensión se adjuntará al final de la cadena.<br /><blockquote>[!Note]<br />El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda usar la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> más segura en su lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a><br /> | Determina si una ruta de acceso determinada tiene el formato correcto y está completa.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a><br /> | Establece el texto de un control secundario en una ventana o cuadro de diálogo, mediante <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> para asegurarse de que la ruta de acceso se ajuste al control.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a><br /> | Recupera un puntero al primer carácter de una ruta de acceso después de la letra de unidad o los elementos de la ruta de acceso un servidor/recurso compartido UNC.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a><br /> | Quita la parte de la ruta de acceso de un archivo y una ruta de acceso completos.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a><br /> | Quita todos los elementos de archivos y directorios de una ruta de acceso, excepto la información raíz.<br /><blockquote>[!Note]<br />El uso incorrecto de esta función puede provocar una saturación del búfer. Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> más segura en su lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a><br /> | Quita la decoración de una cadena de ruta de acceso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a><br /> | Reemplaza determinados nombres de carpeta en una ruta de acceso completa por su cadena de entorno asociada.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a><br /> | Quita los atributos de una carpeta que lo convierten en una carpeta del sistema. Esta carpeta debe existir realmente en el sistema de archivos.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a><br /> | Quita las comillas del principio y el final de una ruta de acceso.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a><br /> | Comprueba un contexto de enlace para ver si es seguro enlazar a un objeto de componente determinado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a><br /> | Determina un esquema para una cadena de dirección URL especificada y devuelve una cadena con un prefijo adecuado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanalizar</strong></a><br /> | Convierte una cadena de dirección URL al formato canónico.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a><br /> | Cuando se proporciona con una dirección URL relativa y su base, devuelve una dirección URL en formato canónico.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a><br /> | Realiza una comparación que distingue mayúsculas de minúsculas de dos cadenas de dirección URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a><br /> | Convierte una ruta de acceso de MS-DOS en una dirección URL canónica.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a><br /> | Convierte caracteres o pares suplentes en una dirección URL que se puede modificar durante el transporte a través de Internet ("caracteres no seguros") en sus secuencias de escape correspondientes. Los pares suplentes son caracteres entre U+10000 y U+10FFFF (en UTF-32) o entre DC00 y DFFF (en UTF-16). <br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a><br /> | Macro que convierte los caracteres de espacio en su secuencia de escape correspondiente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a><br /> | Recupera la ubicación de una dirección URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a><br /> | Acepta una cadena de dirección URL y devuelve una parte especificada de esa dirección URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a><br /> | Aplica un algoritmo hash a una cadena de dirección URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>Direcciones URL</strong></a><br /> | Comprueba si una dirección URL es un tipo especificado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a><br /> | Prueba una dirección URL para determinar si es una dirección URL de archivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a><br /> | Devuelve si una dirección URL es una dirección URL que los exploradores normalmente no incluyen en el historial de navegación.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a><br /> | Devuelve si una dirección URL es opaca.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a><br /> | Convierte las secuencias de escape de nuevo en caracteres normales.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a><br /> | Convierte las secuencias de escape de nuevo en caracteres normales y sobrescribe la cadena original.<br /> | 




 

 

 




