---
description: ICE77 comprueba que las acciones personalizadas con el conjunto de bits msidbCustomActionTypeInScript se ordenan después de la acción InstallInitialize y antes de la acción InstallFinalize.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154817"
---
# <a name="ice77"></a><span data-ttu-id="e85d6-103">ICE77</span><span class="sxs-lookup"><span data-stu-id="e85d6-103">ICE77</span></span>

<span data-ttu-id="e85d6-104">ICE77 comprueba que las acciones personalizadas con el conjunto de bits **msidbCustomActionTypeInScript** se ordenan después de la [acción InstallInitialize](installinitialize-action.md) y antes de la [acción InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e85d6-104">ICE77 verifies that custom actions with the **msidbCustomActionTypeInScript** bit set are sequenced after the [InstallInitialize action](installinitialize-action.md) and before the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="e85d6-105">ICE77 comprueba la secuencia en la tabla [InstallExecuteSequence](installexecutesequence-table.md) y en la [tabla AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="e85d6-105">ICE77 checks the sequence in the [InstallExecuteSequence table](installexecutesequence-table.md) and [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="e85d6-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="e85d6-106">Result</span></span>

<span data-ttu-id="e85d6-107">ICE77 publica un error si se secuencia una acción personalizada en el script antes de la acción InstallInitialize o después de la acción InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="e85d6-107">ICE77 posts an error if an in-script custom action is sequenced before the InstallInitialize action or after the InstallFinalize action.</span></span>

<span data-ttu-id="e85d6-108">ICE77 publica un error si falta la acción InstallInitialize o la acción InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="e85d6-108">ICE77 posts an error if the InstallInitialize action or the InstallFinalize action is missing.</span></span>

## <a name="example"></a><span data-ttu-id="e85d6-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e85d6-109">Example</span></span>

<span data-ttu-id="e85d6-110">ICE77 notifica los siguientes errores para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e85d6-110">ICE77 reports the following errors for the example:</span></span>

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

<span data-ttu-id="e85d6-111">[Tabla CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e85d6-111">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="e85d6-112">Acción</span><span class="sxs-lookup"><span data-stu-id="e85d6-112">Action</span></span>              | <span data-ttu-id="e85d6-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="e85d6-113">Type</span></span> |
|---------------------|------|
| <span data-ttu-id="e85d6-114">CA \_ InScriptInstall</span><span class="sxs-lookup"><span data-stu-id="e85d6-114">CA\_InScriptInstall</span></span> | <span data-ttu-id="e85d6-115">1025</span><span class="sxs-lookup"><span data-stu-id="e85d6-115">1025</span></span> |
| <span data-ttu-id="e85d6-116">CA \_ InScriptAdmin</span><span class="sxs-lookup"><span data-stu-id="e85d6-116">CA\_InScriptAdmin</span></span>   | <span data-ttu-id="e85d6-117">1026</span><span class="sxs-lookup"><span data-stu-id="e85d6-117">1026</span></span> |



 

<span data-ttu-id="e85d6-118">[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e85d6-118">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="e85d6-119">Acción</span><span class="sxs-lookup"><span data-stu-id="e85d6-119">Action</span></span>              | <span data-ttu-id="e85d6-120">Secuencia</span><span class="sxs-lookup"><span data-stu-id="e85d6-120">Sequence</span></span> |
|---------------------|----------|
| <span data-ttu-id="e85d6-121">CA \_ InScriptInstall</span><span class="sxs-lookup"><span data-stu-id="e85d6-121">CA\_InScriptInstall</span></span> | <span data-ttu-id="e85d6-122">2000</span><span class="sxs-lookup"><span data-stu-id="e85d6-122">2000</span></span>     |
| <span data-ttu-id="e85d6-123">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="e85d6-123">InstallInitialize</span></span>   | <span data-ttu-id="e85d6-124">1.500</span><span class="sxs-lookup"><span data-stu-id="e85d6-124">1500</span></span>     |



 

<span data-ttu-id="e85d6-125">[Tabla AdminExecuteSequence](adminexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e85d6-125">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="e85d6-126">Acción</span><span class="sxs-lookup"><span data-stu-id="e85d6-126">Action</span></span>            | <span data-ttu-id="e85d6-127">Secuencia</span><span class="sxs-lookup"><span data-stu-id="e85d6-127">Sequence</span></span> |
|-------------------|----------|
| <span data-ttu-id="e85d6-128">CA \_ InScriptAdmin</span><span class="sxs-lookup"><span data-stu-id="e85d6-128">CA\_InScriptAdmin</span></span> | <span data-ttu-id="e85d6-129">1400</span><span class="sxs-lookup"><span data-stu-id="e85d6-129">1400</span></span>     |
| <span data-ttu-id="e85d6-130">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="e85d6-130">InstallInitialize</span></span> | <span data-ttu-id="e85d6-131">1.500</span><span class="sxs-lookup"><span data-stu-id="e85d6-131">1500</span></span>     |
| <span data-ttu-id="e85d6-132">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="e85d6-132">InstallFinalize</span></span>   | <span data-ttu-id="e85d6-133">6600</span><span class="sxs-lookup"><span data-stu-id="e85d6-133">6600</span></span>     |



 

<span data-ttu-id="e85d6-134">Para corregir los errores, ordene las acciones personalizadas en el script después de la acción InstallInitialize y antes de la acción InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="e85d6-134">To fix the errors, sequence the in-script custom actions after the InstallInitialize action and before the InstallFinalize action.</span></span> <span data-ttu-id="e85d6-135">Las acciones InstallInitialize y InstallFinalize deben estar presentes en la tabla InstallExecuteSequence y en la tabla AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="e85d6-135">The InstallInitialize and InstallFinalize actions must be present in the InstallExecuteSequence table and the AdminExecuteSequence table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e85d6-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e85d6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e85d6-137">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="e85d6-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



