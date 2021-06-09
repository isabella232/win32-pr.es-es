---
title: Objetos del modelo de sombreador 5.1
description: Los siguientes objetos se han agregado al modelo de sombreador 5.1.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376ce272e789501e21f5866be37f56daf31bc829
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825722"
---
# <a name="shader-model-51-objects"></a><span data-ttu-id="342e4-103">Objetos del modelo de sombreador 5.1</span><span class="sxs-lookup"><span data-stu-id="342e4-103">Shader Model 5.1 Objects</span></span>

<span data-ttu-id="342e4-104">Los siguientes objetos se han agregado al modelo de sombreador 5.1.</span><span class="sxs-lookup"><span data-stu-id="342e4-104">The following objects have been added to shader model 5.1.</span></span>

<span data-ttu-id="342e4-105">Para las vistas de [orden de rasterizador](/windows/desktop/direct3d11/rasterizer-order-views) (disponibles en D3D11.3 y D3D12), los objetos siguientes son nuevos y solo se permiten en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="342e4-105">For the [Rasterizer Order Views](/windows/desktop/direct3d11/rasterizer-order-views) (available in D3D11.3 and D3D12), the following objects are new, and are only allowed in the pixel shader.</span></span> <span data-ttu-id="342e4-106">Tenga en cuenta que los métodos que admiten son idénticos a los objetos UAV correspondientes.</span><span class="sxs-lookup"><span data-stu-id="342e4-106">Note that the methods they support are identical to the corresponding UAV objects.</span></span>



| <span data-ttu-id="342e4-107">Objeto Rasterizer</span><span class="sxs-lookup"><span data-stu-id="342e4-107">Rasterizer object</span></span>                                   | <span data-ttu-id="342e4-108">Objeto UAV</span><span class="sxs-lookup"><span data-stu-id="342e4-108">UAV object</span></span>                                                              |
|------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="342e4-109">RasterizerOrderedBuffer</span><span class="sxs-lookup"><span data-stu-id="342e4-109">RasterizerOrderedBuffer</span></span>            | [<span data-ttu-id="342e4-110">**RWBuffer**</span><span class="sxs-lookup"><span data-stu-id="342e4-110">**RWBuffer**</span></span>](sm5-object-rwbuffer.md)                       |
| <span data-ttu-id="342e4-111">RasterizerOrderedByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="342e4-111">RasterizerOrderedByteAddressBuffer</span></span> | [<span data-ttu-id="342e4-112">**RWByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="342e4-112">**RWByteAddressBuffer**</span></span>](sm5-object-rwbyteaddressbuffer.md) |
| <span data-ttu-id="342e4-113">RasterizerOrderedStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="342e4-113">RasterizerOrderedStructuredBuffer</span></span>  | [<span data-ttu-id="342e4-114">**RWStructuredBuffer**</span><span class="sxs-lookup"><span data-stu-id="342e4-114">**RWStructuredBuffer**</span></span>](sm5-object-rwstructuredbuffer.md)   |
| <span data-ttu-id="342e4-115">RasterizerOrderedTexture1D</span><span class="sxs-lookup"><span data-stu-id="342e4-115">RasterizerOrderedTexture1D</span></span>         | [<span data-ttu-id="342e4-116">**RWTexture1D**</span><span class="sxs-lookup"><span data-stu-id="342e4-116">**RWTexture1D**</span></span>](sm5-object-rwtexture1d.md)                 |
| <span data-ttu-id="342e4-117">RasterizerOrderedTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="342e4-117">RasterizerOrderedTexture1DArray</span></span>    | [<span data-ttu-id="342e4-118">**RWTexture1DArray**</span><span class="sxs-lookup"><span data-stu-id="342e4-118">**RWTexture1DArray**</span></span>](sm5-object-rwtexture1darray.md)       |
| <span data-ttu-id="342e4-119">RasterizerOrderedTexture2D</span><span class="sxs-lookup"><span data-stu-id="342e4-119">RasterizerOrderedTexture2D</span></span>         | [<span data-ttu-id="342e4-120">**RWTexture2D**</span><span class="sxs-lookup"><span data-stu-id="342e4-120">**RWTexture2D**</span></span>](sm5-object-rwtexture2d.md)                 |
| <span data-ttu-id="342e4-121">RasterizerOrderedTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="342e4-121">RasterizerOrderedTexture2DArray</span></span>    | [<span data-ttu-id="342e4-122">**RWTexture2DArray**</span><span class="sxs-lookup"><span data-stu-id="342e4-122">**RWTexture2DArray**</span></span>](sm5-object-rwtexture2darray.md)       |
| <span data-ttu-id="342e4-123">RasterizerOrderedTexture3D</span><span class="sxs-lookup"><span data-stu-id="342e4-123">RasterizerOrderedTexture3D</span></span>         | [<span data-ttu-id="342e4-124">**RWTexture3D**</span><span class="sxs-lookup"><span data-stu-id="342e4-124">**RWTexture3D**</span></span>](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="342e4-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="342e4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="342e4-126">Modelo de sombreador 5.1</span><span class="sxs-lookup"><span data-stu-id="342e4-126">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> <dt>

[<span data-ttu-id="342e4-127">Características del modelo de sombreador HLSL 5.1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="342e4-127">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
