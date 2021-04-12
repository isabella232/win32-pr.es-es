---
description: En esta tabla se asignan miembros de una declaración de D3DVERTEXELEMENT9 a un código de FVF.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Asignación entre una declaración de Direct3D y códigos de FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152322"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a><span data-ttu-id="0167c-103">Asignación entre una declaración de Direct3D y códigos de FVF (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0167c-103">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="0167c-104">En esta tabla se asignan miembros de una declaración de [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) a un código de FVF.</span><span class="sxs-lookup"><span data-stu-id="0167c-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a FVF code.</span></span>



| <span data-ttu-id="0167c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0167c-105">Data type</span></span>             | <span data-ttu-id="0167c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="0167c-106">Usage</span></span>                      | <span data-ttu-id="0167c-107">Índice de uso</span><span class="sxs-lookup"><span data-stu-id="0167c-107">Usage index</span></span> | <span data-ttu-id="0167c-108">FVF</span><span class="sxs-lookup"><span data-stu-id="0167c-108">FVF</span></span>                       |
|-----------------------|----------------------------|-------------|---------------------------|
| <span data-ttu-id="0167c-109">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="0167c-109">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="0167c-110">\_Posición D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="0167c-110">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="0167c-111">0</span><span class="sxs-lookup"><span data-stu-id="0167c-111">0</span></span>           | <span data-ttu-id="0167c-112">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="0167c-112">D3DFVF\_XYZ</span></span>               |
| <span data-ttu-id="0167c-113">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="0167c-113">D3DDECLTYPE\_FLOAT4</span></span>   | <span data-ttu-id="0167c-114">D3DDECLUSAGE \_ posición</span><span class="sxs-lookup"><span data-stu-id="0167c-114">D3DDECLUSAGE\_POSITIONT</span></span>    | <span data-ttu-id="0167c-115">0</span><span class="sxs-lookup"><span data-stu-id="0167c-115">0</span></span>           | <span data-ttu-id="0167c-116">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="0167c-116">D3DFVF\_XYZRHW</span></span>            |
| <span data-ttu-id="0167c-117">D3DDECLTYPE \_ floatn</span><span class="sxs-lookup"><span data-stu-id="0167c-117">D3DDECLTYPE\_FLOATn</span></span>   | <span data-ttu-id="0167c-118">D3DDECLUSAGE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="0167c-118">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="0167c-119">0</span><span class="sxs-lookup"><span data-stu-id="0167c-119">0</span></span>           | <span data-ttu-id="0167c-120">D3DFVF \_ XYZBn</span><span class="sxs-lookup"><span data-stu-id="0167c-120">D3DFVF\_XYZBn</span></span>             |
| <span data-ttu-id="0167c-121">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="0167c-121">D3DDECLTYPE\_UBYTE4</span></span>   | <span data-ttu-id="0167c-122">D3DDECLUSAGE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="0167c-122">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="0167c-123">0</span><span class="sxs-lookup"><span data-stu-id="0167c-123">0</span></span>           | <span data-ttu-id="0167c-124">D3DFVF \_ XYZB (nWeights + 1)</span><span class="sxs-lookup"><span data-stu-id="0167c-124">D3DFVF\_XYZB (nWeights+1)</span></span> |
| <span data-ttu-id="0167c-125">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="0167c-125">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="0167c-126">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="0167c-126">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="0167c-127">0</span><span class="sxs-lookup"><span data-stu-id="0167c-127">0</span></span>           | <span data-ttu-id="0167c-128">D3DFVF \_ normal</span><span class="sxs-lookup"><span data-stu-id="0167c-128">D3DFVF\_NORMAL</span></span>            |
| <span data-ttu-id="0167c-129">D3DDECLTYPE \_ FLOAT1</span><span class="sxs-lookup"><span data-stu-id="0167c-129">D3DDECLTYPE\_FLOAT1</span></span>   | <span data-ttu-id="0167c-130">D3DDECLUSAGE \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="0167c-130">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="0167c-131">0</span><span class="sxs-lookup"><span data-stu-id="0167c-131">0</span></span>           | <span data-ttu-id="0167c-132">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="0167c-132">D3DFVF\_PSIZE</span></span>             |
| <span data-ttu-id="0167c-133">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="0167c-133">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="0167c-134">COLOR de D3DDECLUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="0167c-134">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="0167c-135">0</span><span class="sxs-lookup"><span data-stu-id="0167c-135">0</span></span>           | <span data-ttu-id="0167c-136">\_Difusión D3DFVF</span><span class="sxs-lookup"><span data-stu-id="0167c-136">D3DFVF\_DIFFUSE</span></span>           |
| <span data-ttu-id="0167c-137">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="0167c-137">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="0167c-138">COLOR de D3DDECLUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="0167c-138">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="0167c-139">1</span><span class="sxs-lookup"><span data-stu-id="0167c-139">1</span></span>           | <span data-ttu-id="0167c-140">\_Reflejo D3DFVF</span><span class="sxs-lookup"><span data-stu-id="0167c-140">D3DFVF\_SPECULAR</span></span>          |
| <span data-ttu-id="0167c-141">D3DDECLTYPE \_ FLOATm</span><span class="sxs-lookup"><span data-stu-id="0167c-141">D3DDECLTYPE\_FLOATm</span></span>   | <span data-ttu-id="0167c-142">D3DDECLUSAGE \_ TEXCOORD</span><span class="sxs-lookup"><span data-stu-id="0167c-142">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="0167c-143">n</span><span class="sxs-lookup"><span data-stu-id="0167c-143">n</span></span>           | <span data-ttu-id="0167c-144">D3DFVF \_ TEXCOORDSIZEm (n)</span><span class="sxs-lookup"><span data-stu-id="0167c-144">D3DFVF\_TEXCOORDSIZEm(n)</span></span>  |
| <span data-ttu-id="0167c-145">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="0167c-145">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="0167c-146">\_Posición D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="0167c-146">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="0167c-147">1</span><span class="sxs-lookup"><span data-stu-id="0167c-147">1</span></span>           | <span data-ttu-id="0167c-148">N/D</span><span class="sxs-lookup"><span data-stu-id="0167c-148">N/A</span></span>                       |
| <span data-ttu-id="0167c-149">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="0167c-149">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="0167c-150">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="0167c-150">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="0167c-151">1</span><span class="sxs-lookup"><span data-stu-id="0167c-151">1</span></span>           | <span data-ttu-id="0167c-152">N/D</span><span class="sxs-lookup"><span data-stu-id="0167c-152">N/A</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="0167c-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0167c-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0167c-154">Declaración de vértice</span><span class="sxs-lookup"><span data-stu-id="0167c-154">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



