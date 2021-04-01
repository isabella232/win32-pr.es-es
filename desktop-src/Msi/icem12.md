---
description: ICEM12 comprueba que en una tabla ModuleSequence, las acciones estándar tienen números de secuencia y acciones personalizadas tienen valores de BaseAction y after.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082260"
---
# <a name="icem12"></a><span data-ttu-id="33bbf-103">ICEM12</span><span class="sxs-lookup"><span data-stu-id="33bbf-103">ICEM12</span></span>

<span data-ttu-id="33bbf-104">ICEM12 comprueba que en una tabla ModuleSequence, las acciones estándar tienen números de secuencia y acciones personalizadas tienen valores de BaseAction y after.</span><span class="sxs-lookup"><span data-stu-id="33bbf-104">ICEM12 verifies that in a ModuleSequence table, standard actions have sequence numbers and custom actions have BaseAction and After values.</span></span>

<span data-ttu-id="33bbf-105">Este ICEM está disponible en el archivo Mergemod. Cub proporcionado en el SDK de Windows Installer 2,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="33bbf-105">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="33bbf-106">Para obtener más información, consulte [componentes de Windows SDK para desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="33bbf-106">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="33bbf-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="33bbf-107">Result</span></span>

<span data-ttu-id="33bbf-108">ICEM12 publica un error en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="33bbf-108">ICEM12 posts an error in the following cases:</span></span>

-   <span data-ttu-id="33bbf-109">Busca el módulo que contiene una [acción estándar](standard-actions.md) sin un número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="33bbf-109">It finds the module contains a [standard action](standard-actions.md) without a sequence number.</span></span>
-   <span data-ttu-id="33bbf-110">Detecta que una acción estándar tiene valores especificados en los campos BaseAction o After de la [tabla ModuleAdminUISequence](moduleadminuisequence-table.md), tabla [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), tabla [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), tabla [ModuleInstallUISequence](moduleinstalluisequence-table.md)o [tabla ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="33bbf-110">It finds that a standard action has values entered in the BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>
-   <span data-ttu-id="33bbf-111">Busca el módulo contiene una [acción personalizada](custom-actions.md) sin ningún valor especificado en los campos Sequence, BaseAction o After de la [tabla ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)Table, [ModuleInstallUISequence Table](moduleinstalluisequence-table.md)o [ModuleInstallExecuteSequence Table](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="33bbf-111">It finds the module contains a [custom action](custom-actions.md) without any values entered into the Sequence, BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>

<span data-ttu-id="33bbf-112">ICEM12 publica una advertencia si encuentra una acción personalizada que tiene un número de secuencia especificado, pero ningún valor en los campos BaseAction o After.</span><span class="sxs-lookup"><span data-stu-id="33bbf-112">ICEM12 posts a warning if it finds a custom action that has a Sequence number specified, but no value in the BaseAction or After fields.</span></span>

<span data-ttu-id="33bbf-113">Tenga en cuenta que todas las acciones que se encuentran en la [tabla CustomAction](customaction-table.md) se consideran acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="33bbf-113">Note that all actions found in the [CustomAction table](customaction-table.md) are considered custom actions.</span></span> <span data-ttu-id="33bbf-114">Todas las demás acciones se consideran acciones estándar.</span><span class="sxs-lookup"><span data-stu-id="33bbf-114">All other action are considered standard actions.</span></span>

## <a name="example"></a><span data-ttu-id="33bbf-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33bbf-115">Example</span></span>

<span data-ttu-id="33bbf-116">ICEM12 expone los siguientes mensajes de error y advertencia para un módulo que contiene las entradas de base de datos que se muestran a continuación:</span><span class="sxs-lookup"><span data-stu-id="33bbf-116">ICEM12 posts the following error and warning messages for a module that contains the database entries shown below:</span></span>

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[<span data-ttu-id="33bbf-117">CustomAction</span><span class="sxs-lookup"><span data-stu-id="33bbf-117">CustomAction</span></span>](customaction-table.md)



| <span data-ttu-id="33bbf-118">Acción</span><span class="sxs-lookup"><span data-stu-id="33bbf-118">Action</span></span>  | <span data-ttu-id="33bbf-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="33bbf-119">Type</span></span> | <span data-ttu-id="33bbf-120">Source</span><span class="sxs-lookup"><span data-stu-id="33bbf-120">Source</span></span>  | <span data-ttu-id="33bbf-121">Destino</span><span class="sxs-lookup"><span data-stu-id="33bbf-121">Target</span></span>  |
|---------|------|---------|---------|
| <span data-ttu-id="33bbf-122">Action1</span><span class="sxs-lookup"><span data-stu-id="33bbf-122">Action1</span></span> | <span data-ttu-id="33bbf-123">30</span><span class="sxs-lookup"><span data-stu-id="33bbf-123">30</span></span>   | <span data-ttu-id="33bbf-124">Source1</span><span class="sxs-lookup"><span data-stu-id="33bbf-124">source1</span></span> | <span data-ttu-id="33bbf-125">target1</span><span class="sxs-lookup"><span data-stu-id="33bbf-125">target1</span></span> |
| <span data-ttu-id="33bbf-126">Action3</span><span class="sxs-lookup"><span data-stu-id="33bbf-126">Action3</span></span> | <span data-ttu-id="33bbf-127">30</span><span class="sxs-lookup"><span data-stu-id="33bbf-127">30</span></span>   | <span data-ttu-id="33bbf-128">source3</span><span class="sxs-lookup"><span data-stu-id="33bbf-128">source3</span></span> | <span data-ttu-id="33bbf-129">target3</span><span class="sxs-lookup"><span data-stu-id="33bbf-129">target3</span></span> |



 

[<span data-ttu-id="33bbf-130">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="33bbf-130">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)



| <span data-ttu-id="33bbf-131">Acción</span><span class="sxs-lookup"><span data-stu-id="33bbf-131">Action</span></span>  | <span data-ttu-id="33bbf-132">Secuencia</span><span class="sxs-lookup"><span data-stu-id="33bbf-132">Sequence</span></span> | <span data-ttu-id="33bbf-133">BaseAction</span><span class="sxs-lookup"><span data-stu-id="33bbf-133">BaseAction</span></span> | <span data-ttu-id="33bbf-134">Después</span><span class="sxs-lookup"><span data-stu-id="33bbf-134">After</span></span> | <span data-ttu-id="33bbf-135">Condición</span><span class="sxs-lookup"><span data-stu-id="33bbf-135">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="33bbf-136">Action2</span><span class="sxs-lookup"><span data-stu-id="33bbf-136">Action2</span></span> |          | <span data-ttu-id="33bbf-137">Action1</span><span class="sxs-lookup"><span data-stu-id="33bbf-137">Action1</span></span>    | <span data-ttu-id="33bbf-138">1</span><span class="sxs-lookup"><span data-stu-id="33bbf-138">1</span></span>     | <span data-ttu-id="33bbf-139">true</span><span class="sxs-lookup"><span data-stu-id="33bbf-139">true</span></span>      |
| <span data-ttu-id="33bbf-140">Action3</span><span class="sxs-lookup"><span data-stu-id="33bbf-140">Action3</span></span> |          |            |       | <span data-ttu-id="33bbf-141">true</span><span class="sxs-lookup"><span data-stu-id="33bbf-141">true</span></span>      |



 

[<span data-ttu-id="33bbf-142">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="33bbf-142">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="33bbf-143">Acción</span><span class="sxs-lookup"><span data-stu-id="33bbf-143">Action</span></span>  | <span data-ttu-id="33bbf-144">Secuencia</span><span class="sxs-lookup"><span data-stu-id="33bbf-144">Sequence</span></span> | <span data-ttu-id="33bbf-145">BaseAction</span><span class="sxs-lookup"><span data-stu-id="33bbf-145">BaseAction</span></span> | <span data-ttu-id="33bbf-146">Después</span><span class="sxs-lookup"><span data-stu-id="33bbf-146">After</span></span> | <span data-ttu-id="33bbf-147">Condición</span><span class="sxs-lookup"><span data-stu-id="33bbf-147">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="33bbf-148">Action1</span><span class="sxs-lookup"><span data-stu-id="33bbf-148">Action1</span></span> | <span data-ttu-id="33bbf-149">1</span><span class="sxs-lookup"><span data-stu-id="33bbf-149">1</span></span>        |            |       | <span data-ttu-id="33bbf-150">true</span><span class="sxs-lookup"><span data-stu-id="33bbf-150">true</span></span>      |



 

<span data-ttu-id="33bbf-151">Para corregir estos errores, pruebe lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="33bbf-151">To fix these errors try the following:</span></span>

-   <span data-ttu-id="33bbf-152">Quite el número de secuencia de la acción personalizada Action1 y use en su lugar los campos BaseAction y after.</span><span class="sxs-lookup"><span data-stu-id="33bbf-152">Remove the sequence number for the custom action Action1 and use the BaseAction and After fields instead.</span></span>
-   <span data-ttu-id="33bbf-153">Escriba valores en los campos Sequence, BaseAction o After para la acción personalizada Action3.</span><span class="sxs-lookup"><span data-stu-id="33bbf-153">Enter values into the Sequence, BaseAction, or After fields for the custom action Action3.</span></span> <span data-ttu-id="33bbf-154">Deje los campos BaseAction y After vacíos para la acción estándar Action2.</span><span class="sxs-lookup"><span data-stu-id="33bbf-154">Leave the BaseAction and After fields empty for standard action Action2.</span></span>
-   <span data-ttu-id="33bbf-155">No deje el campo de secuencia vacío para la acción estándar Action2.</span><span class="sxs-lookup"><span data-stu-id="33bbf-155">Do not leave the Sequence field empty for standard action Action2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33bbf-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33bbf-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33bbf-157">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="33bbf-157">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



