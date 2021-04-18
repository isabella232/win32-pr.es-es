---
description: ICE12 valida las tablas CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence y InstallUISequence de la base de datos Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667769"
---
# <a name="ice12"></a><span data-ttu-id="6e00a-103">ICE12</span><span class="sxs-lookup"><span data-stu-id="6e00a-103">ICE12</span></span>

<span data-ttu-id="6e00a-104">ICE12 consulta las tablas [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)y [InstallUISequence](installuisequence-table.md) para validar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6e00a-104">ICE12 queries the [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [InstallUISequence](installuisequence-table.md) tables to validate the following:</span></span>

-   <span data-ttu-id="6e00a-105">Que la [acción CostFinalize](costfinalize-action.md) se produce en cualquier tabla de secuencia que contenga acciones del tipo de [acción personalizada Type 35](custom-action-type-35.md) o el [tipo de acción personalizada 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="6e00a-105">That the [CostFinalize action](costfinalize-action.md) occurs in any sequence table containing actions of the type [Custom Action Type 35](custom-action-type-35.md) or [Custom Action Type 51](custom-action-type-51.md).</span></span>
-   <span data-ttu-id="6e00a-106">Que cada [tipo de acción personalizada 35](custom-action-type-35.md) venga después de la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="6e00a-106">That every [Custom Action Type 35](custom-action-type-35.md) comes after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="6e00a-107">en las tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="6e00a-107">in the sequence tables.</span></span>
-   <span data-ttu-id="6e00a-108">Que cada [acción personalizada tipo 51](custom-action-type-51.md) que tiene una clave externa en la tabla de directorio de la columna de origen de la tabla CustomAction viene antes de la [acción CostFinalize](costfinalize-action.md) en las tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="6e00a-108">That every [Custom Action Type 51](custom-action-type-51.md) that has a foreign key to the Directory table in the Source column of the CustomAction table comes before the [CostFinalize action](costfinalize-action.md) in the sequence tables.</span></span>

<span data-ttu-id="6e00a-109">Tenga en cuenta que ICE12 no valida el texto con formato de la columna de destino de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="6e00a-109">Note that ICE12 does not validate the formatted text in the Target column of the CustomAction table.</span></span>

## <a name="result"></a><span data-ttu-id="6e00a-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="6e00a-110">Result</span></span>

<span data-ttu-id="6e00a-111">ICE12 envía un mensaje de error si se produce un error en la validación de las acciones personalizadas que establecen una propiedad de directorio.</span><span class="sxs-lookup"><span data-stu-id="6e00a-111">ICE12 posts an error message if validation of the custom actions that set a directory property fails.</span></span>

## <a name="example"></a><span data-ttu-id="6e00a-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e00a-112">Example</span></span>

<span data-ttu-id="6e00a-113">ICE12 publicaría tres errores para el ejemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="6e00a-113">ICE12 would post three errors for the example shown.</span></span>

-   <span data-ttu-id="6e00a-114">En el caso de CA1, no se encontró la carpeta ' carpeta ' en la tabla de directorios</span><span class="sxs-lookup"><span data-stu-id="6e00a-114">For CA1, Folder 'MyFolder' not found in Directory table</span></span>
-   <span data-ttu-id="6e00a-115">En el caso de CA2, la secuencia ' 80 ' viene antes de CostFinalize en la tabla InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="6e00a-115">For CA2, Sequence '80' comes before CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="6e00a-116">Debe aparecer después de ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="6e00a-116">It must come after (CF@100)</span></span>
-   <span data-ttu-id="6e00a-117">En el caso de CA3, la secuencia ' 125 ' se incluye después de CostFinalize en la tabla InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="6e00a-117">For CA3, Sequence '125' comes after CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="6e00a-118">Debe ser anterior a ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="6e00a-118">It must come before (CF@100)</span></span>

<span data-ttu-id="6e00a-119">[Tabla CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6e00a-119">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="6e00a-120">Acción</span><span class="sxs-lookup"><span data-stu-id="6e00a-120">Action</span></span> | <span data-ttu-id="6e00a-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e00a-121">Type</span></span> | <span data-ttu-id="6e00a-122">Source</span><span class="sxs-lookup"><span data-stu-id="6e00a-122">Source</span></span>        |
|--------|------|---------------|
| <span data-ttu-id="6e00a-123">CA1</span><span class="sxs-lookup"><span data-stu-id="6e00a-123">CA1</span></span>    | <span data-ttu-id="6e00a-124">35</span><span class="sxs-lookup"><span data-stu-id="6e00a-124">35</span></span>   | <span data-ttu-id="6e00a-125">MyFolder</span><span class="sxs-lookup"><span data-stu-id="6e00a-125">MyFolder</span></span>      |
| <span data-ttu-id="6e00a-126">CA2</span><span class="sxs-lookup"><span data-stu-id="6e00a-126">CA2</span></span>    | <span data-ttu-id="6e00a-127">35</span><span class="sxs-lookup"><span data-stu-id="6e00a-127">35</span></span>   | <span data-ttu-id="6e00a-128">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="6e00a-128">WindowsFolder</span></span> |
| <span data-ttu-id="6e00a-129">CA3</span><span class="sxs-lookup"><span data-stu-id="6e00a-129">CA3</span></span>    | <span data-ttu-id="6e00a-130">51</span><span class="sxs-lookup"><span data-stu-id="6e00a-130">51</span></span>   | <span data-ttu-id="6e00a-131">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="6e00a-131">WindowsFolder</span></span> |



 

[<span data-ttu-id="6e00a-132">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="6e00a-132">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="6e00a-133">Directorio</span><span class="sxs-lookup"><span data-stu-id="6e00a-133">Directory</span></span>     | <span data-ttu-id="6e00a-134">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="6e00a-134">Directory\_Parent</span></span> | <span data-ttu-id="6e00a-135">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="6e00a-135">DefaultDir</span></span>    |
|---------------|-------------------|---------------|
| <span data-ttu-id="6e00a-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="6e00a-136">TARGETDIR</span></span>     |                   | <span data-ttu-id="6e00a-137">SourceDir</span><span class="sxs-lookup"><span data-stu-id="6e00a-137">SourceDir</span></span>     |
| <span data-ttu-id="6e00a-138">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="6e00a-138">WindowsFolder</span></span> | <span data-ttu-id="6e00a-139">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="6e00a-139">TARGETDIR</span></span>         | <span data-ttu-id="6e00a-140">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="6e00a-140">WindowsFolder</span></span> |



 

<span data-ttu-id="6e00a-141">[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6e00a-141">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="6e00a-142">Acción</span><span class="sxs-lookup"><span data-stu-id="6e00a-142">Action</span></span>       | <span data-ttu-id="6e00a-143">Secuencia</span><span class="sxs-lookup"><span data-stu-id="6e00a-143">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="6e00a-144">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="6e00a-144">CostFinalize</span></span> | <span data-ttu-id="6e00a-145">100</span><span class="sxs-lookup"><span data-stu-id="6e00a-145">100</span></span>      |
| <span data-ttu-id="6e00a-146">CA2</span><span class="sxs-lookup"><span data-stu-id="6e00a-146">CA2</span></span>          | <span data-ttu-id="6e00a-147">80</span><span class="sxs-lookup"><span data-stu-id="6e00a-147">80</span></span>       |
| <span data-ttu-id="6e00a-148">CA3</span><span class="sxs-lookup"><span data-stu-id="6e00a-148">CA3</span></span>          | <span data-ttu-id="6e00a-149">125</span><span class="sxs-lookup"><span data-stu-id="6e00a-149">125</span></span>      |



 

<span data-ttu-id="6e00a-150">Para corregir el error de CA1, cambie su entrada en la columna de origen de la tabla CustomAction a una entrada existente en la tabla del directorio o agregue mi carpeta a la tabla del directorio.</span><span class="sxs-lookup"><span data-stu-id="6e00a-150">To fix the error for CA1 change its entry in its Source column in the CustomAction table to an existing entry in the Directory table or add MyFolder to the Directory table.</span></span>

<span data-ttu-id="6e00a-151">Para corregir el error de CA2, cambie su secuencia en la tabla InstallExecuteSequence de forma que venga después de la acción CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="6e00a-151">To fix the error for CA2, change its sequence in the InstallExecuteSequence table such that it comes after the CostFinalize action.</span></span>

<span data-ttu-id="6e00a-152">Para corregir el error de CA3, cambie su secuencia en la tabla InstallExecuteSequence de forma que venga antes de la acción CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="6e00a-152">To fix the error for CA3, change its sequence in the InstallExecuteSequence table such that it comes before the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e00a-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e00a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e00a-154">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="6e00a-154">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



