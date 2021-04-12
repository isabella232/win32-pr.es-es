---
title: Compilar una actualización del catálogo desde catálogos completos
description: Compilar una actualización del catálogo desde catálogos completos
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player tiendas en línea, compilar catálogos
- tiendas en línea, compilar catálogos
- Escriba 1 tiendas en línea, compilando catálogos
- Windows Media Player tiendas en línea, actualizaciones del catálogo
- tiendas en línea, actualizaciones del catálogo
- tipo 1 almacenes en línea, actualizaciones del catálogo
- Windows Media Player tiendas en línea, catálogos completos
- tiendas en línea, catálogos completos
- tipo 1 tiendas en línea, catálogos completos
- compilar catálogos
- actualizaciones del catálogo
- catálogos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358666"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a><span data-ttu-id="757e2-115">Compilar una actualización del catálogo desde catálogos completos</span><span class="sxs-lookup"><span data-stu-id="757e2-115">Compiling a Catalog Update from Full Catalogs</span></span>

<span data-ttu-id="757e2-116">Una actualización de catálogo que contenga los cambios entre dos versiones de un catálogo compilado se puede crear con la siguiente sintaxis, donde *ruta1* es el directorio que contiene el primer catálogo, *ruta2* es el directorio que contiene el segundo catálogo y, opcionalmente, se puede incluir la depuración para mostrar información de error detallada en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="757e2-116">A catalog update containing the changes between two versions of a compiled catalog can be created by using the syntax below, where *path1* is the directory containing the first catalog, *path2* is the directory containing the second catalog, and debug can be optionally included to display detailed error information on the screen.</span></span> <span data-ttu-id="757e2-117">Los archivos de catálogo deben estar en un formato sin comprimir; el nombre de archivo del catálogo compilado sería Catalog. wmdb, en lugar de Catalog. wmdb. LZ.</span><span class="sxs-lookup"><span data-stu-id="757e2-117">The catalog files must be in uncompressed form—the file name of the compiled catalog would be catalog.wmdb, rather than catalog.wmdb.lz.</span></span>


```C++
catcomp diff <path1> <path2> [debug]
```



<span data-ttu-id="757e2-118">Por ejemplo, si el directorio C: \\ Catalog210 \\ contiene la versión 210 de un catálogo compilado completo y C: \\ Catalog211 contiene la \\ versión 211, el siguiente comando crea un archivo de diferencias que contiene los cambios entre las dos versiones:</span><span class="sxs-lookup"><span data-stu-id="757e2-118">For example, if the C:\\Catalog210\\ directory contains version 210 of a full compiled catalog and C:\\Catalog211\\ contains version 211, the following command creates a difference file that contains the changes between the two versions:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



<span data-ttu-id="757e2-119">Para mostrar información detallada del error, puede Agregar el parámetro de depuración opcional de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="757e2-119">To display detailed error information, you can add the optional debug parameter as follows:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



<span data-ttu-id="757e2-120">Si la compilación se realiza correctamente, catcomp.exe crea los archivos de salida que se enumeran a continuación y los guarda en el directorio que contiene el primer catálogo.</span><span class="sxs-lookup"><span data-stu-id="757e2-120">If compilation is successful, catcomp.exe creates the output files listed below and saves them in the directory that contains the first catalog.</span></span>



| <span data-ttu-id="757e2-121">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="757e2-121">File name</span></span>             | <span data-ttu-id="757e2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="757e2-122">Description</span></span>                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="757e2-123">Catalog. diff</span><span class="sxs-lookup"><span data-stu-id="757e2-123">catalog.diff</span></span>          | <span data-ttu-id="757e2-124">Archivo de diferencias compiladas sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="757e2-124">Uncompressed compiled difference file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="757e2-125">Catalog. diff. LZ</span><span class="sxs-lookup"><span data-stu-id="757e2-125">catalog.diff.lz</span></span>       | <span data-ttu-id="757e2-126">Versión comprimida del archivo de actualización de catálogo.</span><span class="sxs-lookup"><span data-stu-id="757e2-126">Compressed version of catalog update file.</span></span> <span data-ttu-id="757e2-127">El complemento puede proporcionar la ubicación de este archivo a Windows Media Player en [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="757e2-127">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="757e2-128">Catalog. wmdb. Delta</span><span class="sxs-lookup"><span data-stu-id="757e2-128">catalog.wmdb.delta</span></span>    | <span data-ttu-id="757e2-129">Archivo de salida intermedio.</span><span class="sxs-lookup"><span data-stu-id="757e2-129">Intermediate output file.</span></span> <span data-ttu-id="757e2-130">No lo utiliza Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="757e2-130">Not used by Windows Media Player</span></span>                                                                                                                                       |
| <span data-ttu-id="757e2-131">Catalog. wmdb. Modified</span><span class="sxs-lookup"><span data-stu-id="757e2-131">catalog.wmdb.modified</span></span> | <span data-ttu-id="757e2-132">Archivo de salida intermedio.</span><span class="sxs-lookup"><span data-stu-id="757e2-132">Intermediate output file.</span></span> <span data-ttu-id="757e2-133">No lo utiliza Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="757e2-133">Not used by Windows Media Player</span></span>                                                                                                                                       |



 

 

 




