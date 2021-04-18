---
description: Transición de compositor
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transición de compositor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556999"
---
# <a name="compositor-transition"></a><span data-ttu-id="c48c8-103">Transición de compositor</span><span class="sxs-lookup"><span data-stu-id="c48c8-103">Compositor Transition</span></span>

> [!Note]  
> <span data-ttu-id="c48c8-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c48c8-104">\[Deprecated.</span></span> <span data-ttu-id="c48c8-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c48c8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c48c8-106">La transición de compositor compone un subrectángulo desde el primer plano en un rectángulo designado en el fondo, sin alterar el resto del fondo.</span><span class="sxs-lookup"><span data-stu-id="c48c8-106">The Compositor transition composites a subrectangle from the foreground into a designated rectangle on the background, without altering the rest of the background.</span></span> <span data-ttu-id="c48c8-107">Use esta transición para crear efectos de pantalla dividida o imagen en imagen.</span><span class="sxs-lookup"><span data-stu-id="c48c8-107">Use this transition to create split-screen or picture-in-picture effects.</span></span>

<span data-ttu-id="c48c8-108">La siguiente imagen muestra la transición de compositor:</span><span class="sxs-lookup"><span data-stu-id="c48c8-108">The following image shows the compositor transition:</span></span>

![transición de compositor](images/trans-compositor.png)

<span data-ttu-id="c48c8-110">IDENTIFICADOR de clase (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span><span class="sxs-lookup"><span data-stu-id="c48c8-110">Class ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span></span>

<span data-ttu-id="c48c8-111">Nombre de la variable CLSID: CLSID \_ DxtCompositor</span><span class="sxs-lookup"><span data-stu-id="c48c8-111">CLSID Variable Name: CLSID\_DxtCompositor</span></span>

<span data-ttu-id="c48c8-112">Nombre descriptivo: "DxtCompositor"</span><span class="sxs-lookup"><span data-stu-id="c48c8-112">Friendly Name: "DxtCompositor"</span></span>

<span data-ttu-id="c48c8-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c48c8-113">Properties</span></span>



| <span data-ttu-id="c48c8-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c48c8-114">Property</span></span>   | <span data-ttu-id="c48c8-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="c48c8-115">Type</span></span> | <span data-ttu-id="c48c8-116">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="c48c8-116">Default</span></span> | <span data-ttu-id="c48c8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c48c8-117">Description</span></span>                                                    |
|------------|------|---------|----------------------------------------------------------------|
| <span data-ttu-id="c48c8-118">Alto</span><span class="sxs-lookup"><span data-stu-id="c48c8-118">Height</span></span>     | <span data-ttu-id="c48c8-119">long</span><span class="sxs-lookup"><span data-stu-id="c48c8-119">long</span></span> | <span data-ttu-id="c48c8-120">0</span><span class="sxs-lookup"><span data-stu-id="c48c8-120">0</span></span>       | <span data-ttu-id="c48c8-121">Alto del rectángulo de destino, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c48c8-121">Height of the target rectangle, in pixels.</span></span>                     |
| <span data-ttu-id="c48c8-122">OffsetX</span><span class="sxs-lookup"><span data-stu-id="c48c8-122">OffsetX</span></span>    | <span data-ttu-id="c48c8-123">long</span><span class="sxs-lookup"><span data-stu-id="c48c8-123">long</span></span> | <span data-ttu-id="c48c8-124">0</span><span class="sxs-lookup"><span data-stu-id="c48c8-124">0</span></span>       | <span data-ttu-id="c48c8-125">Desplazamiento horizontal del rectángulo de destino, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c48c8-125">Horizontal offset of the target rectangle, in pixels.</span></span>          |
| <span data-ttu-id="c48c8-126">OffsetY</span><span class="sxs-lookup"><span data-stu-id="c48c8-126">OffsetY</span></span>    | <span data-ttu-id="c48c8-127">long</span><span class="sxs-lookup"><span data-stu-id="c48c8-127">long</span></span> | <span data-ttu-id="c48c8-128">0</span><span class="sxs-lookup"><span data-stu-id="c48c8-128">0</span></span>       | <span data-ttu-id="c48c8-129">Desplazamiento vertical del rectángulo de destino, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c48c8-129">Vertical offset of the target rectangle, in pixels.</span></span>            |
| <span data-ttu-id="c48c8-130">SrcHeight</span><span class="sxs-lookup"><span data-stu-id="c48c8-130">SrcHeight</span></span>  | <span data-ttu-id="c48c8-131">long</span><span class="sxs-lookup"><span data-stu-id="c48c8-131">long</span></span> | <span data-ttu-id="c48c8-132">0</span><span class="sxs-lookup"><span data-stu-id="c48c8-132">0</span></span>       | <span data-ttu-id="c48c8-133">Alto del subrectángulo en el origen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c48c8-133">The height of the subrectangle on the source, in pixels.</span></span>       |
| <span data-ttu-id="c48c8-134">SrcOffsetX</span><span class="sxs-lookup"><span data-stu-id="c48c8-134">SrcOffsetX</span></span> | <span data-ttu-id="c48c8-135">long</span><span class="sxs-lookup"><span data-stu-id="c48c8-135">long</span></span> | <span data-ttu-id="c48c8-136">0</span><span class="sxs-lookup"><span data-stu-id="c48c8-136">0</span></span>       | <span data-ttu-id="c48c8-137">Coordenada x del subrectángulo en el origen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c48c8-137">The x-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="c48c8-138">SrcOffsetY</span><span class="sxs-lookup"><span data-stu-id="c48c8-138">SrcOffsetY</span></span> | <span data-ttu-id="c48c8-139">long</span><span class="sxs-lookup"><span data-stu-id="c48c8-139">long</span></span> | <span data-ttu-id="c48c8-140">0</span><span class="sxs-lookup"><span data-stu-id="c48c8-140">0</span></span>       | <span data-ttu-id="c48c8-141">Coordenada y del subrectángulo en el origen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c48c8-141">The y-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="c48c8-142">SrcWidth</span><span class="sxs-lookup"><span data-stu-id="c48c8-142">SrcWidth</span></span>   | <span data-ttu-id="c48c8-143">long</span><span class="sxs-lookup"><span data-stu-id="c48c8-143">long</span></span> | <span data-ttu-id="c48c8-144">0</span><span class="sxs-lookup"><span data-stu-id="c48c8-144">0</span></span>       | <span data-ttu-id="c48c8-145">Ancho del subrectángulo en el origen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c48c8-145">The width of the subrectangle on the source, in pixels.</span></span>        |
| <span data-ttu-id="c48c8-146">Ancho</span><span class="sxs-lookup"><span data-stu-id="c48c8-146">Width</span></span>      | <span data-ttu-id="c48c8-147">long</span><span class="sxs-lookup"><span data-stu-id="c48c8-147">long</span></span> | <span data-ttu-id="c48c8-148">0</span><span class="sxs-lookup"><span data-stu-id="c48c8-148">0</span></span>       | <span data-ttu-id="c48c8-149">Ancho del rectángulo de destino, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c48c8-149">Width of the target rectangle, in pixels.</span></span>                      |



 

<span data-ttu-id="c48c8-150">En el diagrama siguiente se muestran estas propiedades:</span><span class="sxs-lookup"><span data-stu-id="c48c8-150">The following diagram illustrates these properties:</span></span>

![propiedades de compositor](images/compmeasure.png)

## <a name="related-topics"></a><span data-ttu-id="c48c8-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c48c8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c48c8-153">Transiciones y efectos</span><span class="sxs-lookup"><span data-stu-id="c48c8-153">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> </dl>

 

 



