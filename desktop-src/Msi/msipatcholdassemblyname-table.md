---
description: La tabla MsiPatchOldAssemblyName especifica el nombre anterior de un ensamblado.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Tabla MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361068"
---
# <a name="msipatcholdassemblyname-table"></a><span data-ttu-id="2f6fd-103">Tabla MsiPatchOldAssemblyName</span><span class="sxs-lookup"><span data-stu-id="2f6fd-103">MsiPatchOldAssemblyName Table</span></span>

<span data-ttu-id="2f6fd-104">La tabla MsiPatchOldAssemblyName especifica el nombre anterior de un ensamblado.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-104">The MsiPatchOldAssemblyName table specifies the old name for an assembly.</span></span>

<span data-ttu-id="2f6fd-105">La tabla MsiPatchOldAssemblyName tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-105">The MsiPatchOldAssemblyName table has the following columns.</span></span>



| <span data-ttu-id="2f6fd-106">Columna</span><span class="sxs-lookup"><span data-stu-id="2f6fd-106">Column</span></span>   | <span data-ttu-id="2f6fd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f6fd-107">Type</span></span>                         | <span data-ttu-id="2f6fd-108">Clave</span><span class="sxs-lookup"><span data-stu-id="2f6fd-108">Key</span></span> | <span data-ttu-id="2f6fd-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="2f6fd-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="2f6fd-110">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="2f6fd-110">Assembly</span></span> | [<span data-ttu-id="2f6fd-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="2f6fd-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="2f6fd-112">Y</span><span class="sxs-lookup"><span data-stu-id="2f6fd-112">Y</span></span>   | <span data-ttu-id="2f6fd-113">N</span><span class="sxs-lookup"><span data-stu-id="2f6fd-113">N</span></span>        |
| <span data-ttu-id="2f6fd-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="2f6fd-114">Name</span></span>     | [<span data-ttu-id="2f6fd-115">Texto</span><span class="sxs-lookup"><span data-stu-id="2f6fd-115">Text</span></span>](text.md)             | <span data-ttu-id="2f6fd-116">Y</span><span class="sxs-lookup"><span data-stu-id="2f6fd-116">Y</span></span>   | <span data-ttu-id="2f6fd-117">N</span><span class="sxs-lookup"><span data-stu-id="2f6fd-117">N</span></span>        |
| <span data-ttu-id="2f6fd-118">Value</span><span class="sxs-lookup"><span data-stu-id="2f6fd-118">Value</span></span>    | [<span data-ttu-id="2f6fd-119">Texto</span><span class="sxs-lookup"><span data-stu-id="2f6fd-119">Text</span></span>](text.md)             | <span data-ttu-id="2f6fd-120">N</span><span class="sxs-lookup"><span data-stu-id="2f6fd-120">N</span></span>   | <span data-ttu-id="2f6fd-121">N</span><span class="sxs-lookup"><span data-stu-id="2f6fd-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2f6fd-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="2f6fd-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2f6fd-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembl</span><span class="sxs-lookup"><span data-stu-id="2f6fd-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembly</span></span>
</dt> <dd>

<span data-ttu-id="2f6fd-124">Identificador único del nombre del ensamblado antiguo.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-124">Unique identifier for the old assembly name.</span></span> <span data-ttu-id="2f6fd-125">Esta clave se usa como una asignación entre esta y la [tabla MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).</span><span class="sxs-lookup"><span data-stu-id="2f6fd-125">This key is used as a mapping between this and the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f6fd-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="2f6fd-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="2f6fd-127">Nombre del atributo asociado con el valor especificado en la columna valor.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-127">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="2f6fd-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="2f6fd-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="2f6fd-129">Valor asociado al nombre especificado en la columna nombre.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-129">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f6fd-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f6fd-130">Remarks</span></span>

<span data-ttu-id="2f6fd-131">Windows Installer usa la tabla [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla MsiPatchOldAssemblyName al aplicar revisiones a los ensamblados instalados en la caché de ensamblados global (GAC).</span><span class="sxs-lookup"><span data-stu-id="2f6fd-131">Windows Installer uses the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="2f6fd-132">Al liberar una versión más reciente de un ensamblado, se cambia el nombre seguro del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-132">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="2f6fd-133">Las dos tablas juntas identifican el nombre anterior del ensamblado de un ensamblado actualizado.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-133">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="2f6fd-134">Esto permite al instalador usar el nombre de ensamblado anterior para buscar el archivo original en la GAC y aplicar una revisión binaria.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-134">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="2f6fd-135">Sin esta información, es posible que el instalador tenga que obtener acceso al origen de instalación original con el fin de aplicar una revisión a un ensamblado instalado en la GAC.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-135">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="2f6fd-136">[PatchWiz](patchwiz-dll.md)no genera automáticamente la tabla [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla MsiPatchOldAssemblyName.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-136">The [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="2f6fd-137">El paquete de actualización especificado en la [tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md) debe contener estas tablas para que la revisión tenga esta información.</span><span class="sxs-lookup"><span data-stu-id="2f6fd-137">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="2f6fd-138">Validación</span><span class="sxs-lookup"><span data-stu-id="2f6fd-138">Validation</span></span>

<dl>

[<span data-ttu-id="2f6fd-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="2f6fd-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2f6fd-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="2f6fd-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2f6fd-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="2f6fd-141">ICE32</span></span>](ice32.md)  
</dl>

 

 



