---
description: La tabla PatchSequence se usa para generar la tabla MsiPatchSequence en una revisión. La tabla requiere la versión de PATCHWIZ.DLL que está disponible con Windows Installer&\# 160; 3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Tabla PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913465"
---
# <a name="patchsequence-table-patchwizdll"></a><span data-ttu-id="683d7-104">Tabla PatchSequence (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="683d7-104">PatchSequence Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="683d7-105">La tabla PatchSequence se usa para generar la [tabla MsiPatchSequence](msipatchsequence-table.md) en una revisión.</span><span class="sxs-lookup"><span data-stu-id="683d7-105">The PatchSequence Table is used to generate the [MsiPatchSequence Table](msipatchsequence-table.md) in a patch.</span></span> <span data-ttu-id="683d7-106">La tabla requiere la versión de [PATCHWIZ.DLL](patchwiz-dll.md) que está disponible con Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="683d7-106">The table requires the version of [PATCHWIZ.DLL](patchwiz-dll.md) that is available with Windows Installer 3.0.</span></span>

<span data-ttu-id="683d7-107">En la tabla siguiente se identifican las columnas de la tabla PatchSequence.</span><span class="sxs-lookup"><span data-stu-id="683d7-107">The following table identifies the columns of the PatchSequence Table.</span></span>



| <span data-ttu-id="683d7-108">Columna</span><span class="sxs-lookup"><span data-stu-id="683d7-108">Column</span></span>      | <span data-ttu-id="683d7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="683d7-109">Type</span></span>       | <span data-ttu-id="683d7-110">Clave</span><span class="sxs-lookup"><span data-stu-id="683d7-110">Key</span></span> | <span data-ttu-id="683d7-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="683d7-111">Nullable</span></span> |
|-------------|------------|-----|----------|
| <span data-ttu-id="683d7-112">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="683d7-112">PatchFamily</span></span> | <span data-ttu-id="683d7-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="683d7-113">Identifier</span></span> | <span data-ttu-id="683d7-114">Y</span><span class="sxs-lookup"><span data-stu-id="683d7-114">Y</span></span>   | <span data-ttu-id="683d7-115">N</span><span class="sxs-lookup"><span data-stu-id="683d7-115">N</span></span>        |
| <span data-ttu-id="683d7-116">Destino</span><span class="sxs-lookup"><span data-stu-id="683d7-116">Target</span></span>      | <span data-ttu-id="683d7-117">Texto</span><span class="sxs-lookup"><span data-stu-id="683d7-117">Text</span></span>       | <span data-ttu-id="683d7-118">Y</span><span class="sxs-lookup"><span data-stu-id="683d7-118">Y</span></span>   | <span data-ttu-id="683d7-119">Y</span><span class="sxs-lookup"><span data-stu-id="683d7-119">Y</span></span>        |
| <span data-ttu-id="683d7-120">Secuencia</span><span class="sxs-lookup"><span data-stu-id="683d7-120">Sequence</span></span>    | <span data-ttu-id="683d7-121">Versión</span><span class="sxs-lookup"><span data-stu-id="683d7-121">Version</span></span>    |     | <span data-ttu-id="683d7-122">Y</span><span class="sxs-lookup"><span data-stu-id="683d7-122">Y</span></span>        |
| <span data-ttu-id="683d7-123">Sustituir</span><span class="sxs-lookup"><span data-stu-id="683d7-123">Supersede</span></span>   | <span data-ttu-id="683d7-124">Entero</span><span class="sxs-lookup"><span data-stu-id="683d7-124">Integer</span></span>    |     | <span data-ttu-id="683d7-125">Y</span><span class="sxs-lookup"><span data-stu-id="683d7-125">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="683d7-126">Columnas</span><span class="sxs-lookup"><span data-stu-id="683d7-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="683d7-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="683d7-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="683d7-128">El identificador que indica las familias de secuencias a las que pertenece esta revisión.</span><span class="sxs-lookup"><span data-stu-id="683d7-128">The identifier that indicates the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="683d7-129">Los valores de las columnas target y PatchFamily definen conjuntamente la clave principal de la tabla.</span><span class="sxs-lookup"><span data-stu-id="683d7-129">The values in the Target and PatchFamily columns together define the primary key for the table.</span></span> <span data-ttu-id="683d7-130">Una revisión que pertenece a varias familias de secuencias, o tiene secuencias diferentes según el código de producto del destino, puede tener una fila por cada emparejamiento.</span><span class="sxs-lookup"><span data-stu-id="683d7-130">A patch that belongs to multiple sequence families, or has different sequences depending on the product code of the target, can have one row for each pairing.</span></span> <span data-ttu-id="683d7-131">Este valor se usa para rellenar la columna PatchFamily de la [tabla MsiPatchSequence](msipatchsequence-table.md) que pertenece a la revisión.</span><span class="sxs-lookup"><span data-stu-id="683d7-131">This value is used to populate the PatchFamily column of the [MsiPatchSequence Table](msipatchsequence-table.md) that belongs to the patch.</span></span>

</dd> <dt>

<span data-ttu-id="683d7-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Dirigir</span><span class="sxs-lookup"><span data-stu-id="683d7-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="683d7-133">La columna de destino se usa para filtrar el PatchFamily por el código de producto.</span><span class="sxs-lookup"><span data-stu-id="683d7-133">The Target column is used to filter the PatchFamily by product code.</span></span>

<span data-ttu-id="683d7-134">Un valor NULL en esta columna indica que este PatchFamily se aplica a todos los destinos de la revisión.</span><span class="sxs-lookup"><span data-stu-id="683d7-134">A NULL value in this column indicates that this PatchFamily applies to all targets of the patch.</span></span> <span data-ttu-id="683d7-135">Si esta columna contiene una clave externa para la [tabla TargetImages](targetimages-table-patchwiz-dll-.md), el código de producto de la imagen especificada se recupera y se usa para rellenar el valor del código de producto en la fila de la nueva revisión de la [tabla MsiPatchSequence](msipatchsequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="683d7-135">If this column contains a foreign key to the [TargetImages Table](targetimages-table-patchwiz-dll-.md), the product code of the specified image is retrieved and used to populate the product code value in the new patch's row of the [MsiPatchSequence Table](msipatchsequence-table.md).</span></span> <span data-ttu-id="683d7-136">Si esta columna contiene un GUID, el GUID se usa para rellenar el valor de código de producto de la fila en la tabla MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="683d7-136">If this column contains a GUID, the GUID is used to populate the product code value of the row in the MsiPatchSequence Table.</span></span>

</dd> <dt>

<span data-ttu-id="683d7-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="683d7-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="683d7-138">El valor de la columna Sequence se usa para rellenar la columna Sequence de la [tabla MsiPatchSequence](msipatchsequence-table.md) del nuevo archivo de revisión.</span><span class="sxs-lookup"><span data-stu-id="683d7-138">The value in the Sequence column is used to populate the Sequence column of the [MsiPatchSequence Table](msipatchsequence-table.md) of the new patch file.</span></span>

<span data-ttu-id="683d7-139">Si el valor es NULL, se genera automáticamente un número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="683d7-139">If the value is NULL, a sequence number is generated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="683d7-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Sustituir</span><span class="sxs-lookup"><span data-stu-id="683d7-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Supersede</span></span>
</dt> <dd>

<span data-ttu-id="683d7-141">Un valor de **msidbPatchSequenceSupersedeEarlier** o 1 en este campo indica que esta revisión sustituye a [las actualizaciones pequeñas](small-updates.md) anteriores de las familias de secuencias a las que pertenece esta revisión.</span><span class="sxs-lookup"><span data-stu-id="683d7-141">A value of **msidbPatchSequenceSupersedeEarlier** or 1 in this field indicates that this patch supersedes earlier [small updates](small-updates.md) in the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="683d7-142">El valor de esta columna se utiliza para establecer la columna de atributos de la fila de la nueva revisión en la [tabla MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="683d7-142">The value in this column is used to set the Attributes column of the new patch's row in the [MsiPatchSequence Table](msipatchsequence-table.md) .</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="683d7-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="683d7-143">Remarks</span></span>

<span data-ttu-id="683d7-144">Disponible a partir de Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="683d7-144">Available beginning in Windows Installer 3.0.</span></span>

 

 



