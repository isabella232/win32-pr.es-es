---
description: Constantes de generación de mapas normales.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4263237cedf92a5e322f2fe139e9afe2297f6b9b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342860"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="d32d0-103">D3DX \_ NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="d32d0-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="d32d0-104">Constantes de generación de mapas normales.</span><span class="sxs-lookup"><span data-stu-id="d32d0-104">Normal maps generation constants.</span></span>



| <span data-ttu-id="d32d0-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="d32d0-105">\#define</span></span>                            | <span data-ttu-id="d32d0-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d32d0-106">Description</span></span>                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d32d0-107">D3DX \_ NORMALMAP \_ MIRROR \_ U</span><span class="sxs-lookup"><span data-stu-id="d32d0-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="d32d0-108">Indica que los píxeles del borde de la textura en el eje u deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="d32d0-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="d32d0-109">D3DX \_ NORMALMAP \_ MIRROR \_ V</span><span class="sxs-lookup"><span data-stu-id="d32d0-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="d32d0-110">Indica que los píxeles del borde de la textura del eje v deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="d32d0-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="d32d0-111">D3DX \_ NORMALMAP \_ MIRROR</span><span class="sxs-lookup"><span data-stu-id="d32d0-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="d32d0-112">Igual que especificar D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.</span><span class="sxs-lookup"><span data-stu-id="d32d0-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="d32d0-113">D3DX \_ NORMALMAP \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="d32d0-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="d32d0-114">Invierte la dirección de cada normal.</span><span class="sxs-lookup"><span data-stu-id="d32d0-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d32d0-115">\_OCLUSIÓN DE PROCESO DE D3DX NORMALMAP \_ \_</span><span class="sxs-lookup"><span data-stu-id="d32d0-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="d32d0-116">Calcula el término de oclusión por píxel y lo codifica en el alfa.</span><span class="sxs-lookup"><span data-stu-id="d32d0-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="d32d0-117">Un alfa de 1 significa que el píxel no se oculta de ninguna manera, y un alfa de 0 significa que el píxel está completamente oculto.</span><span class="sxs-lookup"><span data-stu-id="d32d0-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="d32d0-118">Información constante</span><span class="sxs-lookup"><span data-stu-id="d32d0-118">Constant Information</span></span>



| <span data-ttu-id="d32d0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d32d0-119">Requirement</span></span>                         | <span data-ttu-id="d32d0-120">Value</span><span class="sxs-lookup"><span data-stu-id="d32d0-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="d32d0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d32d0-121">Header</span></span>                   | <span data-ttu-id="d32d0-122">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="d32d0-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="d32d0-123">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="d32d0-123">Minimum operating system</span></span> | <span data-ttu-id="d32d0-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d32d0-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d32d0-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d32d0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d32d0-126">Constantes D3DX</span><span class="sxs-lookup"><span data-stu-id="d32d0-126">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="d32d0-127">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="d32d0-127">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



