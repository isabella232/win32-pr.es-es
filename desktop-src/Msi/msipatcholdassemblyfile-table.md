---
description: La tabla MsiPatchOldAssemblyFile relaciona un archivo de la tabla de archivos con un nombre de ensamblado de la tabla MsiPatchOldAssemblyName. Se pueden asociar varios nombres de ensamblado anteriores a un único archivo.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Tabla MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669845"
---
# <a name="msipatcholdassemblyfile-table"></a><span data-ttu-id="97ad5-104">Tabla MsiPatchOldAssemblyFile</span><span class="sxs-lookup"><span data-stu-id="97ad5-104">MsiPatchOldAssemblyFile Table</span></span>

<span data-ttu-id="97ad5-105">La tabla MsiPatchOldAssemblyFile relaciona un archivo de la tabla de [archivos](file-table.md) con un nombre de ensamblado de la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md).</span><span class="sxs-lookup"><span data-stu-id="97ad5-105">The MsiPatchOldAssemblyFile table relates a file in the [File table](file-table.md) to an assembly name in the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md).</span></span> <span data-ttu-id="97ad5-106">Se pueden asociar varios nombres de ensamblado anteriores a un único archivo.</span><span class="sxs-lookup"><span data-stu-id="97ad5-106">Multiple old assembly names can be associated with a single file.</span></span>

<span data-ttu-id="97ad5-107">La tabla MsiPatchOldAssemblyFile tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="97ad5-107">The MsiPatchOldAssemblyFile table has the following columns.</span></span>



| <span data-ttu-id="97ad5-108">Columna</span><span class="sxs-lookup"><span data-stu-id="97ad5-108">Column</span></span>     | <span data-ttu-id="97ad5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="97ad5-109">Type</span></span>                         | <span data-ttu-id="97ad5-110">Clave</span><span class="sxs-lookup"><span data-stu-id="97ad5-110">Key</span></span> | <span data-ttu-id="97ad5-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="97ad5-111">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="97ad5-112">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="97ad5-112">File\_</span></span>     | [<span data-ttu-id="97ad5-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="97ad5-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="97ad5-114">Y</span><span class="sxs-lookup"><span data-stu-id="97ad5-114">Y</span></span>   | <span data-ttu-id="97ad5-115">N</span><span class="sxs-lookup"><span data-stu-id="97ad5-115">N</span></span>        |
| <span data-ttu-id="97ad5-116">Assembl\_</span><span class="sxs-lookup"><span data-stu-id="97ad5-116">Assembly\_</span></span> | [<span data-ttu-id="97ad5-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="97ad5-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="97ad5-118">Y</span><span class="sxs-lookup"><span data-stu-id="97ad5-118">Y</span></span>   | <span data-ttu-id="97ad5-119">N</span><span class="sxs-lookup"><span data-stu-id="97ad5-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="97ad5-120">Columnas</span><span class="sxs-lookup"><span data-stu-id="97ad5-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="97ad5-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="97ad5-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="97ad5-122">Clave externa de la [tabla de archivos](file-table.md) que especifica el ensamblado que se va a revisar.</span><span class="sxs-lookup"><span data-stu-id="97ad5-122">Foreign key to the [File table](file-table.md) that specifies the assembly to be patched.</span></span> <span data-ttu-id="97ad5-123">Esta columna forma parte de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="97ad5-123">This column is part of the primary key.</span></span>

</dd> <dt>

<span data-ttu-id="97ad5-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembl\_</span><span class="sxs-lookup"><span data-stu-id="97ad5-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembly\_</span></span>
</dt> <dd>

<span data-ttu-id="97ad5-125">Clave externa de la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) que identifica uno de los nombres de ensamblado anteriores para el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="97ad5-125">Foreign key to the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) that identifies one of the old assembly names for the assembly.</span></span> <span data-ttu-id="97ad5-126">Esta columna forma parte de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="97ad5-126">This column is part of the primary key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97ad5-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97ad5-127">Remarks</span></span>

<span data-ttu-id="97ad5-128">Windows Installer usa la tabla MsiPatchOldAssemblyFile y la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) al aplicar revisiones a los ensamblados instalados en la caché de ensamblados global (GAC).</span><span class="sxs-lookup"><span data-stu-id="97ad5-128">Windows Installer uses the MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="97ad5-129">Al liberar una versión más reciente de un ensamblado, se cambia el nombre seguro del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="97ad5-129">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="97ad5-130">Las dos tablas juntas identifican el nombre anterior del ensamblado de un ensamblado actualizado.</span><span class="sxs-lookup"><span data-stu-id="97ad5-130">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="97ad5-131">Esto permite al instalador usar el nombre de ensamblado anterior para buscar el archivo original en la GAC y aplicar una revisión binaria.</span><span class="sxs-lookup"><span data-stu-id="97ad5-131">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="97ad5-132">Sin esta información, es posible que el instalador tenga que obtener acceso al origen de instalación original con el fin de aplicar una revisión a un ensamblado instalado en la GAC.</span><span class="sxs-lookup"><span data-stu-id="97ad5-132">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="97ad5-133">[PatchWiz](patchwiz-dll.md)no genera automáticamente la tabla MsiPatchOldAssemblyFile y la [tabla MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) .</span><span class="sxs-lookup"><span data-stu-id="97ad5-133">The MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="97ad5-134">El paquete de actualización especificado en la [tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md) debe contener estas tablas para que la revisión tenga esta información.</span><span class="sxs-lookup"><span data-stu-id="97ad5-134">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="97ad5-135">Validación</span><span class="sxs-lookup"><span data-stu-id="97ad5-135">Validation</span></span>

<dl>

[<span data-ttu-id="97ad5-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="97ad5-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="97ad5-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="97ad5-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="97ad5-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="97ad5-138">ICE32</span></span>](ice32.md)  
</dl>

 

 



