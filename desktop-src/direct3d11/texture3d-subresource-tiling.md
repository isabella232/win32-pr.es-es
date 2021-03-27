---
title: Mosaico de subrecurso Texture3D
description: En esta tabla se muestra cómo se muestran los Subrecursos de Texture3D en mosaico.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997169"
---
# <a name="texture3d-subresource-tiling"></a><span data-ttu-id="0da08-103">Mosaico de subrecurso Texture3D</span><span class="sxs-lookup"><span data-stu-id="0da08-103">Texture3D subresource tiling</span></span>

<span data-ttu-id="0da08-104">En esta tabla se muestra cómo se muestran los Subrecursos de [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) en mosaico.</span><span class="sxs-lookup"><span data-stu-id="0da08-104">This table shows how [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) subresources are tiled.</span></span> <span data-ttu-id="0da08-105">Los valores de esta tabla no cuentan el empaquetado de la cola MIP.</span><span class="sxs-lookup"><span data-stu-id="0da08-105">The values in this table don't count tail mip packing.</span></span>

<span data-ttu-id="0da08-106">En esta tabla se toma el mosaico [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y se dividen las dimensiones x/y en 4 cada una de ellas y se agregan 16 niveles de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0da08-106">This table takes the [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) tiling and divides the x/y dimensions by 4 each and adds 16 layers of depth.</span></span> <span data-ttu-id="0da08-107">Todos los mosaicos para el primer plano (plano 2D de mosaicos que definen las 16 primeras capas de profundidad) aparecen antes que los planos posteriores.</span><span class="sxs-lookup"><span data-stu-id="0da08-107">All the tiles for the first plane (2D plane of tiles defining the first 16 layers of depth) appear before the subsequent planes.</span></span>

> [!Note]  
> <span data-ttu-id="0da08-108">La compatibilidad con [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) en recursos en mosaico no se expone en la implementación inicial de los recursos en mosaico, pero las formas de iconos deseadas se enumeran aquí porque es posible que se tenga en cuenta la compatibilidad en una versión futura.</span><span class="sxs-lookup"><span data-stu-id="0da08-108">[**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) support in tiled resources isn't exposed in the initial implementation of tiled resources, but the desired tile shapes are listed here because support might be consideration in a future release.</span></span>

 



| <span data-ttu-id="0da08-109">Bits/píxel (1 ejemplo/píxel)</span><span class="sxs-lookup"><span data-stu-id="0da08-109">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="0da08-110">Dimensiones del mosaico (píxeles, a la x)</span><span class="sxs-lookup"><span data-stu-id="0da08-110">Tile Dimensions (Pixels, WxHxD)</span></span> |
|-----------------------------|---------------------------------|
| <span data-ttu-id="0da08-111">8</span><span class="sxs-lookup"><span data-stu-id="0da08-111">8</span></span>                           | <span data-ttu-id="0da08-112">64x32x32</span><span class="sxs-lookup"><span data-stu-id="0da08-112">64x32x32</span></span>                        |
| <span data-ttu-id="0da08-113">16</span><span class="sxs-lookup"><span data-stu-id="0da08-113">16</span></span>                          | <span data-ttu-id="0da08-114">32x32x32</span><span class="sxs-lookup"><span data-stu-id="0da08-114">32x32x32</span></span>                        |
| <span data-ttu-id="0da08-115">32</span><span class="sxs-lookup"><span data-stu-id="0da08-115">32</span></span>                          | <span data-ttu-id="0da08-116">32x32x16</span><span class="sxs-lookup"><span data-stu-id="0da08-116">32x32x16</span></span>                        |
| <span data-ttu-id="0da08-117">64</span><span class="sxs-lookup"><span data-stu-id="0da08-117">64</span></span>                          | <span data-ttu-id="0da08-118">32x16x16</span><span class="sxs-lookup"><span data-stu-id="0da08-118">32x16x16</span></span>                        |
| <span data-ttu-id="0da08-119">128</span><span class="sxs-lookup"><span data-stu-id="0da08-119">128</span></span>                         | <span data-ttu-id="0da08-120">16x16x16</span><span class="sxs-lookup"><span data-stu-id="0da08-120">16x16x16</span></span>                        |
| <span data-ttu-id="0da08-121">BC1, 4</span><span class="sxs-lookup"><span data-stu-id="0da08-121">BC1,4</span></span>                       | <span data-ttu-id="0da08-122">128x64x16</span><span class="sxs-lookup"><span data-stu-id="0da08-122">128x64x16</span></span>                       |
| <span data-ttu-id="0da08-123">BC2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="0da08-123">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="0da08-124">64x64x16</span><span class="sxs-lookup"><span data-stu-id="0da08-124">64x64x16</span></span>                        |



 

<span data-ttu-id="0da08-125">Los recuentos de bits de formato no admitidos con los recursos en mosaico son formatos de 96 BPP, formatos de vídeo, formato de DXGI \_ \_ R1 \_ UNORM, formato de dxgi \_ \_ R8G8 \_ B8G8 \_ UNORM y formato de dxgi \_ \_ R8R8 \_ \_ G8B8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="0da08-125">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0da08-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0da08-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0da08-127">Cómo se organiza en mosaico el área de un recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="0da08-127">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 