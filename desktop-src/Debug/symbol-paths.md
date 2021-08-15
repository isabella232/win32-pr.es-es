---
description: La biblioteca DbgHelp usa la ruta de acceso de búsqueda de símbolos para buscar símbolos de depuración (archivos .pdb y .dbg). La ruta de acceso de búsqueda se puede crear con uno o varios elementos de ruta de acceso separados por punto y coma.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Rutas de acceso de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddf01dfbb5aedfcdd2d96cdfd5d4fdd10e6d3f71b5c69024917ddac534d3824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405905"
---
# <a name="symbol-paths"></a>Rutas de acceso de símbolos

La biblioteca DbgHelp usa la ruta de acceso de búsqueda de símbolos para buscar símbolos de depuración (archivos .pdb y .dbg). La ruta de acceso de búsqueda se puede crear con uno o varios elementos de ruta de acceso separados por punto y coma.

## <a name="specifying-search-paths"></a>Especificar rutas de acceso de búsqueda

Para especificar dónde el controlador de símbolos buscará archivos de símbolos en los directorios de disco, llame a la [**función SymSetSearchPath.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) Como alternativa, puede especificar una ruta de acceso de búsqueda de símbolos en el *parámetro UserSearchPath* de la [**función SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)

El *parámetro UserSearchPath* de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) y el parámetro *SearchPath* de [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) toman un puntero a una cadena terminada en NULL que especifica una ruta de acceso o una serie de rutas separadas por un punto y coma. El controlador de símbolos usa estas rutas de acceso para buscar archivos de símbolos. Si este parámetro es **NULL,** el controlador de símbolos busca en el directorio que contiene el módulo para el que se buscan símbolos. De lo contrario, si este parámetro se especifica como un valor distinto de **NULL,** el controlador de símbolos busca primero en las rutas de acceso establecidas por la aplicación antes de buscar en el directorio del módulo. Si establece la variable de entorno NT SYMBOL PATH o NT ALT SYMBOL PATH, el controlador de símbolos busca archivos de \_ símbolos en el orden \_ \_ \_ \_ \_ \_ siguiente:

1. Variable \_ de entorno NT SYMBOL \_ \_ PATH.
2. Variable \_ de entorno NT ALT SYMBOL \_ \_ \_ PATH.
3. Directorio que contiene el módulo correspondiente.

Para recuperar las rutas de acceso de búsqueda, llame a [**la función SymGetSearchPath.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)

La ruta de búsqueda de los archivos de base de datos de programa (.pdb) es diferente de la ruta de acceso para los archivos de depuración (.dbg). El algoritmo viene determinado por la funcionalidad de la biblioteca de símbolos. De forma predeterminada, Microsoft Visual C/C++ crea símbolos de formato de Microsoft, los quita de la imagen y los coloca en un archivo .pdb independiente. Normalmente, el archivo .pdb se ubicará en el directorio que contiene la imagen ejecutable. Visual C/C++ inserta la ruta de acceso absoluta al archivo .pdb en la imagen ejecutable. Si el controlador de símbolos no encuentra el archivo .pdb en esa ubicación o si el archivo .pdb se ha movido a otro directorio, el controlador de símbolos buscará el archivo .pdb mediante la ruta de acceso de búsqueda descrita para los archivos .dbg.

## <a name="path-element-types"></a>Tipos de elemento Path

Hay tres tipos de elementos de ruta de acceso.

### <a name="standard-path-element"></a>Elemento Path estándar

Para buscar un elemento de ruta de acceso estándar, busque en la raíz del directorio especificado por el elemento path. El controlador de símbolos también busca en un subdirectorio de "símbolos" que coincida con la extensión de archivo del módulo que se están buscando símbolos. Suele ser "dll", "exe" o "sys". Por último, busca en un subdirectorio denominado "símbolos" con un directorio con el mismo nombre que la extensión. Por ejemplo, si el elemento de ruta de acceso del símbolo es "c: mySymbols" y el archivo que se buscan los símbolos es "boo.dll", se buscarían los \\ directorios siguientes.

- c: \\ mySymbols  
- c: \\ mySymbols \\ dll  
- c: \\ mySymbols \\ symbols \\ dll  

El controlador de símbolos usa esta lógica para buscar en cualquier elemento de ruta de acceso que no cumpla los criterios para ser un servidor de símbolos o una memoria *caché* (que se describe *a* continuación).

### <a name="symbol-server-path-element"></a>Elemento Symbol Server Path

Un *elemento de ruta de* acceso del servidor de símbolos usa tecnología especial que puede localizar un símbolo que sea una coincidencia exacta para el módulo en cuestión. Consulte [Uso de SymSrv](using-symsrv.md) para obtener más detalles.

El controlador de símbolos trata un elemento de ruta de acceso como un servidor de símbolos si comienza con el texto \* "srv".

> [!Note]  
> Si no se especifica el texto "srv", pero el elemento de ruta de acceso real es un almacén de servidores de símbolos, el controlador de símbolos actuará como si se hubiera especificado \* \* "srv". El controlador de símbolos realiza esta determinación buscando la existencia de un archivo denominado "pingme.txt" en el directorio raíz de la ruta de acceso especificada.

 

### <a name="cache-path-element"></a>Elemento Cache Path

Un *elemento de ruta* de acceso de caché es una variación en un elemento de ruta de acceso del servidor de símbolos.

Este directorio se busca como cualquier otro servidor de símbolos. Sin embargo, si el símbolo no se encuentra aquí y se encuentra en un elemento de ruta de acceso más abajo en la cadena de la ruta de acceso del símbolo, el símbolo se copiará y almacenará en el servidor de símbolos especificado en este elemento.

El controlador de símbolos trata un elemento de ruta de acceso como un elemento de caché si comienza con el texto \* "cache". Para especificar una caché en "c: myCache", use un elemento de ruta de acceso de símbolos \\ de "cache \* c: \\ myCache".

## <a name="example-search-path"></a>Ruta de acceso de búsqueda de ejemplo

Para ver cómo funciona, establezca esta ruta de búsqueda.

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

A continuación se muestra una lista de la salida detallada del controlador de símbolos al buscar ntdll.pdb, mediante la ruta de acceso de búsqueda indicada anteriormente.

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

Las tres primeras líneas de salida muestran el controlador de símbolos que procesa el primer elemento de ruta de acceso de `.` . Se trata de un elemento de ruta de acceso estándar.

La cuarta línea muestra el controlador de símbolos que usa el servidor de símbolos para buscar el archivo en el segundo elemento path del que es un elemento de ruta `cache*c:\myCache` de acceso de caché.

La quinta línea muestra que el archivo se encuentra en el tercer elemento path de `srv*\\symbols\symbols` , que es un elemento de ruta de acceso del servidor de símbolos.

La sexta línea muestra que el archivo se copia en la memoria caché.

Las dos últimas líneas que abre el archivo desde la memoria caché.
