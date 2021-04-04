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
# <a name="symbol-paths"></a><span data-ttu-id="bc73e-104">Rutas de acceso de símbolos</span><span class="sxs-lookup"><span data-stu-id="bc73e-104">Symbol Paths</span></span>

<span data-ttu-id="bc73e-105">La biblioteca DbgHelp utiliza la ruta de acceso de búsqueda de símbolos para buscar símbolos de depuración (archivos. PDB y. dbg).</span><span class="sxs-lookup"><span data-stu-id="bc73e-105">The DbgHelp library uses the symbol search path to locate debug symbols (.pdb and .dbg files).</span></span> <span data-ttu-id="bc73e-106">La ruta de búsqueda puede estar formada por uno o varios elementos de la ruta de acceso separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="bc73e-106">The search path can be made up of one or more path elements separated by semicolons.</span></span>

## <a name="specifying-search-paths"></a><span data-ttu-id="bc73e-107">Especificar rutas de acceso de búsqueda</span><span class="sxs-lookup"><span data-stu-id="bc73e-107">Specifying Search Paths</span></span>

<span data-ttu-id="bc73e-108">Para especificar dónde buscará el controlador de símbolos los archivos de símbolos, llame a la función [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="bc73e-108">To specify where the symbol handler will search disk directories for symbol files, call the [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) function.</span></span> <span data-ttu-id="bc73e-109">Como alternativa, puede especificar una ruta de acceso de búsqueda de símbolos en el parámetro *UserSearchPath* de la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="bc73e-109">Alternatively, you can specify a symbol search path in the *UserSearchPath* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

<span data-ttu-id="bc73e-110">El parámetro *UserSearchPath* de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) y el parámetro *SearchPath* en [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) toman un puntero a una cadena terminada en null que especifica una ruta de acceso o una serie de rutas de acceso separadas por un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="bc73e-110">The *UserSearchPath* parameter in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) and the *SearchPath* parameter in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) take a pointer to a null-terminated string that specifies a path, or series of paths separated by a semicolon.</span></span> <span data-ttu-id="bc73e-111">El controlador de símbolos usa estas rutas de acceso para buscar archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bc73e-111">The symbol handler uses these paths to search for symbol files.</span></span> <span data-ttu-id="bc73e-112">Si este parámetro es **null**, el controlador de símbolos busca en el directorio que contiene el módulo para el que se buscan los símbolos.</span><span class="sxs-lookup"><span data-stu-id="bc73e-112">If this parameter is **NULL**, the symbol handler searches the directory that contains the module for which symbols are being searched.</span></span> <span data-ttu-id="bc73e-113">De lo contrario, si este parámetro se especifica como un valor distinto de **null** , el controlador de símbolos busca primero las rutas de acceso establecidas por la aplicación antes de buscar en el directorio del módulo.</span><span class="sxs-lookup"><span data-stu-id="bc73e-113">Otherwise, if this parameter is specified as a non-**NULL** value, the symbol handler first searches the paths set by the application before searching the module directory.</span></span> <span data-ttu-id="bc73e-114">Si establece la \_ ruta de \_ acceso de símbolos NT o la \_ variable de \_ \_ entorno Path de símbolos NT ALT \_ \_ , el controlador de símbolos busca archivos de símbolos en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="bc73e-114">If you set the \_NT\_SYMBOL\_PATH or \_NT\_ALT\_SYMBOL\_PATH environment variable, the symbol handler searches for symbol files in the following order:</span></span>

1. <span data-ttu-id="bc73e-115">\_Variable de \_ entorno de ruta de acceso de símbolos NT \_ .</span><span class="sxs-lookup"><span data-stu-id="bc73e-115">The \_NT\_SYMBOL\_PATH environment variable.</span></span>
2. <span data-ttu-id="bc73e-116">La \_ \_ variable de \_ entorno de ruta de acceso Symbol de NT ALT \_ .</span><span class="sxs-lookup"><span data-stu-id="bc73e-116">The \_NT\_ALT\_SYMBOL\_PATH environment variable.</span></span>
3. <span data-ttu-id="bc73e-117">Directorio que contiene el módulo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bc73e-117">The directory that contains the corresponding module.</span></span>

<span data-ttu-id="bc73e-118">Para recuperar las rutas de acceso de búsqueda, llame a la función [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="bc73e-118">To retrieve the search paths, call the [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) function.</span></span>

<span data-ttu-id="bc73e-119">La ruta de búsqueda de los archivos de base de datos de programa (. pdb) es diferente de la ruta de acceso para los archivos de depuración (. dbg).</span><span class="sxs-lookup"><span data-stu-id="bc73e-119">The search path for program database (.pdb) files is different than the path for debug (.dbg) files.</span></span> <span data-ttu-id="bc73e-120">El algoritmo viene determinado por la funcionalidad de la biblioteca de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bc73e-120">The algorithm is determined by the functionality of the symbol library.</span></span> <span data-ttu-id="bc73e-121">De forma predeterminada, Microsoft Visual C/C++ crea símbolos de formato de Microsoft, los quita de la imagen y los coloca en un archivo. pdb independiente.</span><span class="sxs-lookup"><span data-stu-id="bc73e-121">By default, Microsoft Visual C/C++ creates Microsoft format symbols, strips them from the image, and places them in a separate .pdb file.</span></span> <span data-ttu-id="bc73e-122">Normalmente, el archivo. pdb se ubicará en el directorio que contiene la imagen ejecutable.</span><span class="sxs-lookup"><span data-stu-id="bc73e-122">Typically, the .pdb file will be located in the directory that contains the executable image.</span></span> <span data-ttu-id="bc73e-123">Visual C/C++ incrusta la ruta de acceso absoluta al archivo. pdb en la imagen ejecutable.</span><span class="sxs-lookup"><span data-stu-id="bc73e-123">Visual C/C++ embeds the absolute path to the .pdb file in the executable image.</span></span> <span data-ttu-id="bc73e-124">Si el controlador de símbolos no encuentra el archivo. pdb en esa ubicación o si el archivo. pdb se ha migrado a otro directorio, el controlador de símbolos buscará el archivo. pdb mediante la ruta de acceso de búsqueda descrita para los archivos. dbg.</span><span class="sxs-lookup"><span data-stu-id="bc73e-124">If the symbol handler cannot find the .pdb file in that location or if the .pdb file was moved to another directory, the symbol handler will locate the .pdb file using the search path described for .dbg files.</span></span>

## <a name="path-element-types"></a><span data-ttu-id="bc73e-125">Tipos de elemento de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="bc73e-125">Path Element Types</span></span>

<span data-ttu-id="bc73e-126">Hay tres tipos de elementos de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="bc73e-126">There are three types of path elements.</span></span>

### <a name="standard-path-element"></a><span data-ttu-id="bc73e-127">Elemento path estándar</span><span class="sxs-lookup"><span data-stu-id="bc73e-127">Standard Path Element</span></span>

<span data-ttu-id="bc73e-128">Para buscar un elemento de ruta de acceso estándar, se busca en la raíz del directorio especificado por el elemento path.</span><span class="sxs-lookup"><span data-stu-id="bc73e-128">A standard path element is searched by looking in the root of the directory specified by the path element.</span></span> <span data-ttu-id="bc73e-129">El controlador de símbolos también busca en un subdirectorio de "Symbols" que coincida con la extensión de archivo del módulo que se está buscando en los símbolos.</span><span class="sxs-lookup"><span data-stu-id="bc73e-129">The symbol handler also looks in a subdirectory of "symbols" that matches the file extension of the module that symbols are being looked for.</span></span> <span data-ttu-id="bc73e-130">Suele ser "dll", "exe" o "sys".</span><span class="sxs-lookup"><span data-stu-id="bc73e-130">This is typically "dll", "exe", or "sys".</span></span> <span data-ttu-id="bc73e-131">Por último, busca en un subdirectorio denominado "Symbols" con un directorio con el mismo nombre que la extensión.</span><span class="sxs-lookup"><span data-stu-id="bc73e-131">Lastly, it looks in a subdirectory called "symbols" with a directory of the same name as the extension.</span></span> <span data-ttu-id="bc73e-132">Por ejemplo, si el elemento de ruta de acceso de símbolos es "c: \\ símbolos" y el archivo en el que se buscan los símbolos es "boo.dll", se buscarían los siguientes directorios.</span><span class="sxs-lookup"><span data-stu-id="bc73e-132">For example, if the symbol path element is "c:\\mySymbols" and the file that symbols are being searched for is "boo.dll", then the following directories would be searched.</span></span>

- <span data-ttu-id="bc73e-133">c: \\ símbolos</span><span class="sxs-lookup"><span data-stu-id="bc73e-133">c:\\mySymbols</span></span>  
- <span data-ttu-id="bc73e-134">c: \\ símbolos \\ dll</span><span class="sxs-lookup"><span data-stu-id="bc73e-134">c:\\mySymbols\\dll</span></span>  
- <span data-ttu-id="bc73e-135">c: \\ \\ símbolos dll de símbolos \\</span><span class="sxs-lookup"><span data-stu-id="bc73e-135">c:\\mySymbols\\symbols\\dll</span></span>  

<span data-ttu-id="bc73e-136">El controlador de símbolos usa esta lógica para buscar en cualquier elemento de la ruta de acceso que no cumple los criterios como un *servidor de símbolos* o *caché* (se describe a continuación).</span><span class="sxs-lookup"><span data-stu-id="bc73e-136">The symbol handler uses this logic to search any path element that does not meet the criteria to be a *symbol server* or *cache* (described below).</span></span>

### <a name="symbol-server-path-element"></a><span data-ttu-id="bc73e-137">Elemento path del servidor de símbolos</span><span class="sxs-lookup"><span data-stu-id="bc73e-137">Symbol Server Path Element</span></span>

<span data-ttu-id="bc73e-138">Un elemento de ruta de acceso del *servidor de símbolos* usa una tecnología especial que puede buscar un símbolo que sea una coincidencia exacta del módulo en cuestión.</span><span class="sxs-lookup"><span data-stu-id="bc73e-138">A *symbol server* path element uses special technology that can locate a symbol that is an exact match for the module in question.</span></span> <span data-ttu-id="bc73e-139">Consulte [uso de SymSrv](using-symsrv.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="bc73e-139">See [Using SymSrv](using-symsrv.md) for more details.</span></span>

<span data-ttu-id="bc73e-140">El controlador de símbolos trata un elemento de ruta de acceso como un servidor de símbolos si comienza con el texto "SRV \* ".</span><span class="sxs-lookup"><span data-stu-id="bc73e-140">The symbol handler treats a path element as a symbol server if it begins with the text, "srv\*".</span></span>

> [!Note]  
> <span data-ttu-id="bc73e-141">Si \* no se especifica el texto "SRV" pero el elemento de ruta de acceso real es un almacén del servidor de símbolos, el controlador de símbolos actuará como si \* se hubiera especificado "SRV".</span><span class="sxs-lookup"><span data-stu-id="bc73e-141">If the "srv\*" text is not specified but the actual path element is a symbol server store, then the symbol handler will act as if "srv\*" were specified.</span></span> <span data-ttu-id="bc73e-142">El controlador de símbolos realiza esta determinación buscando la existencia de un archivo llamado "pingme.txt" en el directorio raíz de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="bc73e-142">The symbol handler makes this determination by searching for the existence of a file called "pingme.txt" in the root directory of the specified path.</span></span>

 

### <a name="cache-path-element"></a><span data-ttu-id="bc73e-143">Cache (elemento)</span><span class="sxs-lookup"><span data-stu-id="bc73e-143">Cache Path Element</span></span>

<span data-ttu-id="bc73e-144">Un elemento de ruta de acceso de *caché* es una variación de un elemento de ruta de acceso del servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bc73e-144">A *cache* path element is a variation on a symbol server path element.</span></span>

<span data-ttu-id="bc73e-145">Este directorio se busca como cualquier otro servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bc73e-145">This directory is searched like any other symbol server.</span></span> <span data-ttu-id="bc73e-146">Sin embargo, si el símbolo no se encuentra aquí y se encuentra en un elemento de ruta de acceso más abajo en la cadena de la ruta de acceso de símbolos, el símbolo se copiará y almacenará en el servidor de símbolos especificado en este elemento.</span><span class="sxs-lookup"><span data-stu-id="bc73e-146">However, if the symbol is not found here and it is found in a path element farther down the chain of the symbol path, then the symbol will be copied and stored in the symbol server specified in this element.</span></span>

<span data-ttu-id="bc73e-147">El controlador de símbolos trata un elemento de ruta de acceso como un elemento de caché si comienza con el texto "cache \* ".</span><span class="sxs-lookup"><span data-stu-id="bc73e-147">The symbol handler treats a path element as a cache element if it begins with the text, "cache\*".</span></span> <span data-ttu-id="bc73e-148">Para especificar una caché en "c: \\ caché", use un elemento de ruta de acceso de símbolos de "cache \* c: caché \\ ".</span><span class="sxs-lookup"><span data-stu-id="bc73e-148">To specify a cache in "c:\\myCache", use a symbol path element of "cache\*c:\\myCache".</span></span>

## <a name="example-search-path"></a><span data-ttu-id="bc73e-149">Ejemplo de ruta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="bc73e-149">Example Search Path</span></span>

<span data-ttu-id="bc73e-150">Para ver cómo funciona esto, establezca esta ruta de acceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bc73e-150">To see how this works, set this search path.</span></span>

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

<span data-ttu-id="bc73e-151">A continuación se muestra una lista de los resultados detallados del controlador de símbolos al buscar ntdll. pdb, mediante la ruta de búsqueda de la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="bc73e-151">The following is a listing of the symbol handler's verbose output while searching for ntdll.pdb, using the above listed search path.</span></span>

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

<span data-ttu-id="bc73e-152">Las tres primeras líneas de salida muestran el controlador de símbolos que procesa el primer elemento de la ruta de acceso de `.` .</span><span class="sxs-lookup"><span data-stu-id="bc73e-152">The first three lines of output show the symbol handler processing the first path element of `.`.</span></span> <span data-ttu-id="bc73e-153">Es un elemento de ruta de acceso estándar.</span><span class="sxs-lookup"><span data-stu-id="bc73e-153">This is a standard path element.</span></span>

<span data-ttu-id="bc73e-154">La cuarta línea muestra el controlador de símbolos mediante el servidor de símbolos para buscar el archivo en el segundo elemento de la ruta de acceso `cache*c:\myCache` que es un elemento de ruta de acceso de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bc73e-154">The fourth line shows the symbol handler using the symbol server to look for the file in the second path element of `cache*c:\myCache` which is a cache path element.</span></span>

<span data-ttu-id="bc73e-155">La quinta línea muestra que el archivo se encuentra en el tercer elemento path de `srv*\\symbols\symbols` , que es un elemento de ruta de acceso del servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bc73e-155">The fifth line shows the file is found in the third path element of `srv*\\symbols\symbols`, which is a symbol server path element.</span></span>

<span data-ttu-id="bc73e-156">La sexta línea muestra que el archivo se copia en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bc73e-156">The sixth line shows that the file is copied to the cache.</span></span>

<span data-ttu-id="bc73e-157">Las dos últimas líneas que el archivo se abre desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bc73e-157">The last two lines that the file is opened from the cache.</span></span>
