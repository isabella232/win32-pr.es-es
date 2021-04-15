---
title: Aplicar una actualización a un catálogo
description: Aplicar una actualización a un catálogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player tiendas en línea, aplicar actualizaciones a catálogos
- tiendas en línea, aplicar actualizaciones a catálogos
- tipo 1 almacenes en línea, aplicar actualizaciones a catálogos
- Windows Media Player tiendas en línea, actualizar catálogos
- tiendas en línea, actualizar catálogos
- tipo 1 almacenes en línea, actualizar catálogos
- Windows Media Player tiendas en línea, actualizaciones del catálogo
- tiendas en línea, actualizaciones del catálogo
- tipo 1 almacenes en línea, actualizaciones del catálogo
- actualizaciones del catálogo
- actualizar catálogos
- aplicar actualizaciones a catálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695476"
---
# <a name="applying-an-update-to-a-catalog"></a><span data-ttu-id="c59c0-115">Aplicar una actualización a un catálogo</span><span class="sxs-lookup"><span data-stu-id="c59c0-115">Applying an Update To a Catalog</span></span>

> [!Note]  
> <span data-ttu-id="c59c0-116">Normalmente, esto no se hace salvo con fines de diagnóstico, por ejemplo, para ayudar a comprobar que un archivo de diferencias es válido.</span><span class="sxs-lookup"><span data-stu-id="c59c0-116">This is not normally done except for diagnostic purposes—for instance, to help verify that a difference file is valid.</span></span> <span data-ttu-id="c59c0-117">El catálogo generado de esta manera no está en formato comprimido y no se debe pasar a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c59c0-117">The catalog generated in this way is not in compressed form and should not be passed to Windows Media Player.</span></span>

 

<span data-ttu-id="c59c0-118">Se puede crear un nuevo archivo de catálogo mediante la sintaxis siguiente, donde *inputcatalog* es la ubicación del catálogo original y *inputdiff* es la ubicación del archivo de diferencia que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="c59c0-118">A new catalog file can be created by using the syntax below, where *inputcatalog* is the location of the original catalog, and *inputdiff* is the location of the difference file to apply.</span></span> <span data-ttu-id="c59c0-119">Los archivos de catálogo deben estar en un formato sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="c59c0-119">The catalog files must be in uncompressed form.</span></span>


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



<span data-ttu-id="c59c0-120">Por ejemplo, lo siguiente crea un nuevo catálogo a partir de C: \\ Catalog210 \\ Catalog. Wmdb y C: \\ Catalog210 \\ Catalog. diff.</span><span class="sxs-lookup"><span data-stu-id="c59c0-120">For example, the following creates a new catalog from C:\\Catalog210\\catalog.wmdb and C:\\Catalog210\\catalog.diff.</span></span>


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



<span data-ttu-id="c59c0-121">Si la compilación se realiza correctamente, catcomp.exe crea los siguientes archivos de salida.</span><span class="sxs-lookup"><span data-stu-id="c59c0-121">If compilation is successful, catcomp.exe creates the follow output files.</span></span>



| <span data-ttu-id="c59c0-122">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="c59c0-122">File name</span></span>        | <span data-ttu-id="c59c0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="c59c0-123">Description</span></span>       |
|------------------|-------------------|
| <span data-ttu-id="c59c0-124">Catalog. wmdb. New</span><span class="sxs-lookup"><span data-stu-id="c59c0-124">catalog.wmdb.new</span></span> | <span data-ttu-id="c59c0-125">Nuevo archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="c59c0-125">New catalog file.</span></span> |



 

 

 




