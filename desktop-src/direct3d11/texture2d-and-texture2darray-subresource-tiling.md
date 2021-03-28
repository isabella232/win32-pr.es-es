---
title: Mosaico de subrecurso Texture2D y Texture2DArray
description: En estas tablas se muestra cómo se muestran los Subrecursos Texture2D y Texture2DArray en mosaico.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421041"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a><span data-ttu-id="d21f7-103">Mosaico de subrecurso Texture2D y Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d21f7-103">Texture2D and Texture2DArray subresource tiling</span></span>

<span data-ttu-id="d21f7-104">En estas tablas se muestra cómo se muestran los Subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) en mosaico.</span><span class="sxs-lookup"><span data-stu-id="d21f7-104">These tables show how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources are tiled.</span></span> <span data-ttu-id="d21f7-105">Los valores de estas tablas no cuentan el empaquetado de la cola MIP.</span><span class="sxs-lookup"><span data-stu-id="d21f7-105">The values in these tables don't count tail mip packing.</span></span>

<span data-ttu-id="d21f7-106">En esta tabla se muestra cómo se muestran en mosaico los Subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con recuentos Multimuestra de 1.</span><span class="sxs-lookup"><span data-stu-id="d21f7-106">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with multisample counts of 1 are tiled.</span></span>



| <span data-ttu-id="d21f7-107">Bits/píxel (1 ejemplo/píxel)</span><span class="sxs-lookup"><span data-stu-id="d21f7-107">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="d21f7-108">Dimensiones del mosaico (píxeles, WxH)</span><span class="sxs-lookup"><span data-stu-id="d21f7-108">Tile Dimensions (Pixels, WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="d21f7-109">8</span><span class="sxs-lookup"><span data-stu-id="d21f7-109">8</span></span>                           | <span data-ttu-id="d21f7-110">256x256</span><span class="sxs-lookup"><span data-stu-id="d21f7-110">256x256</span></span>                       |
| <span data-ttu-id="d21f7-111">16</span><span class="sxs-lookup"><span data-stu-id="d21f7-111">16</span></span>                          | <span data-ttu-id="d21f7-112">256x128</span><span class="sxs-lookup"><span data-stu-id="d21f7-112">256x128</span></span>                       |
| <span data-ttu-id="d21f7-113">32</span><span class="sxs-lookup"><span data-stu-id="d21f7-113">32</span></span>                          | <span data-ttu-id="d21f7-114">128x128</span><span class="sxs-lookup"><span data-stu-id="d21f7-114">128x128</span></span>                       |
| <span data-ttu-id="d21f7-115">64</span><span class="sxs-lookup"><span data-stu-id="d21f7-115">64</span></span>                          | <span data-ttu-id="d21f7-116">128x64</span><span class="sxs-lookup"><span data-stu-id="d21f7-116">128x64</span></span>                        |
| <span data-ttu-id="d21f7-117">128</span><span class="sxs-lookup"><span data-stu-id="d21f7-117">128</span></span>                         | <span data-ttu-id="d21f7-118">64x64</span><span class="sxs-lookup"><span data-stu-id="d21f7-118">64x64</span></span>                         |
| <span data-ttu-id="d21f7-119">BC1, 4</span><span class="sxs-lookup"><span data-stu-id="d21f7-119">BC1,4</span></span>                       | <span data-ttu-id="d21f7-120">512x256</span><span class="sxs-lookup"><span data-stu-id="d21f7-120">512x256</span></span>                       |
| <span data-ttu-id="d21f7-121">BC2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="d21f7-121">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="d21f7-122">256x256</span><span class="sxs-lookup"><span data-stu-id="d21f7-122">256x256</span></span>                       |



 

<span data-ttu-id="d21f7-123">Los recuentos de bits de formato no admitidos con los recursos en mosaico son formatos de 96 BPP, formatos de vídeo, formato de DXGI \_ \_ R1 \_ UNORM, formato de dxgi \_ \_ R8G8 \_ B8G8 \_ UNORM y formato de dxgi \_ \_ R8R8 \_ \_ G8B8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="d21f7-123">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="d21f7-124">En esta tabla se muestra cómo se muestran en mosaico los Subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con varios recuentos de muestras.</span><span class="sxs-lookup"><span data-stu-id="d21f7-124">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with various multisample counts are tiled.</span></span>



| <span data-ttu-id="d21f7-125">Recuento de muestras Multimuestra</span><span class="sxs-lookup"><span data-stu-id="d21f7-125">Multisample Count</span></span>           | <span data-ttu-id="d21f7-126">Dividir las dimensiones del mosaico por encima de (WxH)</span><span class="sxs-lookup"><span data-stu-id="d21f7-126">Divide Tile Dimensions Above by (WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="d21f7-127">1</span><span class="sxs-lookup"><span data-stu-id="d21f7-127">1</span></span>                           | <span data-ttu-id="d21f7-128">asesoramiento</span><span class="sxs-lookup"><span data-stu-id="d21f7-128">1x1</span></span>                           |
| <span data-ttu-id="d21f7-129">2</span><span class="sxs-lookup"><span data-stu-id="d21f7-129">2</span></span>                           | <span data-ttu-id="d21f7-130">2x1</span><span class="sxs-lookup"><span data-stu-id="d21f7-130">2x1</span></span>                           |
| <span data-ttu-id="d21f7-131">4</span><span class="sxs-lookup"><span data-stu-id="d21f7-131">4</span></span>                           | <span data-ttu-id="d21f7-132">2x2</span><span class="sxs-lookup"><span data-stu-id="d21f7-132">2x2</span></span>                           |
| <span data-ttu-id="d21f7-133">8</span><span class="sxs-lookup"><span data-stu-id="d21f7-133">8</span></span>                           | <span data-ttu-id="d21f7-134">4 TB</span><span class="sxs-lookup"><span data-stu-id="d21f7-134">4x2</span></span>                           |
| <span data-ttu-id="d21f7-135">16</span><span class="sxs-lookup"><span data-stu-id="d21f7-135">16</span></span>                          | <span data-ttu-id="d21f7-136">4 x 4</span><span class="sxs-lookup"><span data-stu-id="d21f7-136">4x4</span></span>                           |



 

<span data-ttu-id="d21f7-137">Solo se requieren (y se permiten) los recuentos de muestras 1 y 4 para que se admitan con recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="d21f7-137">Only sample counts 1 and 4 are required (and allowed) to be supported with tiled resources.</span></span> <span data-ttu-id="d21f7-138">Los recursos en mosaico no admiten actualmente 2, 8 y 16 aunque se muestren.</span><span class="sxs-lookup"><span data-stu-id="d21f7-138">Tiled resources don't currently support 2, 8, and 16 even though they are shown.</span></span>

<span data-ttu-id="d21f7-139">Las implementaciones pueden optar por admitir el modo 2, 8 o 16 de ejemplo de suavizado de contorno de muestreo múltiple (MSAA) para los recursos no en mosaico, aunque los recursos en mosaico no los admitan.</span><span class="sxs-lookup"><span data-stu-id="d21f7-139">Implementations can choose to support 2, 8, and/or 16 sample multisample antialiasing (MSAA) mode for non-tiled resources even though tiled resource don't support them.</span></span>

<span data-ttu-id="d21f7-140">Los recursos en mosaico con recuentos de muestras mayores que 1 no pueden usar formatos de 128 BPP.</span><span class="sxs-lookup"><span data-stu-id="d21f7-140">Tiled resources with sample counts larger than 1 can't use 128 bpp formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d21f7-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d21f7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d21f7-142">Cómo se organiza en mosaico el área de un recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="d21f7-142">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 