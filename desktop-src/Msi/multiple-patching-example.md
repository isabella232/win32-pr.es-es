---
description: En el ejemplo siguiente se muestra cómo se pueden usar Windows Installer 3,0 y versiones posteriores para aplicar revisiones en el orden en que se crearon.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Ejemplo de varias revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677657"
---
# <a name="multiple-patching-example"></a><span data-ttu-id="e50aa-103">Ejemplo de varias revisiones</span><span class="sxs-lookup"><span data-stu-id="e50aa-103">Multiple Patching Example</span></span>

<span data-ttu-id="e50aa-104">En el ejemplo siguiente se muestra cómo se pueden usar Windows Installer 3,0 y versiones posteriores para aplicar revisiones en el orden en que se crearon.</span><span class="sxs-lookup"><span data-stu-id="e50aa-104">The following example shows how Windows Installer 3.0 and later can be used to apply patches in the order in which they are authored.</span></span>

## <a name="example"></a><span data-ttu-id="e50aa-105">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e50aa-105">Example</span></span>

<span data-ttu-id="e50aa-106">En este ejemplo hay tres revisiones, QFE1, QFE2 y ServicePack1, y cada una tiene una tabla [MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e50aa-106">In this example there are three patches, QFE1, QFE2, and ServicePack1, and they each have a [MsiPatchSequence](msipatchsequence-table.md) table.</span></span> <span data-ttu-id="e50aa-107">Estas revisiones se han creado para aplicarse a la versión 1,0 de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e50aa-107">These patches have been authored to be applied to version 1.0 of the application.</span></span>



| <span data-ttu-id="e50aa-108">Nombre de revisión</span><span class="sxs-lookup"><span data-stu-id="e50aa-108">Patch Name</span></span>   | <span data-ttu-id="e50aa-109">Tipo de revisión</span><span class="sxs-lookup"><span data-stu-id="e50aa-109">Patch Type</span></span>    | <span data-ttu-id="e50aa-110">Sequence Number</span><span class="sxs-lookup"><span data-stu-id="e50aa-110">Sequence Number</span></span> |
|--------------|---------------|-----------------|
| <span data-ttu-id="e50aa-111">QFE1</span><span class="sxs-lookup"><span data-stu-id="e50aa-111">QFE1</span></span>         | <span data-ttu-id="e50aa-112">Actualización pequeña</span><span class="sxs-lookup"><span data-stu-id="e50aa-112">Small Update</span></span>  | <span data-ttu-id="e50aa-113">1.1.0</span><span class="sxs-lookup"><span data-stu-id="e50aa-113">1.1.0</span></span>           |
| <span data-ttu-id="e50aa-114">QFE2</span><span class="sxs-lookup"><span data-stu-id="e50aa-114">QFE2</span></span>         | <span data-ttu-id="e50aa-115">Actualización pequeña</span><span class="sxs-lookup"><span data-stu-id="e50aa-115">Small Update</span></span>  | <span data-ttu-id="e50aa-116">1.2.0</span><span class="sxs-lookup"><span data-stu-id="e50aa-116">1.2.0</span></span>           |
| <span data-ttu-id="e50aa-117">ServicePack1</span><span class="sxs-lookup"><span data-stu-id="e50aa-117">ServicePack1</span></span> | <span data-ttu-id="e50aa-118">Actualización secundaria</span><span class="sxs-lookup"><span data-stu-id="e50aa-118">Minor Upgrade</span></span> | <span data-ttu-id="e50aa-119">1.3.0</span><span class="sxs-lookup"><span data-stu-id="e50aa-119">1.3.0</span></span>           |



 

<span data-ttu-id="e50aa-120">La tabla [MsiPatchSequence](msipatchsequence-table.md) de cada revisión solo tiene un registro que contiene la familia de revisiones, el código de producto y el número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="e50aa-120">The [MsiPatchSequence](msipatchsequence-table.md) table of each patch has only one record that contains the patch family, product code, and sequence number.</span></span> <span data-ttu-id="e50aa-121">Las tres revisiones se aplican al mismo producto y pertenecen a la misma familia de revisiones, denominada AppPatch.</span><span class="sxs-lookup"><span data-stu-id="e50aa-121">The three patches are all applied to the same product and belong to the same patch family, named AppPatch.</span></span> <span data-ttu-id="e50aa-122">Ninguno de los parches tiene el atributo **msidbPatchSequenceSupersedeEarlier** .</span><span class="sxs-lookup"><span data-stu-id="e50aa-122">None of the patches have the **msidbPatchSequenceSupersedeEarlier** attribute.</span></span>

<span data-ttu-id="e50aa-123">[Tabla MsiPatchSequence](msipatchsequence-table.md) para la [actualización pequeña](small-updates.md)de QFE1.</span><span class="sxs-lookup"><span data-stu-id="e50aa-123">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE1 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="e50aa-124">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="e50aa-124">PatchFamily</span></span> | <span data-ttu-id="e50aa-125">ProductCode</span><span class="sxs-lookup"><span data-stu-id="e50aa-125">ProductCode</span></span>                            | <span data-ttu-id="e50aa-126">Secuencia</span><span class="sxs-lookup"><span data-stu-id="e50aa-126">Sequence</span></span> | <span data-ttu-id="e50aa-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="e50aa-127">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="e50aa-128">AppPatch</span><span class="sxs-lookup"><span data-stu-id="e50aa-128">AppPatch</span></span>    | <span data-ttu-id="e50aa-129">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="e50aa-129">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="e50aa-130">1.1.0</span><span class="sxs-lookup"><span data-stu-id="e50aa-130">1.1.0</span></span>    |            |



 

<span data-ttu-id="e50aa-131">[Tabla MsiPatchSequence](msipatchsequence-table.md) para la [actualización pequeña](small-updates.md)de QFE2.</span><span class="sxs-lookup"><span data-stu-id="e50aa-131">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE2 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="e50aa-132">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="e50aa-132">PatchFamily</span></span> | <span data-ttu-id="e50aa-133">ProductCode</span><span class="sxs-lookup"><span data-stu-id="e50aa-133">ProductCode</span></span>                            | <span data-ttu-id="e50aa-134">Secuencia</span><span class="sxs-lookup"><span data-stu-id="e50aa-134">Sequence</span></span> | <span data-ttu-id="e50aa-135">Atributos</span><span class="sxs-lookup"><span data-stu-id="e50aa-135">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="e50aa-136">AppPatch</span><span class="sxs-lookup"><span data-stu-id="e50aa-136">AppPatch</span></span>    | <span data-ttu-id="e50aa-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="e50aa-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="e50aa-138">1.2.0</span><span class="sxs-lookup"><span data-stu-id="e50aa-138">1.2.0</span></span>    |            |



 

<span data-ttu-id="e50aa-139">[Tabla MsiPatchSequence](msipatchsequence-table.md) para la [actualización secundaria](minor-upgrades.md)de ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="e50aa-139">[MsiPatchSequence Table](msipatchsequence-table.md) for ServicePack1 [minor upgrade](minor-upgrades.md).</span></span> 

| <span data-ttu-id="e50aa-140">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="e50aa-140">PatchFamily</span></span> | <span data-ttu-id="e50aa-141">ProductCode</span><span class="sxs-lookup"><span data-stu-id="e50aa-141">ProductCode</span></span>                            | <span data-ttu-id="e50aa-142">Secuencia</span><span class="sxs-lookup"><span data-stu-id="e50aa-142">Sequence</span></span> | <span data-ttu-id="e50aa-143">Atributos</span><span class="sxs-lookup"><span data-stu-id="e50aa-143">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="e50aa-144">AppPatch</span><span class="sxs-lookup"><span data-stu-id="e50aa-144">AppPatch</span></span>    | <span data-ttu-id="e50aa-145">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="e50aa-145">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="e50aa-146">1.3.0</span><span class="sxs-lookup"><span data-stu-id="e50aa-146">1.3.0</span></span>    |            |



 

<span data-ttu-id="e50aa-147">Si un usuario instala la versión 1,0 del producto y, a continuación, aplica QFE2 y, en una fecha posterior, decide aplicar QFE1, Windows Installer garantiza que la secuencia efectiva de la aplicación de revisión en el producto se aplica con anterioridad a QFE2.</span><span class="sxs-lookup"><span data-stu-id="e50aa-147">If a user installs version 1.0 of the product, and then applies QFE2, and then at a later date decides to apply QFE1, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 applied ahead of QFE2.</span></span> <span data-ttu-id="e50aa-148">Si el usuario aplica ServicePack1 y, a continuación, aplica QFE2 y QFE1 en una fecha posterior, Windows Installer garantiza que la secuencia efectiva de la aplicación de revisión en el producto se QFE1 por encima de QFE2 y por encima de ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="e50aa-148">If the user applies ServicePack1, then applies QFE2 and QFE1 together at a later date, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 ahead of QFE2 and ahead of ServicePack1.</span></span>

<span data-ttu-id="e50aa-149">Si ServicePack1 tiene **msidbPatchSequenceSupersedeEarlier** establecido en la columna Attributes de su tabla [MsiPatchSequence](msipatchsequence-table.md) , significa que el Service Pack contiene todos los cambios en QFE1 y QFE2.</span><span class="sxs-lookup"><span data-stu-id="e50aa-149">If ServicePack1 has **msidbPatchSequenceSupersedeEarlier** set in the Attributes column of its [MsiPatchSequence](msipatchsequence-table.md) table, this means that the service pack contains all the changes in QFE1 and QFE2.</span></span> <span data-ttu-id="e50aa-150">En este caso, QFE1 y QFE2 no se aplican cuando se aplica ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="e50aa-150">In this case, QFE1 and QFE2 are not applied when ServicePack1 is applied.</span></span>

<span data-ttu-id="e50aa-151">**Windows Installer 2,0:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="e50aa-151">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="e50aa-152">Las versiones anteriores a Windows Installer 3,0 solo pueden instalar una revisión por transacción y las revisiones se aplican en la secuencia en la que se proporcionan.</span><span class="sxs-lookup"><span data-stu-id="e50aa-152">Versions earlier than Windows Installer 3.0 can install only one patch per transaction and patches are applied in the sequence that they are provided.</span></span> <span data-ttu-id="e50aa-153">En el ejemplo anterior, si se aplica primero QFE2 y, a continuación, se aplica QFE1, es decir, dos transacciones y las revisiones se aplican a la versión 1,0 de la aplicación en la secuencia QFE2 seguida de QFE1.</span><span class="sxs-lookup"><span data-stu-id="e50aa-153">For the preceding example, if QFE2 is applied first and then QFE1 is applied, that is two transactions and the patches are applied to version 1.0 of the application in the sequence QFE2 followed by QFE1.</span></span> <span data-ttu-id="e50aa-154">Si se aplica primero ServicePack1, QFE1 o QFE2 no se pueden aplicar en una transacción posterior porque ServicePack1 es una actualización secundaria que cambia la versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e50aa-154">If ServicePack1 is applied first, then QFE1 or QFE2 cannot be applied in a later transaction because ServicePack1 is a minor upgrade that changes the application version.</span></span> <span data-ttu-id="e50aa-155">QFE1 y QFE2 solo se pueden aplicar a la versión 1,0 de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e50aa-155">QFE1 and QFE2 can only be applied to version 1.0 of the application.</span></span>

 

 



