---
description: ICE75 comprueba que todas las acciones personalizadas de tipo de acción personalizada 17 (DLL), tipo de acción personalizada 18 (EXE), tipo de acción personalizada 21 (JScript) y tipo de acción personalizada 22 (VBScript) se ordenan después de la acción CostFinalize.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361070"
---
# <a name="ice75"></a><span data-ttu-id="d4579-103">ICE75</span><span class="sxs-lookup"><span data-stu-id="d4579-103">ICE75</span></span>

<span data-ttu-id="d4579-104">ICE75 comprueba que todas las acciones personalizadas de tipo de acción personalizada [17](custom-action-type-17.md) (dll), [tipo de acción personalizada 18](custom-action-type-18.md) (exe), tipo de [acción personalizada 21](custom-action-type-21.md) (JScript) y [tipo de acción personalizada 22](custom-action-type-22.md) (VBScript) se ordenan después de la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="d4579-104">ICE75 verifies that all [Custom Action Type 17](custom-action-type-17.md) (DLL), [Custom Action Type 18](custom-action-type-18.md) (EXE), [Custom Action type 21](custom-action-type-21.md) (JScript), and [Custom Action Type 22](custom-action-type-22.md) (VBScript) custom actions are sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="d4579-105">Estos tipos de acciones personalizadas usan un archivo instalado como origen.</span><span class="sxs-lookup"><span data-stu-id="d4579-105">These types of custom action use an installed file as their source.</span></span> <span data-ttu-id="d4579-106">ICE75 comprueba la tabla [InstallUISequence](installuisequence-table.md), la tabla [InstallExecuteSequence](installexecutesequence-table.md), la tabla [AdminUISequence](adminuisequence-table.md)y la [tabla AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d4579-106">ICE75 checks the [InstallUISequence Table](installuisequence-table.md), [InstallExecuteSequence Table](installexecutesequence-table.md), [AdminUISequence Table](adminuisequence-table.md), and [AdminExecuteSequence Table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="d4579-107">Tenga en cuenta que la acción CostFinalize es necesaria en estas tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="d4579-107">Note that the CostFinalize action is required in these sequence tables.</span></span>

## <a name="result"></a><span data-ttu-id="d4579-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="d4579-108">Result</span></span>

<span data-ttu-id="d4579-109">ICE75 publica un error si encuentra una acción personalizada mediante un archivo instalado como un archivo de código fuente que no se secuencia después de la acción CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="d4579-109">ICE75 posts an error if it finds a custom action using an installed file as a source file that is not sequenced after the CostFinalize action.</span></span>

## <a name="example"></a><span data-ttu-id="d4579-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4579-110">Example</span></span>

<span data-ttu-id="d4579-111">ICE75 notifica los siguientes errores para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="d4579-111">ICE75 reports the following errors for the example shown:</span></span>

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

<span data-ttu-id="d4579-112">[Tabla CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d4579-112">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="d4579-113">Acción</span><span class="sxs-lookup"><span data-stu-id="d4579-113">Action</span></span>      | <span data-ttu-id="d4579-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4579-114">Type</span></span> | <span data-ttu-id="d4579-115">Source</span><span class="sxs-lookup"><span data-stu-id="d4579-115">Source</span></span>  |
|-------------|------|---------|
| <span data-ttu-id="d4579-116">CA \_ FileExe</span><span class="sxs-lookup"><span data-stu-id="d4579-116">CA\_FileExe</span></span> | <span data-ttu-id="d4579-117">18</span><span class="sxs-lookup"><span data-stu-id="d4579-117">18</span></span>   | <span data-ttu-id="d4579-118">FileExe</span><span class="sxs-lookup"><span data-stu-id="d4579-118">FileExe</span></span> |
| <span data-ttu-id="d4579-119">CA \_ FileDLL</span><span class="sxs-lookup"><span data-stu-id="d4579-119">CA\_FileDLL</span></span> | <span data-ttu-id="d4579-120">17</span><span class="sxs-lookup"><span data-stu-id="d4579-120">17</span></span>   | <span data-ttu-id="d4579-121">FileDLL</span><span class="sxs-lookup"><span data-stu-id="d4579-121">FileDLL</span></span> |



 

<span data-ttu-id="d4579-122">[Tabla AdminUISequence](adminuisequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d4579-122">[AdminUISequence Table](adminuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="d4579-123">Acción</span><span class="sxs-lookup"><span data-stu-id="d4579-123">Action</span></span>      | <span data-ttu-id="d4579-124">Secuencia</span><span class="sxs-lookup"><span data-stu-id="d4579-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="d4579-125">CA \_ FileExe</span><span class="sxs-lookup"><span data-stu-id="d4579-125">CA\_FileExe</span></span> | <span data-ttu-id="d4579-126">1100</span><span class="sxs-lookup"><span data-stu-id="d4579-126">1100</span></span>     |



 

<span data-ttu-id="d4579-127">[Tabla AdminExecuteSequence](adminexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d4579-127">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="d4579-128">Acción</span><span class="sxs-lookup"><span data-stu-id="d4579-128">Action</span></span>       | <span data-ttu-id="d4579-129">Secuencia</span><span class="sxs-lookup"><span data-stu-id="d4579-129">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="d4579-130">CA \_ FileDLL</span><span class="sxs-lookup"><span data-stu-id="d4579-130">CA\_FileDLL</span></span>  | <span data-ttu-id="d4579-131">800</span><span class="sxs-lookup"><span data-stu-id="d4579-131">800</span></span>      |
| <span data-ttu-id="d4579-132">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="d4579-132">CostFinalize</span></span> | <span data-ttu-id="d4579-133">1000</span><span class="sxs-lookup"><span data-stu-id="d4579-133">1000</span></span>     |



 

<span data-ttu-id="d4579-134">Para corregir los errores, ordene las acciones personalizadas después de la acción CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="d4579-134">To fix the errors, sequence the custom actions after the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4579-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4579-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4579-136">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="d4579-136">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



