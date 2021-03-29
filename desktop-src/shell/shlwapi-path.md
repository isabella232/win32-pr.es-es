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
# <a name="shell-path-handling-functions"></a><span data-ttu-id="a03f3-104">Funciones de control de rutas de Shell</span><span class="sxs-lookup"><span data-stu-id="a03f3-104">Shell Path Handling Functions</span></span>

<span data-ttu-id="a03f3-105">En esta sección se describen las funciones de control de rutas del shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="a03f3-105">This section describes the Windows Shell path handling functions.</span></span> <span data-ttu-id="a03f3-106">Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="a03f3-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a03f3-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a03f3-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a03f3-108">Tema</span><span class="sxs-lookup"><span data-stu-id="a03f3-108">Topic</span></span></th>
<th><span data-ttu-id="a03f3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a03f3-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a03f3-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-111">Agrega una barra diagonal inversa al final de una cadena para crear la sintaxis correcta para una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a03f3-111">Adds a backslash to the end of a string to create the correct syntax for a path.</span></span> <span data-ttu-id="a03f3-112">Si la ruta de acceso de origen ya tiene una barra diagonal inversa al final, no se agregará ninguna barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="a03f3-112">If the source path already has a trailing backslash, no backslash will be added.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a03f3-113">El uso incorrecto de esta función puede provocar una saturación del búfer.</span><span class="sxs-lookup"><span data-stu-id="a03f3-113">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="a03f3-114">Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> más segura en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a03f3-114">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-116">Agrega una extensión de nombre de archivo a una cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a03f3-116">Adds a file name extension to a path string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a03f3-117">El uso incorrecto de esta función puede provocar una saturación del búfer.</span><span class="sxs-lookup"><span data-stu-id="a03f3-117">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="a03f3-118">Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> más segura en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a03f3-118">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-120">Anexa una ruta de acceso al final de otro.</span><span class="sxs-lookup"><span data-stu-id="a03f3-120">Appends one path to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a03f3-121">El uso incorrecto de esta función puede provocar una saturación del búfer.</span><span class="sxs-lookup"><span data-stu-id="a03f3-121">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="a03f3-122">Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> más segura en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a03f3-122">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-124">Crea una ruta de acceso raíz a partir de un número de unidad determinado.</span><span class="sxs-lookup"><span data-stu-id="a03f3-124">Creates a root path from a given drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-126">Simplifica una ruta de acceso quitando elementos de navegación como &quot; . &quot; y &quot; .. &quot; para generar un trazado directo y con formato correcto.</span><span class="sxs-lookup"><span data-stu-id="a03f3-126">Simplifies a path by removing navigation elements such as &quot;.&quot; and &quot;..&quot; to produce a direct, well-formed path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-128">Concatena dos cadenas que representan rutas de acceso con formato correcto en una ruta de acceso; también concatena cualquier elemento de ruta de acceso relativa.</span><span class="sxs-lookup"><span data-stu-id="a03f3-128">Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a03f3-129">El uso incorrecto de esta función puede provocar una saturación del búfer.</span><span class="sxs-lookup"><span data-stu-id="a03f3-129">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="a03f3-130">Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> más segura en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a03f3-130">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-132">Compara dos rutas de acceso para determinar si comparten un prefijo común.</span><span class="sxs-lookup"><span data-stu-id="a03f3-132">Compares two paths to determine if they share a common prefix.</span></span> <span data-ttu-id="a03f3-133">Un prefijo es uno de estos tipos: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="a03f3-133">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-135">Trunca una ruta de acceso de archivo para ajustarse a un ancho de píxel determinado reemplazando los componentes de la ruta de acceso con puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="a03f3-135">Truncates a file path to fit within a given pixel width by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-137">Trunca una ruta de acceso para ajustarse a un determinado número de caracteres reemplazando los componentes de la ruta de acceso con puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="a03f3-137">Truncates a path to fit within a certain number of characters by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-139">Convierte una dirección URL de archivo en una ruta de acceso de Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="a03f3-139">Converts a file URL to a Microsoft MS-DOS path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-141">Crea una ruta de acceso a partir de una dirección URL de archivo.</span><span class="sxs-lookup"><span data-stu-id="a03f3-141">Creates a path from a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-143">Determina si una ruta de acceso a un objeto del sistema de archivos, como un archivo o una carpeta, es válida.</span><span class="sxs-lookup"><span data-stu-id="a03f3-143">Determines whether a path to a file system object such as a file or folder is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-145">Busca una extensión en una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a03f3-145">Searches a path for an extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-147">Busca un nombre de archivo en una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a03f3-147">Searches a path for a file name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-149">Analiza una ruta de acceso y devuelve la parte de esa ruta de acceso que sigue a la primera barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="a03f3-149">Parses a path and returns the portion of that path that follows the first backslash.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-151">Busca un archivo.</span><span class="sxs-lookup"><span data-stu-id="a03f3-151">Searches for a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-153">Determina si un nombre de archivo determinado tiene una lista de sufijos.</span><span class="sxs-lookup"><span data-stu-id="a03f3-153">Determines whether a given file name has one of a list of suffixes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-155">Busca los argumentos de la línea de comandos en una ruta de acceso dada.</span><span class="sxs-lookup"><span data-stu-id="a03f3-155">Finds the command line arguments within a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-157">Determina el tipo de carácter en relación con una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a03f3-157">Determines the type of character in relation to a path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-159">Busca una letra de unidad en el intervalo de la "A" a la "Z" y devuelve el número de unidad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a03f3-159">Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-161">Determina si el tipo de contenido registrado de un archivo coincide con el tipo de contenido especificado.</span><span class="sxs-lookup"><span data-stu-id="a03f3-161">Determines if a file's registered content type matches the specified content type.</span></span> <span data-ttu-id="a03f3-162">Esta función obtiene el tipo de contenido para el tipo de archivo especificado y lo compara con el valor de <em>pszContentType</em>.</span><span class="sxs-lookup"><span data-stu-id="a03f3-162">This function obtains the content type for the specified file type and compares that string with the <em>pszContentType</em>.</span></span> <span data-ttu-id="a03f3-163">La comparación no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a03f3-163">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-165">Comprueba que una ruta de acceso es un directorio válido.</span><span class="sxs-lookup"><span data-stu-id="a03f3-165">Verifies that a path is a valid directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-167">Determina si una ruta de acceso especificada es un directorio vacío.</span><span class="sxs-lookup"><span data-stu-id="a03f3-167">Determines whether a specified path is an empty directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-169">Busca en una ruta de acceso todos los caracteres delimitadores de ruta de acceso (por ejemplo, ': ' o ' \' ).</span><span class="sxs-lookup"><span data-stu-id="a03f3-169">Searches a path for any path-delimiting characters (for example, ':' or '\' ).</span></span> <span data-ttu-id="a03f3-170">Si no hay caracteres que delimiten la ruta de acceso, la ruta de acceso se considera una ruta de acceso de especificación de archivo.</span><span class="sxs-lookup"><span data-stu-id="a03f3-170">If there are no path-delimiting characters present, the path is considered to be a File Spec path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-172">Determina si un archivo es un archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="a03f3-172">Determines if a file is an HTML file.</span></span> <span data-ttu-id="a03f3-173">La determinación se realiza en función del tipo de contenido que se registra para la extensión del archivo.</span><span class="sxs-lookup"><span data-stu-id="a03f3-173">The determination is made based on the content type that is registered for the file's extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-175">Determina si un nombre de archivo está en formato largo.</span><span class="sxs-lookup"><span data-stu-id="a03f3-175">Determines whether a file name is in long format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-177">Determina si una cadena de ruta de acceso representa un recurso de red.</span><span class="sxs-lookup"><span data-stu-id="a03f3-177">Determines whether a path string represents a network resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-179">Busca una ruta de acceso para determinar si contiene un prefijo válido del tipo pasado por <em>pszPrefix</em>.</span><span class="sxs-lookup"><span data-stu-id="a03f3-179">Searches a path to determine if it contains a valid prefix of the type passed by <em>pszPrefix</em>.</span></span> <span data-ttu-id="a03f3-180">Un prefijo es uno de estos tipos: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="a03f3-180">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-182">Busca una ruta de acceso y determina si es relativa.</span><span class="sxs-lookup"><span data-stu-id="a03f3-182">Searches a path and determines if it is relative.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-184">Determina si una cadena de ruta de acceso hace referencia a la raíz de un volumen.</span><span class="sxs-lookup"><span data-stu-id="a03f3-184">Determines whether a path string refers to the root of a volume.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-186">Compara dos rutas de acceso para determinar si tienen un componente raíz común.</span><span class="sxs-lookup"><span data-stu-id="a03f3-186">Compares two paths to determine if they have a common root component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-188">Determina si una carpeta existente contiene los atributos que lo convierten en una carpeta del sistema.</span><span class="sxs-lookup"><span data-stu-id="a03f3-188">Determines if an existing folder contains the attributes that make it a system folder.</span></span> <span data-ttu-id="a03f3-189">Como alternativa, esta función indica si ciertos atributos califican que una carpeta es una carpeta del sistema.</span><span class="sxs-lookup"><span data-stu-id="a03f3-189">Alternately, this function indicates if certain attributes qualify a folder to be a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-191">Determina si una cadena de ruta de acceso es una ruta de acceso UNC (Convención de nomenclatura universal) válida, en lugar de una ruta de acceso basada en una letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="a03f3-191">Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-193">Determina si una cadena es una UNC válida solo para una ruta de acceso de servidor.</span><span class="sxs-lookup"><span data-stu-id="a03f3-193">Determines if a string is a valid UNC for a server path only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-195">Determina si una cadena es una ruta de acceso de recurso compartido UNC válida, un \\ <em></em> \ <em>recurso compartido</em>de servidor.</span><span class="sxs-lookup"><span data-stu-id="a03f3-195">Determines if a string is a valid UNC share path, \\<em>server</em>\<em>share</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-197">Comprueba una cadena determinada para determinar si se ajusta a un formato de dirección URL válido.</span><span class="sxs-lookup"><span data-stu-id="a03f3-197">Tests a given string to determine if it conforms to a valid URL format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-199">Convierte una ruta de acceso todo en mayúsculas a todos los caracteres en minúsculas para dar una apariencia coherente a la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a03f3-199">Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-201">Proporciona a una carpeta existente los atributos adecuados para convertirse en una carpeta del sistema.</span><span class="sxs-lookup"><span data-stu-id="a03f3-201">Gives an existing folder the proper attributes to become a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-203">Busca una cadena mediante un tipo de coincidencia de caracteres comodín de MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="a03f3-203">Searches a string using a MS-DOS wildcard match type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-205">Coincide con un nombre de archivo de una ruta de acceso con uno o más patrones de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="a03f3-205">Matches a file name from a path against one or more file name patterns.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-207">Analiza una cadena de ubicación de archivo que contiene una ubicación de archivo e índice de icono, y devuelve valores distintos.</span><span class="sxs-lookup"><span data-stu-id="a03f3-207">Parses a file location string that contains a file location and icon index, and returns separate values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-209">Busca espacios en una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a03f3-209">Searches a path for spaces.</span></span> <span data-ttu-id="a03f3-210">Si se encuentran espacios, toda la ruta de acceso está entre comillas.</span><span class="sxs-lookup"><span data-stu-id="a03f3-210">If spaces are found, the entire path is enclosed in quotation marks.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-212">Crea una ruta de acceso relativa de un archivo o carpeta a otro.</span><span class="sxs-lookup"><span data-stu-id="a03f3-212">Creates a relative path from one file or folder to another.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-214">Quita todos los argumentos de una ruta de acceso determinada.</span><span class="sxs-lookup"><span data-stu-id="a03f3-214">Removes any arguments from a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-216">Quita la barra diagonal inversa final de una ruta de acceso determinada.</span><span class="sxs-lookup"><span data-stu-id="a03f3-216">Removes the trailing backslash from a given path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a03f3-217">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="a03f3-217">This function is deprecated.</span></span> <span data-ttu-id="a03f3-218">Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> o <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a03f3-218">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-220">Quita todos los espacios iniciales y finales de una cadena.</span><span class="sxs-lookup"><span data-stu-id="a03f3-220">Removes all leading and trailing spaces from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-222">Quita la extensión de nombre de archivo de una ruta de acceso, si está presente.</span><span class="sxs-lookup"><span data-stu-id="a03f3-222">Removes the file name extension from a path, if one is present.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a03f3-223">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="a03f3-223">This function is deprecated.</span></span> <span data-ttu-id="a03f3-224">Se recomienda el uso de <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a03f3-224">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-226">Quita el nombre de archivo final y la barra diagonal inversa de una ruta de acceso, si están presentes.</span><span class="sxs-lookup"><span data-stu-id="a03f3-226">Removes the trailing file name and backslash from a path, if they are present.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a03f3-227">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="a03f3-227">This function is deprecated.</span></span> <span data-ttu-id="a03f3-228">Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a03f3-228">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-230">Reemplaza la extensión de un nombre de archivo por una nueva extensión.</span><span class="sxs-lookup"><span data-stu-id="a03f3-230">Replaces the extension of a file name with a new extension.</span></span> <span data-ttu-id="a03f3-231">Si el nombre de archivo no contiene una extensión, la extensión se adjuntará al final de la cadena.</span><span class="sxs-lookup"><span data-stu-id="a03f3-231">If the file name does not contain an extension, the extension will be attached to the end of the string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a03f3-232">El uso incorrecto de esta función puede provocar una saturación del búfer.</span><span class="sxs-lookup"><span data-stu-id="a03f3-232">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="a03f3-233">Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> más segura en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a03f3-233">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-235">Determina si una ruta de acceso dada tiene un formato correcto y completo.</span><span class="sxs-lookup"><span data-stu-id="a03f3-235">Determines if a given path is correctly formatted and fully qualified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-237">Establece el texto de un control secundario en una ventana o un cuadro de diálogo, usando <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> para asegurarse de que la ruta de acceso quepa en el control.</span><span class="sxs-lookup"><span data-stu-id="a03f3-237">Sets the text of a child control in a window or dialog box, using <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> to ensure the path fits in the control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-239">Recupera un puntero al primer carácter de una ruta de acceso después de los elementos de la letra de unidad o del servidor UNC/ruta de acceso del recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="a03f3-239">Retrieves a pointer to the first character in a path following the drive letter or UNC server/share path elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-241">Quita la parte de la ruta de acceso de un archivo y una ruta de acceso completos.</span><span class="sxs-lookup"><span data-stu-id="a03f3-241">Removes the path portion of a fully qualified path and file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-243">Quita todos los elementos de archivo y directorio de una ruta de acceso excepto la información raíz.</span><span class="sxs-lookup"><span data-stu-id="a03f3-243">Removes all file and directory elements in a path except for the root information.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a03f3-244">El uso incorrecto de esta función puede provocar una saturación del búfer.</span><span class="sxs-lookup"><span data-stu-id="a03f3-244">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="a03f3-245">Se recomienda el uso de la función <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> más segura en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a03f3-245">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-247">Quita la decoración de una cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a03f3-247">Removes the decoration from a path string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-249">Reemplaza algunos nombres de carpeta en una ruta de acceso completa con su cadena de entorno asociada.</span><span class="sxs-lookup"><span data-stu-id="a03f3-249">Replaces certain folder names in a fully qualified path with their associated environment string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-251">Quita los atributos de una carpeta que lo convierten en una carpeta del sistema.</span><span class="sxs-lookup"><span data-stu-id="a03f3-251">Removes the attributes from a folder that make it a system folder.</span></span> <span data-ttu-id="a03f3-252">Esta carpeta debe existir realmente en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a03f3-252">This folder must actually exist in the file system.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-254">Quita las comillas del principio y el final de una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a03f3-254">Removes quotes from the beginning and end of a path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-256">Comprueba un contexto de enlace para ver si es seguro enlazar a un objeto de componente determinado.</span><span class="sxs-lookup"><span data-stu-id="a03f3-256">Checks a bind context to see if it is safe to bind to a particular component object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-258">Determina un esquema para una cadena de dirección URL especificada y devuelve una cadena con un prefijo adecuado.</span><span class="sxs-lookup"><span data-stu-id="a03f3-258">Determines a scheme for a specified URL string, and returns a string with an appropriate prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-260">Convierte una cadena de dirección URL al formato canónico.</span><span class="sxs-lookup"><span data-stu-id="a03f3-260">Converts a URL string into canonical form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-262">Cuando se proporciona con una dirección URL relativa y su base, devuelve una dirección URL en formato canónico.</span><span class="sxs-lookup"><span data-stu-id="a03f3-262">When provided with a relative URL and its base, returns a URL in canonical form.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-264">Crea una comparación que distingue entre mayúsculas y minúsculas de dos cadenas URL.</span><span class="sxs-lookup"><span data-stu-id="a03f3-264">Makes a case-sensitive comparison of two URL strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-266">Convierte una ruta de acceso de MS-DOS en una dirección URL con formato canónico.</span><span class="sxs-lookup"><span data-stu-id="a03f3-266">Converts a MS-DOS path to a canonicalized URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-268">Convierte caracteres o pares suplentes en una dirección URL que podrían modificarse durante el transporte a través de Internet ( &quot; caracteres no seguros &quot; ) en sus secuencias de escape correspondientes.</span><span class="sxs-lookup"><span data-stu-id="a03f3-268">Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet (&quot;unsafe&quot; characters) into their corresponding escape sequences.</span></span> <span data-ttu-id="a03f3-269">Los pares suplentes son caracteres entre U + 10000 y U + 10FFFF (en UTF-32) o entre DC00 y DFFF (en UTF-16).</span><span class="sxs-lookup"><span data-stu-id="a03f3-269">Surrogate pairs are characters between U+10000 to U+10FFFF (in UTF-32) or between DC00 to DFFF (in UTF-16).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-271">Macro que convierte los caracteres de espacio en la secuencia de escape correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a03f3-271">A macro that converts space characters into their corresponding escape sequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-273">Recupera la ubicación de una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="a03f3-273">Retrieves the location from a URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-275">Acepta una cadena de dirección URL y devuelve una parte especificada de esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="a03f3-275">Accepts a URL string and returns a specified part of that URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-277">Aplica un algoritmo hash a una cadena de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="a03f3-277">Hashes a URL string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-279">Comprueba si una dirección URL es un tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="a03f3-279">Tests whether a URL is a specified type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-281">Prueba una dirección URL para determinar si es una dirección URL de archivo.</span><span class="sxs-lookup"><span data-stu-id="a03f3-281">Tests a URL to determine if it is a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-283">Devuelve si una dirección URL es una dirección URL que los exploradores no incluyen normalmente en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="a03f3-283">Returns whether a URL is a URL that browsers typically do not include in navigation history.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-285">Devuelve si una dirección URL es opaca.</span><span class="sxs-lookup"><span data-stu-id="a03f3-285">Returns whether a URL is opaque.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03f3-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-287">Vuelve a convertir las secuencias de escape en caracteres ordinarios.</span><span class="sxs-lookup"><span data-stu-id="a03f3-287">Converts escape sequences back into ordinary characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03f3-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="a03f3-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span></span><br/></td>
<td><span data-ttu-id="a03f3-289">Vuelve a convertir las secuencias de escape en caracteres ordinarios y sobrescribe la cadena original.</span><span class="sxs-lookup"><span data-stu-id="a03f3-289">Converts escape sequences back into ordinary characters and overwrites the original string.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




