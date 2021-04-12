---
description: ICE95 comprueba la tabla de control y la tabla BBControl para comprobar que los controles de la cartelera caben en todas las cartelera.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278455"
---
# <a name="ice95"></a><span data-ttu-id="05bac-103">ICE95</span><span class="sxs-lookup"><span data-stu-id="05bac-103">ICE95</span></span>

<span data-ttu-id="05bac-104">ICE95 comprueba la tabla de [control](control-table.md) y la [tabla BBControl](bbcontrol-table.md) para comprobar que los controles de la cartelera caben en todas las cartelera.</span><span class="sxs-lookup"><span data-stu-id="05bac-104">ICE95 checks the [Control table](control-table.md) and [BBControl table](bbcontrol-table.md) to verify that the billboard controls fit onto all the billboards.</span></span>

## <a name="result"></a><span data-ttu-id="05bac-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="05bac-105">Result</span></span>

<span data-ttu-id="05bac-106">Si se cumple alguna de las siguientes condiciones, el control de la cartelera no cabe en una cartelera.</span><span class="sxs-lookup"><span data-stu-id="05bac-106">If any of the following are true, a billboard control fails to fit on a billboard.</span></span> <span data-ttu-id="05bac-107">ICE95 expone las siguientes advertencias.</span><span class="sxs-lookup"><span data-stu-id="05bac-107">ICE95 posts the following warnings.</span></span>



| <span data-ttu-id="05bac-108">ADVERTENCIA de ICE95</span><span class="sxs-lookup"><span data-stu-id="05bac-108">ICE95 warning</span></span>                                                                                                                                                                                                              | <span data-ttu-id="05bac-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="05bac-109">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="05bac-110">El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de la cartelera de la tabla de control.</span><span class="sxs-lookup"><span data-stu-id="05bac-110">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="05bac-111">La coordenada X supera el límite del ancho mínimo del control de la cartelera% s</span><span class="sxs-lookup"><span data-stu-id="05bac-111">The X coordinate exceeds the boundary of the minimum billboard control width %s</span></span>                   | <span data-ttu-id="05bac-112">La coordenada X del control está fuera del ancho de la cartelera.</span><span class="sxs-lookup"><span data-stu-id="05bac-112">The control's X coordinate is outside the width of the billboard.</span></span>                          |
| <span data-ttu-id="05bac-113">El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de la cartelera de la tabla de control.</span><span class="sxs-lookup"><span data-stu-id="05bac-113">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="05bac-114">La coordenada Y supera el límite de la altura del control de la cartelera mínima% s</span><span class="sxs-lookup"><span data-stu-id="05bac-114">The Y coordinate exceeds the boundary of the minimum billboard control height %s</span></span>                  | <span data-ttu-id="05bac-115">La coordenada Y del control está debajo de la parte inferior de la cartelera.</span><span class="sxs-lookup"><span data-stu-id="05bac-115">The control's Y coordinate is below the bottom of the billboard.</span></span>                           |
| <span data-ttu-id="05bac-116">El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de la cartelera de la tabla de control.</span><span class="sxs-lookup"><span data-stu-id="05bac-116">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="05bac-117">La coordenada X y el ancho combinados juntos superan el ancho mínimo del control de la cartelera% s</span><span class="sxs-lookup"><span data-stu-id="05bac-117">The X coordinate and the width combined together exceeds the minimum billboard control width %s</span></span>   | <span data-ttu-id="05bac-118">La coordenada X del control más el ancho del control está fuera del ancho de la cartelera.</span><span class="sxs-lookup"><span data-stu-id="05bac-118">The control's X coordinate plus the control's width is outside the width of the billboard.</span></span> |
| <span data-ttu-id="05bac-119">El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de la cartelera de la tabla de control.</span><span class="sxs-lookup"><span data-stu-id="05bac-119">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="05bac-120">La coordenada Y y el alto combinado juntos superan el alto del control de la cartelera mínimo% s</span><span class="sxs-lookup"><span data-stu-id="05bac-120">The Y coordinate and the height combined together exceeds the minimum billboard control height %s</span></span> | <span data-ttu-id="05bac-121">La coordenada Y del control más el alto del control está por debajo de la parte inferior de la cartelera.</span><span class="sxs-lookup"><span data-stu-id="05bac-121">The control's Y coordinate plus the control's height is below the bottom of the billboard.</span></span> |



 

## <a name="example"></a><span data-ttu-id="05bac-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05bac-122">Example</span></span>

<span data-ttu-id="05bac-123">ICE95 notifica las siguientes advertencias para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="05bac-123">ICE95 reports the following warnings for the example:</span></span>

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

<span data-ttu-id="05bac-124">Tabla de control (parcial) (parcial)</span><span class="sxs-lookup"><span data-stu-id="05bac-124">Control Table (partial) (partial)</span></span>



| <span data-ttu-id="05bac-125">Control</span><span class="sxs-lookup"><span data-stu-id="05bac-125">Control</span></span>  | <span data-ttu-id="05bac-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="05bac-126">Type</span></span>      | <span data-ttu-id="05bac-127">Ancho</span><span class="sxs-lookup"><span data-stu-id="05bac-127">Width</span></span> | <span data-ttu-id="05bac-128">Alto</span><span class="sxs-lookup"><span data-stu-id="05bac-128">Height</span></span> |
|----------|-----------|-------|--------|
| <span data-ttu-id="05bac-129">control1</span><span class="sxs-lookup"><span data-stu-id="05bac-129">control1</span></span> | <span data-ttu-id="05bac-130">Valla</span><span class="sxs-lookup"><span data-stu-id="05bac-130">Billboard</span></span> | <span data-ttu-id="05bac-131">300</span><span class="sxs-lookup"><span data-stu-id="05bac-131">300</span></span>   | <span data-ttu-id="05bac-132">100</span><span class="sxs-lookup"><span data-stu-id="05bac-132">100</span></span>    |
| <span data-ttu-id="05bac-133">Control2</span><span class="sxs-lookup"><span data-stu-id="05bac-133">Control2</span></span> | <span data-ttu-id="05bac-134">Valla</span><span class="sxs-lookup"><span data-stu-id="05bac-134">Billboard</span></span> | <span data-ttu-id="05bac-135">100</span><span class="sxs-lookup"><span data-stu-id="05bac-135">100</span></span>   | <span data-ttu-id="05bac-136">300</span><span class="sxs-lookup"><span data-stu-id="05bac-136">300</span></span>    |



 

[<span data-ttu-id="05bac-137">Tabla BBControl</span><span class="sxs-lookup"><span data-stu-id="05bac-137">BBControl table</span></span>](bbcontrol-table.md)



| <span data-ttu-id="05bac-138">Valla\_</span><span class="sxs-lookup"><span data-stu-id="05bac-138">Billboard\_</span></span> | <span data-ttu-id="05bac-139">BBControl</span><span class="sxs-lookup"><span data-stu-id="05bac-139">BBControl</span></span>  | <span data-ttu-id="05bac-140">X</span><span class="sxs-lookup"><span data-stu-id="05bac-140">X</span></span>   | <span data-ttu-id="05bac-141">Y</span><span class="sxs-lookup"><span data-stu-id="05bac-141">Y</span></span>   | <span data-ttu-id="05bac-142">Ancho</span><span class="sxs-lookup"><span data-stu-id="05bac-142">Width</span></span> | <span data-ttu-id="05bac-143">Alto</span><span class="sxs-lookup"><span data-stu-id="05bac-143">Height</span></span> |
|-------------|------------|-----|-----|-------|--------|
| <span data-ttu-id="05bac-144">billboard1</span><span class="sxs-lookup"><span data-stu-id="05bac-144">billboard1</span></span>  | <span data-ttu-id="05bac-145">bbcontrol1</span><span class="sxs-lookup"><span data-stu-id="05bac-145">bbcontrol1</span></span> | <span data-ttu-id="05bac-146">200</span><span class="sxs-lookup"><span data-stu-id="05bac-146">200</span></span> | <span data-ttu-id="05bac-147">0</span><span class="sxs-lookup"><span data-stu-id="05bac-147">0</span></span>   | <span data-ttu-id="05bac-148">100</span><span class="sxs-lookup"><span data-stu-id="05bac-148">100</span></span>   | <span data-ttu-id="05bac-149">100</span><span class="sxs-lookup"><span data-stu-id="05bac-149">100</span></span>    |
| <span data-ttu-id="05bac-150">billboard1</span><span class="sxs-lookup"><span data-stu-id="05bac-150">billboard1</span></span>  | <span data-ttu-id="05bac-151">bbcontrol2</span><span class="sxs-lookup"><span data-stu-id="05bac-151">bbcontrol2</span></span> | <span data-ttu-id="05bac-152">0</span><span class="sxs-lookup"><span data-stu-id="05bac-152">0</span></span>   | <span data-ttu-id="05bac-153">200</span><span class="sxs-lookup"><span data-stu-id="05bac-153">200</span></span> | <span data-ttu-id="05bac-154">100</span><span class="sxs-lookup"><span data-stu-id="05bac-154">100</span></span>   | <span data-ttu-id="05bac-155">100</span><span class="sxs-lookup"><span data-stu-id="05bac-155">100</span></span>    |
| <span data-ttu-id="05bac-156">billboard1</span><span class="sxs-lookup"><span data-stu-id="05bac-156">billboard1</span></span>  | <span data-ttu-id="05bac-157">bbcontrol3</span><span class="sxs-lookup"><span data-stu-id="05bac-157">bbcontrol3</span></span> | <span data-ttu-id="05bac-158">50</span><span class="sxs-lookup"><span data-stu-id="05bac-158">50</span></span>  | <span data-ttu-id="05bac-159">0</span><span class="sxs-lookup"><span data-stu-id="05bac-159">0</span></span>   | <span data-ttu-id="05bac-160">100</span><span class="sxs-lookup"><span data-stu-id="05bac-160">100</span></span>   | <span data-ttu-id="05bac-161">50</span><span class="sxs-lookup"><span data-stu-id="05bac-161">50</span></span>     |
| <span data-ttu-id="05bac-162">billboard1</span><span class="sxs-lookup"><span data-stu-id="05bac-162">billboard1</span></span>  | <span data-ttu-id="05bac-163">bbcontrol4</span><span class="sxs-lookup"><span data-stu-id="05bac-163">bbcontrol4</span></span> | <span data-ttu-id="05bac-164">0</span><span class="sxs-lookup"><span data-stu-id="05bac-164">0</span></span>   | <span data-ttu-id="05bac-165">50</span><span class="sxs-lookup"><span data-stu-id="05bac-165">50</span></span>  | <span data-ttu-id="05bac-166">50</span><span class="sxs-lookup"><span data-stu-id="05bac-166">50</span></span>    | <span data-ttu-id="05bac-167">100</span><span class="sxs-lookup"><span data-stu-id="05bac-167">100</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="05bac-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05bac-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05bac-169">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="05bac-169">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



