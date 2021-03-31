---
title: Asignación entre declaraciones de D3D9 y D3D8
description: En esta tabla se asignan miembros de una declaración de D3DVERTEXELEMENT9 a una declaración de Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805312"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a><span data-ttu-id="df695-103">Asignación entre declaraciones de D3D9 y D3D8</span><span class="sxs-lookup"><span data-stu-id="df695-103">Map between D3D9 and D3D8 declarations</span></span>

<span data-ttu-id="df695-104">En esta tabla se asignan miembros de una declaración de [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) a una declaración de Direct3D 8.</span><span class="sxs-lookup"><span data-stu-id="df695-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a Direct3D 8 declaration.</span></span>



| <span data-ttu-id="df695-105">Uso de Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="df695-105">Direct3D 9 Usage</span></span>           | <span data-ttu-id="df695-106">Índice de uso de Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="df695-106">Direct3D 9 Usage index</span></span> | <span data-ttu-id="df695-107">Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="df695-107">Direct3D 8</span></span>            |
|----------------------------|------------------------|-----------------------|
| <span data-ttu-id="df695-108">\_Posición D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="df695-108">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="df695-109">0</span><span class="sxs-lookup"><span data-stu-id="df695-109">0</span></span>                      | <span data-ttu-id="df695-110">\_Posición D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="df695-110">D3DVSDE\_POSITION</span></span>     |
| <span data-ttu-id="df695-111">\_Posición D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="df695-111">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="df695-112">1</span><span class="sxs-lookup"><span data-stu-id="df695-112">1</span></span>                      | <span data-ttu-id="df695-113">D3DVSDE \_ POSITION2</span><span class="sxs-lookup"><span data-stu-id="df695-113">D3DVSDE\_POSITION2</span></span>    |
| <span data-ttu-id="df695-114">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="df695-114">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="df695-115">0</span><span class="sxs-lookup"><span data-stu-id="df695-115">0</span></span>                      | <span data-ttu-id="df695-116">D3DVSDE \_ normal</span><span class="sxs-lookup"><span data-stu-id="df695-116">D3DVSDE\_NORMAL</span></span>       |
| <span data-ttu-id="df695-117">D3DDECLUSAGE \_ normal</span><span class="sxs-lookup"><span data-stu-id="df695-117">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="df695-118">1</span><span class="sxs-lookup"><span data-stu-id="df695-118">1</span></span>                      | <span data-ttu-id="df695-119">D3DVSDE \_ NORMAL2</span><span class="sxs-lookup"><span data-stu-id="df695-119">D3DVSDE\_NORMAL2</span></span>      |
| <span data-ttu-id="df695-120">D3DDECLUSAGE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="df695-120">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="df695-121">0</span><span class="sxs-lookup"><span data-stu-id="df695-121">0</span></span>                      | <span data-ttu-id="df695-122">D3DVSDE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="df695-122">D3DVSDE\_BLENDWEIGHT</span></span>  |
| <span data-ttu-id="df695-123">D3DDECLUSAGE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="df695-123">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="df695-124">0</span><span class="sxs-lookup"><span data-stu-id="df695-124">0</span></span>                      | <span data-ttu-id="df695-125">D3DVSDE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="df695-125">D3DVSDE\_BLENDINDICES</span></span> |
| <span data-ttu-id="df695-126">D3DDECLUSAGE \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="df695-126">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="df695-127">0</span><span class="sxs-lookup"><span data-stu-id="df695-127">0</span></span>                      | <span data-ttu-id="df695-128">D3DVSDE \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="df695-128">D3DVSDE\_PSIZE</span></span>        |
| <span data-ttu-id="df695-129">COLOR de D3DDECLUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="df695-129">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="df695-130">0</span><span class="sxs-lookup"><span data-stu-id="df695-130">0</span></span>                      | <span data-ttu-id="df695-131">\_Difusión D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="df695-131">D3DVSDE\_DIFFUSE</span></span>      |
| <span data-ttu-id="df695-132">COLOR de D3DDECLUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="df695-132">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="df695-133">1</span><span class="sxs-lookup"><span data-stu-id="df695-133">1</span></span>                      | <span data-ttu-id="df695-134">\_Reflejo D3DVSDE</span><span class="sxs-lookup"><span data-stu-id="df695-134">D3DVSDE\_SPECULAR</span></span>     |
| <span data-ttu-id="df695-135">D3DDECLUSAGE \_ TEXCOORD</span><span class="sxs-lookup"><span data-stu-id="df695-135">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="df695-136">n</span><span class="sxs-lookup"><span data-stu-id="df695-136">n</span></span>                      | <span data-ttu-id="df695-137">D3DVSDE \_ TEXCOORDn</span><span class="sxs-lookup"><span data-stu-id="df695-137">D3DVSDE\_TEXCOORDn</span></span>    |



 

<span data-ttu-id="df695-138">Cuando se usa una declaración con el procesamiento de vértices de hardware en un controlador de Direct3D 7, el tiempo de ejecución de Direct3D lo convierte en un FVF con las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="df695-138">When a declaration is used with hardware vertex processing on a Direct3D 7 driver, the Direct3D runtime converts it to a FVF with the following rules:</span></span>

-   <span data-ttu-id="df695-139">Solo se debe usar Stream 0 (evidente desde el extremo MaxStreams).</span><span class="sxs-lookup"><span data-stu-id="df695-139">Only stream 0 should be used (evident from the MaxStreams cap).</span></span>
-   <span data-ttu-id="df695-140">El orden de los elementos de vértice debe ser el mismo que el orden de los bits de FVF.</span><span class="sxs-lookup"><span data-stu-id="df695-140">The order of vertex elements should be the same as order of FVF bits.</span></span>
-   <span data-ttu-id="df695-141">No se permiten espacios en las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="df695-141">Gaps in texture coordinates are not allowed.</span></span>
-   <span data-ttu-id="df695-142">Cualquier elemento de vértice no descrito en la tabla no se puede convertir en un FVF válido para todos los controladores anteriores a DirectX 8 y, por lo tanto, no se puede usar en esos controladores.</span><span class="sxs-lookup"><span data-stu-id="df695-142">Any vertex element not described the table cannot be converted into a valid FVF for all pre-DirectX 8 drivers and, hence, cannot be used on those drivers.</span></span>
-   <span data-ttu-id="df695-143">Solo \_ se permite D3DDECLTYPE FLOAT2 para los elementos de vértice con D3DDECLUSAGE \_ TEXCOORD si el dispositivo no establece ninguno de los límites de D3DPTEXTURECAPS \_ previsto o D3DPTEXTURECAPS \_ mapa.</span><span class="sxs-lookup"><span data-stu-id="df695-143">Only D3DDECLTYPE\_FLOAT2 is allowed for vertex elements with D3DDECLUSAGE\_TEXCOORD if device does not set either of the D3DPTEXTURECAPS\_PROJECTED or D3DPTEXTURECAPS\_CUBEMAP caps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df695-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df695-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df695-145">Declaración de vértice</span><span class="sxs-lookup"><span data-stu-id="df695-145">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



