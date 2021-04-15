---
description: La tabla MsiPatchSequence contiene toda la información que el instalador necesita para determinar la secuencia de aplicación de una revisión de actualización pequeña en relación con todas las demás revisiones.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Tabla MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669804"
---
# <a name="msipatchsequence-table"></a><span data-ttu-id="cba48-103">Tabla MsiPatchSequence</span><span class="sxs-lookup"><span data-stu-id="cba48-103">MsiPatchSequence Table</span></span>

<span data-ttu-id="cba48-104">La tabla MsiPatchSequence contiene toda la información que el instalador necesita para determinar la secuencia de aplicación de una revisión de [actualización pequeña](small-updates.md) en relación con todas las demás revisiones.</span><span class="sxs-lookup"><span data-stu-id="cba48-104">The MsiPatchSequence table contains all the information the installer requires to determine the sequence of application of a [small update](small-updates.md) patch relative to all other patches.</span></span> <span data-ttu-id="cba48-105">La tabla debe estar en la base de datos del archivo de revisión y no en una transformación de la revisión.</span><span class="sxs-lookup"><span data-stu-id="cba48-105">The table must be in the database of the patch file and not in a transform in the patch.</span></span> <span data-ttu-id="cba48-106">El instalador omite esta tabla al aplicar una revisión de [actualización principal](major-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="cba48-106">The installer ignores this table when applying a [major upgrade](major-upgrades.md) patch.</span></span> <span data-ttu-id="cba48-107">Al aplicar una revisión de [actualización secundaria](minor-upgrades.md) , el instalador solo usa esta tabla para identificar las revisiones reemplazadas que no se deben secuenciar.</span><span class="sxs-lookup"><span data-stu-id="cba48-107">When applying a [minor upgrade](minor-upgrades.md) patch, the installer only uses this table to identify superseded patches that must not be sequenced.</span></span>

<span data-ttu-id="cba48-108">La **tabla MsiPatchSequence** tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="cba48-108">The **MsiPatchSequence table** has the following columns.</span></span>



| <span data-ttu-id="cba48-109">Columna</span><span class="sxs-lookup"><span data-stu-id="cba48-109">Column</span></span>      | <span data-ttu-id="cba48-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="cba48-110">Type</span></span>                         | <span data-ttu-id="cba48-111">Clave</span><span class="sxs-lookup"><span data-stu-id="cba48-111">Key</span></span> | <span data-ttu-id="cba48-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="cba48-112">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="cba48-113">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="cba48-113">PatchFamily</span></span> | [<span data-ttu-id="cba48-114">Identificador</span><span class="sxs-lookup"><span data-stu-id="cba48-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="cba48-115">Y</span><span class="sxs-lookup"><span data-stu-id="cba48-115">Y</span></span>   | <span data-ttu-id="cba48-116">N</span><span class="sxs-lookup"><span data-stu-id="cba48-116">N</span></span>        |
| <span data-ttu-id="cba48-117">ProductCode</span><span class="sxs-lookup"><span data-stu-id="cba48-117">ProductCode</span></span> | [<span data-ttu-id="cba48-118">GUID</span><span class="sxs-lookup"><span data-stu-id="cba48-118">GUID</span></span>](guid.md)             | <span data-ttu-id="cba48-119">Y</span><span class="sxs-lookup"><span data-stu-id="cba48-119">Y</span></span>   | <span data-ttu-id="cba48-120">Y</span><span class="sxs-lookup"><span data-stu-id="cba48-120">Y</span></span>        |
| <span data-ttu-id="cba48-121">Secuencia</span><span class="sxs-lookup"><span data-stu-id="cba48-121">Sequence</span></span>    | [<span data-ttu-id="cba48-122">Versión</span><span class="sxs-lookup"><span data-stu-id="cba48-122">Version</span></span>](version.md)       | <span data-ttu-id="cba48-123">N</span><span class="sxs-lookup"><span data-stu-id="cba48-123">N</span></span>   | <span data-ttu-id="cba48-124">N</span><span class="sxs-lookup"><span data-stu-id="cba48-124">N</span></span>        |
| <span data-ttu-id="cba48-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="cba48-125">Attributes</span></span>  | [<span data-ttu-id="cba48-126">Entero</span><span class="sxs-lookup"><span data-stu-id="cba48-126">Integer</span></span>](integer.md)       | <span data-ttu-id="cba48-127">N</span><span class="sxs-lookup"><span data-stu-id="cba48-127">N</span></span>   | <span data-ttu-id="cba48-128">Y</span><span class="sxs-lookup"><span data-stu-id="cba48-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cba48-129">Columnas</span><span class="sxs-lookup"><span data-stu-id="cba48-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cba48-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="cba48-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="cba48-131">Especifica que la revisión es miembro de la familia de revisiones mencionada en este campo.</span><span class="sxs-lookup"><span data-stu-id="cba48-131">Specifies that the patch is a member of the patch family named in this field.</span></span> <span data-ttu-id="cba48-132">Las revisiones de la misma familia de revisiones que tienen como destino la misma versión de producto se ordenan por los valores de la columna de secuencia.</span><span class="sxs-lookup"><span data-stu-id="cba48-132">Patches in the same patch family that target the same product version are sorted by the values in the Sequence column.</span></span> <span data-ttu-id="cba48-133">Las revisiones de la familia Patch se aplican al producto de destino en el orden de secuencia creciente.</span><span class="sxs-lookup"><span data-stu-id="cba48-133">The patches within the patch family are applied to the target product in the order of increasing sequence.</span></span> <span data-ttu-id="cba48-134">El PatchFamily también se usa para determinar qué revisiones se van a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="cba48-134">The PatchFamily is also used to determine which patches are to be superseded.</span></span> <span data-ttu-id="cba48-135">Una revisión puede aparecer en varias filas y pertenecer a varias familias de revisiones si se aplica a más de un producto o incluye varias correcciones.</span><span class="sxs-lookup"><span data-stu-id="cba48-135">A patch may be listed in multiple rows and belong to multiple patch families if it applies to more than one product or includes multiple fixes.</span></span>

<span data-ttu-id="cba48-136">El Windows Installer no interpreta el valor de PatchFamily de forma que no sea una comparación de igualdad con respecto a otros valores de PatchFamily.</span><span class="sxs-lookup"><span data-stu-id="cba48-136">The Windows Installer does not interpret the PatchFamily value in any way other than comparisons for equality against other PatchFamily values.</span></span> <span data-ttu-id="cba48-137">Un valor de PatchFamily debe ser único en la ProductCode de destino del conjunto de revisiones.</span><span class="sxs-lookup"><span data-stu-id="cba48-137">A PatchFamily value must be unique within the ProductCode targeted by the set of patches.</span></span> <span data-ttu-id="cba48-138">En los escenarios de revisión complejos, es posible que el identificador PatchFamily tenga que ser único globalmente.</span><span class="sxs-lookup"><span data-stu-id="cba48-138">In the complex patching scenarios the PatchFamily identifier may need to be globally unique.</span></span>

</dd> <dt>

<span data-ttu-id="cba48-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span><span class="sxs-lookup"><span data-stu-id="cba48-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span></span>
</dt> <dd>

<span data-ttu-id="cba48-140">Un valor de este campo es opcional.</span><span class="sxs-lookup"><span data-stu-id="cba48-140">A value in this field is optional.</span></span> <span data-ttu-id="cba48-141">Si se especifica un GUID de [código de producto](product-codes.md) en este campo y la revisión se está aplicando al producto especificado, la revisión se ordenará y se aplicará como miembro del PatchFamily especificado.</span><span class="sxs-lookup"><span data-stu-id="cba48-141">If a [product code](product-codes.md) GUID is entered in this field and the patch is being applied to the specified product, the patch is sorted and applied as a member of the specified PatchFamily.</span></span> <span data-ttu-id="cba48-142">Si se especifica un GUID de código de producto en este campo y la revisión no se aplica al producto especificado por ProductCode, se omite esta fila.</span><span class="sxs-lookup"><span data-stu-id="cba48-142">If a product code GUID is entered in this field and the patch is not being applied to the product specified by ProductCode, this row is ignored.</span></span> <span data-ttu-id="cba48-143">Si el valor de ProductCode es NULL, la revisión se ordena y se aplica como miembro de PatchFamily para todos los destinos de la revisión, independientemente del código de producto.</span><span class="sxs-lookup"><span data-stu-id="cba48-143">If the value in ProductCode is NULL, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

<span data-ttu-id="cba48-144">Una revisión puede tener varias filas en el mismo PatchFamily y un ProductCode diferente para cada producto de destino de la revisión.</span><span class="sxs-lookup"><span data-stu-id="cba48-144">A patch can have multiple rows in the same PatchFamily and a different ProductCode for each product targeted by the patch.</span></span> <span data-ttu-id="cba48-145">Una fila para PatchFamily puede especificar NULL para ProductCode.</span><span class="sxs-lookup"><span data-stu-id="cba48-145">One row for the PatchFamily can specify NULL for ProductCode.</span></span> <span data-ttu-id="cba48-146">Si el producto de destino coincide con una fila con un valor ProductCode que no es NULL, el instalador usa la fila coincidente y omite la fila con el valor ProductCode nulo.</span><span class="sxs-lookup"><span data-stu-id="cba48-146">If the target product matches a row with a non-NULL ProductCode, the installer uses the matching row and ignores the row with the NULL ProductCode.</span></span> <span data-ttu-id="cba48-147">Si ninguno de los códigos de producto especificados coincide con el destino, la revisión se ordena y se aplica como miembro de PatchFamily para todos los destinos de la revisión, independientemente del código de producto.</span><span class="sxs-lookup"><span data-stu-id="cba48-147">If none of the specified product codes match the target, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

</dd> <dt>

<span data-ttu-id="cba48-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="cba48-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="cba48-149">El valor de la columna Sequence especifica la secuencia de esta revisión en el PatchFamily especificado.</span><span class="sxs-lookup"><span data-stu-id="cba48-149">The value in the Sequence column specifies the sequence of this patch within the specified PatchFamily.</span></span> <span data-ttu-id="cba48-150">El valor de Sequence se expresa en el formato de los datos de la [versión](version.md) .</span><span class="sxs-lookup"><span data-stu-id="cba48-150">The value in Sequence is expressed in the format of [Version](version.md) data.</span></span> <span data-ttu-id="cba48-151">El valor contiene entre 1 y 4 campos y cada campo tiene un intervalo de 0 a 65535.</span><span class="sxs-lookup"><span data-stu-id="cba48-151">The value contains between 1 and 4 fields and each field has a range of 0 to 65535.</span></span> <span data-ttu-id="cba48-152">Los miembros de PatchFamily se ordenan y se aplican al producto de destino en el orden en que los valores de secuencia aumentan.</span><span class="sxs-lookup"><span data-stu-id="cba48-152">Members of PatchFamily are sorted and applied to the target product in the order of increasing Sequence values.</span></span> <span data-ttu-id="cba48-153">Por ejemplo, los seis valores siguientes aumentan: 1, 1,1, 1,2, 2,01, 2.01.1, 2.01.1.1.</span><span class="sxs-lookup"><span data-stu-id="cba48-153">For example, the following six values are increasing: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.</span></span>

</dd> <dt>

<span data-ttu-id="cba48-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus</span><span class="sxs-lookup"><span data-stu-id="cba48-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="cba48-155">La presencia del atributo **msidbPatchSequenceSupersedeEarlier** en una fila indica que la revisión de [actualización pequeña](small-updates.md) sustituye las actualizaciones proporcionadas por todas las revisiones con valores de secuencia inferiores en el mismo PatchFamily.</span><span class="sxs-lookup"><span data-stu-id="cba48-155">The presence of the **msidbPatchSequenceSupersedeEarlier** attribute in a row indicates that the [small update](small-updates.md) patch supersedes the updates provided by all patches with lesser Sequence values in the same PatchFamily.</span></span> <span data-ttu-id="cba48-156">Esta revisión contiene todas las revisiones proporcionadas por las revisiones anteriores en el PatchFamily especificado.</span><span class="sxs-lookup"><span data-stu-id="cba48-156">This patch contains all fixes provided by earlier patches in the specified PatchFamily.</span></span> <span data-ttu-id="cba48-157">Este atributo no significa que esta revisión sustituya a las revisiones anteriores en todos los casos, ya que las revisiones anteriores pueden pertenecer a varias familias de revisiones.</span><span class="sxs-lookup"><span data-stu-id="cba48-157">This attribute does not mean that this patch supersedes the earlier patches in all cases because the earlier patches can belong to multiple patch families.</span></span>

<span data-ttu-id="cba48-158">Una revisión de [actualización pequeña](small-updates.md) no puede sustituir una [actualización secundaria](minor-upgrades.md) o una revisión de [actualización importante](major-upgrades.md) en cualquier circunstancia, incluso si se establece **msidbPatchSequenceSupersedeEarlier** .</span><span class="sxs-lookup"><span data-stu-id="cba48-158">A [small update](small-updates.md) patch cannot supersede a [minor upgrade](minor-upgrades.md) or [major upgrade](major-upgrades.md) patch under any circumstances, even if the **msidbPatchSequenceSupersedeEarlier** is set.</span></span> 

| <span data-ttu-id="cba48-159">Nombre</span><span class="sxs-lookup"><span data-stu-id="cba48-159">Name</span></span>                                   | <span data-ttu-id="cba48-160">Value</span><span class="sxs-lookup"><span data-stu-id="cba48-160">Value</span></span> | <span data-ttu-id="cba48-161">Significado</span><span class="sxs-lookup"><span data-stu-id="cba48-161">Meaning</span></span>                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | <span data-ttu-id="cba48-162">0x00</span><span class="sxs-lookup"><span data-stu-id="cba48-162">0x00</span></span>  | <span data-ttu-id="cba48-163">Indica un valor de secuenciación simple.</span><span class="sxs-lookup"><span data-stu-id="cba48-163">Indicates a simple sequencing value.</span></span>                              |
| <span data-ttu-id="cba48-164">**msidbPatchSequenceSupersedeEarlier**</span><span class="sxs-lookup"><span data-stu-id="cba48-164">**msidbPatchSequenceSupersedeEarlier**</span></span> | <span data-ttu-id="cba48-165">0x01</span><span class="sxs-lookup"><span data-stu-id="cba48-165">0x01</span></span>  | <span data-ttu-id="cba48-166">Indica una revisión que sustituye a las revisiones anteriores de esta familia.</span><span class="sxs-lookup"><span data-stu-id="cba48-166">Indicates a patch that supersedes earlier patches in this family.</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="cba48-167">Validación</span><span class="sxs-lookup"><span data-stu-id="cba48-167">Validation</span></span>

<dl>

[<span data-ttu-id="cba48-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="cba48-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cba48-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="cba48-169">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="cba48-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cba48-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cba48-171">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="cba48-171">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



