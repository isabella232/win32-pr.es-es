---
description: La biblioteca DbgHelp utiliza la ruta de acceso de búsqueda de símbolos para buscar símbolos de depuración (archivos. PDB y. dbg). La ruta de búsqueda puede estar formada por uno o varios elementos de la ruta de acceso separados por punto y coma.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Rutas de acceso de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998218"
---
# <a name="symbol-paths"></a>Rutas de acceso de símbolos

La biblioteca DbgHelp utiliza la ruta de acceso de búsqueda de símbolos para buscar símbolos de depuración (archivos. PDB y. dbg). La ruta de búsqueda puede estar formada por uno o varios elementos de la ruta de acceso separados por punto y coma.

## <a name="specifying-search-paths"></a>Especificar rutas de acceso de búsqueda

Para especificar dónde buscará el controlador de símbolos los archivos de símbolos, llame a la función [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) . Como alternativa, puede especificar una ruta de acceso de búsqueda de símbolos en el parámetro *UserSearchPath* de la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

El parámetro *UserSearchPath* de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) y el parámetro *SearchPath* en [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) toman un puntero a una cadena terminada en null que especifica una ruta de acceso o una serie de rutas de acceso separadas por un punto y coma. El controlador de símbolos usa estas rutas de acceso para buscar archivos de símbolos. Si este parámetro es **null**, el controlador de símbolos busca en el directorio que contiene el módulo para el que se buscan los símbolos. De lo contrario, si este parámetro se especifica como un valor distinto de **null** , el controlador de símbolos busca primero las rutas de acceso establecidas por la aplicación antes de buscar en el directorio del módulo. Si establece la \_ ruta de \_ acceso de símbolos NT o la \_ variable de \_ \_ entorno Path de símbolos NT ALT \_ \_ , el controlador de símbolos busca archivos de símbolos en el orden siguiente:

1. \_Variable de \_ entorno de ruta de acceso de símbolos NT \_ .
2. La \_ \_ variable de \_ entorno de ruta de acceso Symbol de NT ALT \_ .
3. Directorio que contiene el módulo correspondiente.

Para recuperar las rutas de acceso de búsqueda, llame a la función [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) .

La ruta de búsqueda de los archivos de base de datos de programa (. pdb) es diferente de la ruta de acceso para los archivos de depuración (. dbg). El algoritmo viene determinado por la funcionalidad de la biblioteca de símbolos. De forma predeterminada, Microsoft Visual C/C++ crea símbolos de formato de Microsoft, los quita de la imagen y los coloca en un archivo. pdb independiente. Normalmente, el archivo. pdb se ubicará en el directorio que contiene la imagen ejecutable. Visual C/C++ incrusta la ruta de acceso absoluta al archivo. pdb en la imagen ejecutable. Si el controlador de símbolos no encuentra el archivo. pdb en esa ubicación o si el archivo. pdb se ha migrado a otro directorio, el controlador de símbolos buscará el archivo. pdb mediante la ruta de acceso de búsqueda descrita para los archivos. dbg.

## <a name="path-element-types"></a>Tipos de elemento de ruta de acceso

Hay tres tipos de elementos de ruta de acceso.

### <a name="standard-path-element"></a>Elemento path estándar

Para buscar un elemento de ruta de acceso estándar, se busca en la raíz del directorio especificado por el elemento path. El controlador de símbolos también busca en un subdirectorio de "Symbols" que coincida con la extensión de archivo del módulo que se está buscando en los símbolos. Suele ser "dll", "exe" o "sys". Por último, busca en un subdirectorio denominado "Symbols" con un directorio con el mismo nombre que la extensión. Por ejemplo, si el elemento de ruta de acceso de símbolos es "c: \\ símbolos" y el archivo en el que se buscan los símbolos es "boo.dll", se buscarían los siguientes directorios.

- c: \\ símbolos  
- c: \\ símbolos \\ dll  
- c: \\ \\ símbolos dll de símbolos \\  

El controlador de símbolos usa esta lógica para buscar en cualquier elemento de la ruta de acceso que no cumple los criterios como un *servidor de símbolos* o *caché* (se describe a continuación).

### <a name="symbol-server-path-element"></a>Elemento path del servidor de símbolos

Un elemento de ruta de acceso del *servidor de símbolos* usa una tecnología especial que puede buscar un símbolo que sea una coincidencia exacta del módulo en cuestión. Consulte [uso de SymSrv](using-symsrv.md) para obtener más información.

El controlador de símbolos trata un elemento de ruta de acceso como un servidor de símbolos si comienza con el texto "SRV \* ".

> [!Note]  
> Si \* no se especifica el texto "SRV" pero el elemento de ruta de acceso real es un almacén del servidor de símbolos, el controlador de símbolos actuará como si \* se hubiera especificado "SRV". El controlador de símbolos realiza esta determinación buscando la existencia de un archivo llamado "pingme.txt" en el directorio raíz de la ruta de acceso especificada.

 

### <a name="cache-path-element"></a>Cache (elemento)

Un elemento de ruta de acceso de *caché* es una variación de un elemento de ruta de acceso del servidor de símbolos.

Este directorio se busca como cualquier otro servidor de símbolos. Sin embargo, si el símbolo no se encuentra aquí y se encuentra en un elemento de ruta de acceso más abajo en la cadena de la ruta de acceso de símbolos, el símbolo se copiará y almacenará en el servidor de símbolos especificado en este elemento.

El controlador de símbolos trata un elemento de ruta de acceso como un elemento de caché si comienza con el texto "cache \* ". Para especificar una caché en "c: \\ caché", use un elemento de ruta de acceso de símbolos de "cache \* c: caché \\ ".

## <a name="example-search-path"></a>Ejemplo de ruta de búsqueda

Para ver cómo funciona esto, establezca esta ruta de acceso de búsqueda.

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

A continuación se muestra una lista de los resultados detallados del controlador de símbolos al buscar ntdll. pdb, mediante la ruta de búsqueda de la lista anterior.

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

Las tres primeras líneas de salida muestran el controlador de símbolos que procesa el primer elemento de la ruta de acceso de `.` . Es un elemento de ruta de acceso estándar.

La cuarta línea muestra el controlador de símbolos mediante el servidor de símbolos para buscar el archivo en el segundo elemento de la ruta de acceso `cache*c:\myCache` que es un elemento de ruta de acceso de la memoria caché.

La quinta línea muestra que el archivo se encuentra en el tercer elemento path de `srv*\\symbols\symbols` , que es un elemento de ruta de acceso del servidor de símbolos.

La sexta línea muestra que el archivo se copia en la memoria caché.

Las dos últimas líneas que el archivo se abre desde la memoria caché.
