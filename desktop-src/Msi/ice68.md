---
description: ICE68 comprueba que todos los tipos de acción personalizados necesarios para una instalación sean válidos.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669809"
---
# <a name="ice68"></a><span data-ttu-id="d5af5-103">ICE68</span><span class="sxs-lookup"><span data-stu-id="d5af5-103">ICE68</span></span>

<span data-ttu-id="d5af5-104">ICE68 comprueba que todos los tipos de acción personalizados necesarios para una instalación sean válidos.</span><span class="sxs-lookup"><span data-stu-id="d5af5-104">ICE68 checks that all custom action types needed for an installation are valid.</span></span> <span data-ttu-id="d5af5-105">Si no se corrige el error detectado por ICE68, se produce un error en una instalación que intenta ejecutar la acción.</span><span class="sxs-lookup"><span data-stu-id="d5af5-105">Failure to fix the error reported by ICE68 causes an installation that attempts to execute the action to fail.</span></span> <span data-ttu-id="d5af5-106">ICE68 emite una advertencia si se establece el atributo **msidbCustomActionTypeNoImpersonate** sin establecer también el atributo **msidbCustomActionTypeInScript** .</span><span class="sxs-lookup"><span data-stu-id="d5af5-106">ICE68 issues a warning if the **msidbCustomActionTypeNoImpersonate** attribute is set without also setting the **msidbCustomActionTypeInScript** attribute.</span></span>

## <a name="result"></a><span data-ttu-id="d5af5-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="d5af5-107">Result</span></span>

<span data-ttu-id="d5af5-108">ICE68 devuelve un error si un tipo de acción necesario para una instalación de no es válido.</span><span class="sxs-lookup"><span data-stu-id="d5af5-108">ICE68 returns an error if an action type needed for an installation is invalid.</span></span>

## <a name="example"></a><span data-ttu-id="d5af5-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5af5-109">Example</span></span>

<span data-ttu-id="d5af5-110">ICE68 envía la siguiente advertencia si una acción personalizada tiene el bit **msidbCustomActionTypeNoImpersonate** establecido en el campo Type de la tabla CustomAction sin la **msidbCustomActionTypeInScript** establecida también.</span><span class="sxs-lookup"><span data-stu-id="d5af5-110">ICE68 posts the following warning if a custom action has the **msidbCustomActionTypeNoImpersonate** bit set in the Type field of the CustomAction table without the **msidbCustomActionTypeInScript** also set.</span></span>

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

<span data-ttu-id="d5af5-111">Para corregir esta advertencia, incluya **msidbCustomActionTypeInScript** (0x400) si la acción personalizada incluye **msidbCustomActionTypeNoImpersonate** (0x800).</span><span class="sxs-lookup"><span data-stu-id="d5af5-111">To fix this warning, include **msidbCustomActionTypeInScript** (0x400) if the custom action includes **msidbCustomActionTypeNoImpersonate** (0x800).</span></span> <span data-ttu-id="d5af5-112">En caso contrario, el instalador omite el atributo **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="d5af5-112">Otherwise the installer ignores the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="d5af5-113">Para obtener más información, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="d5af5-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="d5af5-114">ICE68 notifica el siguiente error para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="d5af5-114">ICE68 reports the following error for the example shown:</span></span>

``` syntax
Invalid custom action type for action 'Action1'.
```

<span data-ttu-id="d5af5-115">1027 no es un tipo de acción válido.</span><span class="sxs-lookup"><span data-stu-id="d5af5-115">1027 is not a valid action type.</span></span>

<span data-ttu-id="d5af5-116">Para corregir este error, elija un tipo de acción personalizado válido.</span><span class="sxs-lookup"><span data-stu-id="d5af5-116">To fix this error, choose a valid custom action type.</span></span>

<span data-ttu-id="d5af5-117">[Tabla CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d5af5-117">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="d5af5-118">Acción</span><span class="sxs-lookup"><span data-stu-id="d5af5-118">Action</span></span>  | <span data-ttu-id="d5af5-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5af5-119">Type</span></span> | <span data-ttu-id="d5af5-120">Source</span><span class="sxs-lookup"><span data-stu-id="d5af5-120">Source</span></span>   | <span data-ttu-id="d5af5-121">Destino</span><span class="sxs-lookup"><span data-stu-id="d5af5-121">Target</span></span>     |
|---------|------|----------|------------|
| <span data-ttu-id="d5af5-122">Action1</span><span class="sxs-lookup"><span data-stu-id="d5af5-122">Action1</span></span> | <span data-ttu-id="d5af5-123">1027</span><span class="sxs-lookup"><span data-stu-id="d5af5-123">1027</span></span> | <span data-ttu-id="d5af5-124">Argumento</span><span class="sxs-lookup"><span data-stu-id="d5af5-124">Argument</span></span> | <span data-ttu-id="d5af5-125">Component1</span><span class="sxs-lookup"><span data-stu-id="d5af5-125">Component1</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d5af5-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5af5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5af5-127">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="d5af5-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



