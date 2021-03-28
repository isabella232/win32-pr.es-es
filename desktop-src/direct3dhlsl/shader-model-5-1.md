---
title: Modelo de sombreador 5,1
description: Esta sección contiene las páginas de referencia del modelo de sombreador HLSL 5,1, introducidos con D3D12.
ms.assetid: 814FAC95-7FD5-450F-964B-18E687DBCC56
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5fd2f2a2f4ebe86a090ebade8ebf8a033a7c612
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996892"
---
# <a name="shader-model-51"></a><span data-ttu-id="05ad8-103">Modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="05ad8-103">Shader Model 5.1</span></span>

<span data-ttu-id="05ad8-104">Esta sección contiene las páginas de referencia del modelo de sombreador HLSL 5,1, introducidos con D3D12.</span><span class="sxs-lookup"><span data-stu-id="05ad8-104">This section contains the reference pages for HLSL Shader Model 5.1, introduced with D3D12.</span></span>

<span data-ttu-id="05ad8-105">El modelo de sombreador 5,1 es funcionalmente muy similar al [modelo de sombreador 5](d3d11-graphics-reference-sm5.md), el cambio principal es más flexible en la selección de recursos, ya que permite la indexación de matrices de descriptores dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="05ad8-105">Shader Model 5.1 is functionally very similar to [Shader Model 5](d3d11-graphics-reference-sm5.md), the main change is more flexibility in resource selection by allowing indexing of arrays of descriptors from within a shader.</span></span>



| <span data-ttu-id="05ad8-106">Característica</span><span class="sxs-lookup"><span data-stu-id="05ad8-106">Feature</span></span>                   | <span data-ttu-id="05ad8-107">Funcionalidad</span><span class="sxs-lookup"><span data-stu-id="05ad8-107">Capability</span></span>                                                                |
|---------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="05ad8-108">Conjunto de instrucciones</span><span class="sxs-lookup"><span data-stu-id="05ad8-108">Instruction Set</span></span>           | [<span data-ttu-id="05ad8-109">**Funciones intrínsecas de HLSL**</span><span class="sxs-lookup"><span data-stu-id="05ad8-109">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)  |
| <span data-ttu-id="05ad8-110">Sombreador de vértices máximo</span><span class="sxs-lookup"><span data-stu-id="05ad8-110">Vertex Shader Max</span></span>         | <span data-ttu-id="05ad8-111">Sin restricción</span><span class="sxs-lookup"><span data-stu-id="05ad8-111">No restriction</span></span>                                                            |
| <span data-ttu-id="05ad8-112">Sombreador de píxeles máximo</span><span class="sxs-lookup"><span data-stu-id="05ad8-112">Pixel Shader Max</span></span>          | <span data-ttu-id="05ad8-113">Sin restricción</span><span class="sxs-lookup"><span data-stu-id="05ad8-113">No restriction</span></span>                                                            |
| <span data-ttu-id="05ad8-114">Nuevos perfiles de sombreador agregados</span><span class="sxs-lookup"><span data-stu-id="05ad8-114">New Shader Profiles Added</span></span> | <span data-ttu-id="05ad8-115">CS \_ 5 \_ 1, DS \_ 5 \_ 1, GS \_ 5 \_ 1, HS \_ 5 \_ 1, PS \_ 5 \_ 1, vs \_ 5 \_ 1, rootsig \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="05ad8-115">cs\_5\_1, ds\_5\_1, gs\_5\_1, hs\_5\_1, ps\_5\_1, vs\_5\_1, rootsig\_1\_0</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="05ad8-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="05ad8-116">In this section</span></span>



| <span data-ttu-id="05ad8-117">Tema</span><span class="sxs-lookup"><span data-stu-id="05ad8-117">Topic</span></span>                                                                           | <span data-ttu-id="05ad8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="05ad8-118">Description</span></span>                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="05ad8-119">Objetos del modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="05ad8-119">Shader Model 5.1 Objects</span></span>](shader-model-5-1-objects.md)<br/>             | <span data-ttu-id="05ad8-120">Se han agregado los siguientes objetos al modelo de sombreador 5,1.</span><span class="sxs-lookup"><span data-stu-id="05ad8-120">The following objects have been added to shader model 5.1.</span></span><br/> |
| [<span data-ttu-id="05ad8-121">Modelo de sombreador 5,1 valores del sistema</span><span class="sxs-lookup"><span data-stu-id="05ad8-121">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)<br/> | <span data-ttu-id="05ad8-122">El modelo de sombreador 5,1 agrega los siguientes valores del sistema nuevos.</span><span class="sxs-lookup"><span data-stu-id="05ad8-122">Shader Model 5.1 adds the following new system values.</span></span><br/>     |



 

## <a name="related-topics"></a><span data-ttu-id="05ad8-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05ad8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05ad8-124">Modelos de sombreador frente a perfiles de sombreador</span><span class="sxs-lookup"><span data-stu-id="05ad8-124">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> <dt>

[<span data-ttu-id="05ad8-125">Características del modelo de sombreador de HLSL 5,1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="05ad8-125">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 





