---
description: Durante una instalación Windows Installer, el instalador puede buscar un directorio y un archivo en ese directorio.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Buscar un directorio y un archivo en el directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667665"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a><span data-ttu-id="f88cd-103">Buscar un directorio y un archivo en el directorio</span><span class="sxs-lookup"><span data-stu-id="f88cd-103">Searching for a Directory and a File in the Directory</span></span>

<span data-ttu-id="f88cd-104">**Para buscar un directorio y, a continuación, un archivo en ese directorio**</span><span class="sxs-lookup"><span data-stu-id="f88cd-104">**To search for a directory and then a file in that directory**</span></span>

1.  <span data-ttu-id="f88cd-105">Primera búsqueda del directorio.</span><span class="sxs-lookup"><span data-stu-id="f88cd-105">First search for the directory.</span></span>

    <span data-ttu-id="f88cd-106">AppDir debe definirse como la firma válida del directorio.</span><span class="sxs-lookup"><span data-stu-id="f88cd-106">AppDir must be defined as the valid signature of the directory.</span></span> <span data-ttu-id="f88cd-107">Si AppDir no está definido como una firma válida, AppSearch no tiene un lugar donde encontrar el archivo; por ejemplo, si la búsqueda es para c: \\ MyDir \\MyApp.exe, AppDir debe definirse como c: \\ MyDir.</span><span class="sxs-lookup"><span data-stu-id="f88cd-107">If AppDir is not defined as a valid signature, AppSearch does not have a place to find the file, for example, if the search is for c:\\MyDir\\MyApp.exe, AppDir should be defined as c:\\MyDir.</span></span> <span data-ttu-id="f88cd-108">AppDir se puede definir mediante la inclusión de un registro en la [tabla DrLocator](drlocator-table.md)o de algún otro método.</span><span class="sxs-lookup"><span data-stu-id="f88cd-108">AppDir might be defined by including a record in the [DrLocator Table](drlocator-table.md), or by some other method.</span></span> <span data-ttu-id="f88cd-109">No se incluye ningún registro en la [tabla de firma](signature-table.md) de la búsqueda de directorio.</span><span class="sxs-lookup"><span data-stu-id="f88cd-109">No record is included in the [Signature Table](signature-table.md) for the directory search.</span></span> <span data-ttu-id="f88cd-110">En la búsqueda de archivos, muestre la firma y el nombre del archivo en la tabla de firmas.</span><span class="sxs-lookup"><span data-stu-id="f88cd-110">For the file search, list the file signature and name in the Signature Table.</span></span> <span data-ttu-id="f88cd-111">Los campos restantes de este registro pueden ser null para buscar cualquier versión de MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="f88cd-111">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="f88cd-112">[Tabla de firmas](signature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="f88cd-112">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="f88cd-113">Firma</span><span class="sxs-lookup"><span data-stu-id="f88cd-113">Signature</span></span>          | <span data-ttu-id="f88cd-114">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="f88cd-114">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="f88cd-115">AppFile</span><span class="sxs-lookup"><span data-stu-id="f88cd-115">AppFile</span></span><br/> | <span data-ttu-id="f88cd-116">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="f88cd-116">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="f88cd-117">Use la [tabla AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="f88cd-117">Use the [AppSearch Table](appsearch-table.md).</span></span>

    <span data-ttu-id="f88cd-118">Escriba la propiedad que va a establecer el instalador si el directorio con la firma AppDir está instalado.</span><span class="sxs-lookup"><span data-stu-id="f88cd-118">Enter the property that the Installer is to set if the directory with the signature AppDir is installed.</span></span> <span data-ttu-id="f88cd-119">Si el instalador encuentra que este directorio está instalado, establece MYDIR en la ruta de acceso del directorio.</span><span class="sxs-lookup"><span data-stu-id="f88cd-119">If the Installer finds this directory is installed, it sets MYDIR to the directory path.</span></span> <span data-ttu-id="f88cd-120">Escriba la propiedad que el instalador va a establecer si MyApp.exe está instalado.</span><span class="sxs-lookup"><span data-stu-id="f88cd-120">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="f88cd-121">[Tabla AppSearch](appsearch-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="f88cd-121">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="f88cd-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f88cd-122">Property</span></span>         | <span data-ttu-id="f88cd-123">Firma</span><span class="sxs-lookup"><span data-stu-id="f88cd-123">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="f88cd-124">MYDIR</span><span class="sxs-lookup"><span data-stu-id="f88cd-124">MYDIR</span></span><br/> | <span data-ttu-id="f88cd-125">AppDir</span><span class="sxs-lookup"><span data-stu-id="f88cd-125">AppDir</span></span><br/>  |
    | <span data-ttu-id="f88cd-126">MYAPP</span><span class="sxs-lookup"><span data-stu-id="f88cd-126">MYAPP</span></span><br/> | <span data-ttu-id="f88cd-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="f88cd-127">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="f88cd-128">Use la [tabla DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="f88cd-128">Use the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="f88cd-129">Escriba en la columna primaria la firma, AppDir, que se define como la ruta de acceso del directorio.</span><span class="sxs-lookup"><span data-stu-id="f88cd-129">Enter in the Parent column the signature, AppDir, that is defined as the path of the directory.</span></span> <span data-ttu-id="f88cd-130">Especifique en la columna profundidad el número de niveles de subdirectorio que se buscarán en este directorio.</span><span class="sxs-lookup"><span data-stu-id="f88cd-130">Specify in the Depth column the number of subdirectory levels to search in this directory.</span></span> <span data-ttu-id="f88cd-131">AppDir debe definirse como la firma del directorio.</span><span class="sxs-lookup"><span data-stu-id="f88cd-131">AppDir must be defined as the directory signature.</span></span> <span data-ttu-id="f88cd-132">AppDir se puede definir mediante la inclusión de un registro como se muestra aquí o mediante otro método.</span><span class="sxs-lookup"><span data-stu-id="f88cd-132">AppDir may be defined by including a record as shown here or by another method.</span></span>

    [<span data-ttu-id="f88cd-133">Tabla DrLocator</span><span class="sxs-lookup"><span data-stu-id="f88cd-133">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="f88cd-134">Firma</span><span class="sxs-lookup"><span data-stu-id="f88cd-134">Signature</span></span> | <span data-ttu-id="f88cd-135">Parent</span><span class="sxs-lookup"><span data-stu-id="f88cd-135">Parent</span></span> | <span data-ttu-id="f88cd-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="f88cd-136">Path</span></span>      | <span data-ttu-id="f88cd-137">Profundidad</span><span class="sxs-lookup"><span data-stu-id="f88cd-137">Depth</span></span> |
    |-----------|--------|-----------|-------|
    | <span data-ttu-id="f88cd-138">AppDir</span><span class="sxs-lookup"><span data-stu-id="f88cd-138">AppDir</span></span>    |        | <span data-ttu-id="f88cd-139">C: \\ MyDir</span><span class="sxs-lookup"><span data-stu-id="f88cd-139">C:\\MyDir</span></span> | <span data-ttu-id="f88cd-140">0</span><span class="sxs-lookup"><span data-stu-id="f88cd-140">0</span></span>     |
    | <span data-ttu-id="f88cd-141">AppFile</span><span class="sxs-lookup"><span data-stu-id="f88cd-141">AppFile</span></span>   | <span data-ttu-id="f88cd-142">AppDir</span><span class="sxs-lookup"><span data-stu-id="f88cd-142">AppDir</span></span> |           | <span data-ttu-id="f88cd-143">0</span><span class="sxs-lookup"><span data-stu-id="f88cd-143">0</span></span>     |

    

     

4.  <span data-ttu-id="f88cd-144">Incluya la acción AppSearch en la secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="f88cd-144">Include the AppSearch action in the action sequence.</span></span>

    <span data-ttu-id="f88cd-145">Si se encuentra MyApp.exe está instalado en AppDir, el instalador establece la propiedad MYAPP en la ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="f88cd-145">If MyApp.exe is found to be installed in AppDir, the Installer sets the property MYAPP to the location of file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f88cd-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f88cd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f88cd-147">Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes</span><span class="sxs-lookup"><span data-stu-id="f88cd-147">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




