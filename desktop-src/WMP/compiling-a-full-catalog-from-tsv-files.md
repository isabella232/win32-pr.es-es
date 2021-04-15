---
title: Compilación de un catálogo completo a partir de archivos TSV
description: Compilación de un catálogo completo a partir de archivos TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player tiendas en línea, compilar catálogos
- tiendas en línea, compilar catálogos
- Escriba 1 tiendas en línea, compilando catálogos
- Windows Media Player tiendas en línea, archivos TSV
- tiendas en línea, archivos TSV
- tipo 1 tiendas en línea, archivos TSV
- Windows Media Player tiendas en línea, catcomp.exe
- tiendas en línea, catcomp.exe
- Escriba 1 tiendas en línea, catcomp.exe
- catcomp.exe
- compilar catálogos
- archivos de valores separados por tabulaciones (TSV)
- Archivos TSV (con valores separados por tabuladores)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695530"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a><span data-ttu-id="a85bf-116">Compilación de un catálogo completo a partir de archivos TSV</span><span class="sxs-lookup"><span data-stu-id="a85bf-116">Compiling a Full Catalog from TSV Files</span></span>

<span data-ttu-id="a85bf-117">Los nuevos catálogos se crean a partir de un conjunto de archivos de valores separados por tabulaciones (TSV).</span><span class="sxs-lookup"><span data-stu-id="a85bf-117">New catalogs are created from a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="a85bf-118">Los archivos deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a85bf-118">The files must be in Unicode format.</span></span> <span data-ttu-id="a85bf-119">Coloque los archivos TSV necesarios que se enumeran a continuación en una carpeta (el argumento de ruta de acceso de entrada para catcomp.exe) y llame a catcomp.exe con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="a85bf-119">Place the required TSV files listed below into a folder (the input path argument to catcomp.exe), and call catcomp.exe using the following syntax:</span></span>


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



<span data-ttu-id="a85bf-120">Si no se proporciona un número de versión, el número de versión se establecerá en 0.</span><span class="sxs-lookup"><span data-stu-id="a85bf-120">If a version number is not provided, the version number will be set to 0.</span></span> <span data-ttu-id="a85bf-121">Si no se proporciona ningún identificador de configuración regional, se utiliza la configuración regional del sistema.</span><span class="sxs-lookup"><span data-stu-id="a85bf-121">If no locale ID is provided, the system locale is used.</span></span> <span data-ttu-id="a85bf-122">Si solo se proporciona un argumento opcional numérico, se supone que es el número de versión.</span><span class="sxs-lookup"><span data-stu-id="a85bf-122">If only one numeric optional argument is provided, it is assumed to be the version number.</span></span> <span data-ttu-id="a85bf-123">Si se especifica debug, la salida en la pantalla proporcionará información de diagnóstico más detallada.</span><span class="sxs-lookup"><span data-stu-id="a85bf-123">If debug is specified, the output to the screen will provide more detailed diagnostic information.</span></span>

<span data-ttu-id="a85bf-124">Por ejemplo, a continuación se compilará un catálogo a partir de los archivos de C: \\ CatalogData \\ 210 y se asignará al catálogo un número de versión de 210:</span><span class="sxs-lookup"><span data-stu-id="a85bf-124">For example, the following will compile a catalog from the files in C:\\CatalogData\\210 and give the catalog a version number of 210:</span></span>


```C++
catcomp C:\CatalogData\210 210
```



<span data-ttu-id="a85bf-125">Para mostrar mensajes de error más detallados, se puede Agregar el argumento opcional debug, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="a85bf-125">To display more detailed error messages, the optional debug argument can be added, as follows:</span></span>


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a><span data-ttu-id="a85bf-126">Archivos TSV necesarios</span><span class="sxs-lookup"><span data-stu-id="a85bf-126">Required TSV Files</span></span>

<span data-ttu-id="a85bf-127">Cada uno de los siguientes archivos debe estar presente, pero se puede usar un archivo vacío si no hay datos para un archivo.</span><span class="sxs-lookup"><span data-stu-id="a85bf-127">Each of the following files must be present, but an empty file can be used if there is no data for a file.</span></span> <span data-ttu-id="a85bf-128">Por ejemplo, si el catálogo no contiene ningún canal de radio, radio.csv puede estar vacío.</span><span class="sxs-lookup"><span data-stu-id="a85bf-128">For instance, if your catalog contains no radio channels, radio.csv can be empty.</span></span> <span data-ttu-id="a85bf-129">Los archivos se deben denominar exactamente como se muestra.</span><span class="sxs-lookup"><span data-stu-id="a85bf-129">The files must be named exactly as listed.</span></span>

[<span data-ttu-id="a85bf-130">track.csv</span><span class="sxs-lookup"><span data-stu-id="a85bf-130">track.csv</span></span>](track-csv.md)

[<span data-ttu-id="a85bf-131">album.csv</span><span class="sxs-lookup"><span data-stu-id="a85bf-131">album.csv</span></span>](album-csv.md)

[<span data-ttu-id="a85bf-132">artist.csv</span><span class="sxs-lookup"><span data-stu-id="a85bf-132">artist.csv</span></span>](artist-csv.md)

[<span data-ttu-id="a85bf-133">genre.csv</span><span class="sxs-lookup"><span data-stu-id="a85bf-133">genre.csv</span></span>](genre-csv.md)

[<span data-ttu-id="a85bf-134">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="a85bf-134">subgenre.csv</span></span>](subgenre-csv.md)

[<span data-ttu-id="a85bf-135">list.csv</span><span class="sxs-lookup"><span data-stu-id="a85bf-135">list.csv</span></span>](list-csv.md)

[<span data-ttu-id="a85bf-136">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="a85bf-136">listitem.csv</span></span>](listitem-csv.md)

[<span data-ttu-id="a85bf-137">radio.csv</span><span class="sxs-lookup"><span data-stu-id="a85bf-137">radio.csv</span></span>](radio-csv.md)

> [!Note]  
> <span data-ttu-id="a85bf-138">Aunque los nombres de archivo deben tener extensiones. csv, los archivos no están en formato de valores separados por comas (CSV).</span><span class="sxs-lookup"><span data-stu-id="a85bf-138">Although the file names must have .csv extensions, the files are not in Comma Separated Values (CSV) format.</span></span> <span data-ttu-id="a85bf-139">Los archivos deben estar en formato de valores separados por tabulaciones (TSV).</span><span class="sxs-lookup"><span data-stu-id="a85bf-139">The files must be in Tab Separated Values (TSV) format.</span></span>

 

<span data-ttu-id="a85bf-140">Si la compilación se realiza correctamente, catcomp.exe crea tres archivos de salida.</span><span class="sxs-lookup"><span data-stu-id="a85bf-140">If compilation is successful, catcomp.exe creates three output files.</span></span>



| <span data-ttu-id="a85bf-141">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="a85bf-141">File name</span></span>                   | <span data-ttu-id="a85bf-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="a85bf-142">Description</span></span>                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a85bf-143">Catalog. wmdb</span><span class="sxs-lookup"><span data-stu-id="a85bf-143">catalog.wmdb</span></span>                | <span data-ttu-id="a85bf-144">Catálogo compilado no comprimido.</span><span class="sxs-lookup"><span data-stu-id="a85bf-144">Uncompressed compiled catalog.</span></span>                                                                                                                                                      |
| <span data-ttu-id="a85bf-145">Catalog. wmdb. LZ</span><span class="sxs-lookup"><span data-stu-id="a85bf-145">catalog.wmdb.lz</span></span>             | <span data-ttu-id="a85bf-146">Catalogar en formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="a85bf-146">Catalog in compressed format.</span></span> <span data-ttu-id="a85bf-147">El complemento puede proporcionar la ubicación de este archivo a Windows Media Player en [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="a85bf-147">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="a85bf-148">\_words.txt únicos compilados \_</span><span class="sxs-lookup"><span data-stu-id="a85bf-148">compiled\_unique\_words.txt</span></span> | <span data-ttu-id="a85bf-149">Un archivo de salida intermedio.</span><span class="sxs-lookup"><span data-stu-id="a85bf-149">An intermediate output file.</span></span> <span data-ttu-id="a85bf-150">No lo usa Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a85bf-150">Not used by Windows Media Player.</span></span>                                                                                                                      |



 

 

 




