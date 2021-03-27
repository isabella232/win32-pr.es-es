---
title: AppendStructuredBuffer
description: Búfer de salida que aparece como un flujo al que el sombreador puede anexar. Solo los búferes estructurados pueden tomar tipos T que son estructuras.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- HLSL de AppendStructuredBuffer
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792291"
---
# <a name="appendstructuredbuffer"></a><span data-ttu-id="3c738-105">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="3c738-105">AppendStructuredBuffer</span></span>

<span data-ttu-id="3c738-106">Búfer de salida que aparece como un flujo al que el sombreador puede anexar.</span><span class="sxs-lookup"><span data-stu-id="3c738-106">Output buffer that appears as a stream the shader may append to.</span></span> <span data-ttu-id="3c738-107">Solo los búferes estructurados pueden tomar tipos T que son estructuras.</span><span class="sxs-lookup"><span data-stu-id="3c738-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="3c738-108">Método</span><span class="sxs-lookup"><span data-stu-id="3c738-108">Method</span></span>                                                                   | <span data-ttu-id="3c738-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c738-109">Description</span></span>                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="3c738-110">**Append**</span><span class="sxs-lookup"><span data-stu-id="3c738-110">**Append**</span></span>](sm5-object-appendstructuredbuffer-append.md)               | <span data-ttu-id="3c738-111">Anexa un valor al final del búfer.</span><span class="sxs-lookup"><span data-stu-id="3c738-111">Appends a value to the end of the buffer.</span></span> |
| [<span data-ttu-id="3c738-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="3c738-112">**GetDimensions**</span></span>](sm5-object-appendstructuredbuffer-getdimensions.md) | <span data-ttu-id="3c738-113">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c738-113">Gets the resource dimensions.</span></span>             |



 

<span data-ttu-id="3c738-114">El formato UAV enlazado a este recurso debe crearse con el formato de DXGI \_ \_ desconocido.</span><span class="sxs-lookup"><span data-stu-id="3c738-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="3c738-115">El UAV enlazado a este recurso se debe haber creado con la [**marca de D3D11 del \_ búfer \_ UAV \_ \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="3c738-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="3c738-116">Para obtener más información sobre un búfer estructurado append, vea ambas secciones: [Append y consume](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer y [buffer estructurado](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="3c738-116">For more information about an append structured buffer, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="3c738-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="3c738-117">Minimum Shader Model</span></span>

<span data-ttu-id="3c738-118">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3c738-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="3c738-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="3c738-119">Shader Model</span></span>                                                                | <span data-ttu-id="3c738-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="3c738-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3c738-121">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="3c738-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="3c738-122">sí</span><span class="sxs-lookup"><span data-stu-id="3c738-122">yes</span></span>       |



 

<span data-ttu-id="3c738-123">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3c738-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3c738-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="3c738-124">Vertex</span></span> | <span data-ttu-id="3c738-125">Casco</span><span class="sxs-lookup"><span data-stu-id="3c738-125">Hull</span></span> | <span data-ttu-id="3c738-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="3c738-126">Domain</span></span> | <span data-ttu-id="3c738-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="3c738-127">Geometry</span></span> | <span data-ttu-id="3c738-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="3c738-128">Pixel</span></span> | <span data-ttu-id="3c738-129">Compute</span><span class="sxs-lookup"><span data-stu-id="3c738-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3c738-130">x</span><span class="sxs-lookup"><span data-stu-id="3c738-130">x</span></span>     | <span data-ttu-id="3c738-131">x</span><span class="sxs-lookup"><span data-stu-id="3c738-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3c738-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c738-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c738-133">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3c738-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 