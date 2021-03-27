---
title: ConsumeStructuredBuffer
description: Un búfer de entrada que aparece como un flujo del que el sombreador puede extraer valores. Solo los búferes estructurados pueden tomar tipos T que son estructuras.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- HLSL de ConsumeStructuredBuffer
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997165"
---
# <a name="consumestructuredbuffer"></a><span data-ttu-id="62f23-105">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="62f23-105">ConsumeStructuredBuffer</span></span>

<span data-ttu-id="62f23-106">Un búfer de entrada que aparece como un flujo del que el sombreador puede extraer valores.</span><span class="sxs-lookup"><span data-stu-id="62f23-106">An input buffer that appears as a stream the shader may pull values from.</span></span> <span data-ttu-id="62f23-107">Solo los búferes estructurados pueden tomar tipos T que son estructuras.</span><span class="sxs-lookup"><span data-stu-id="62f23-107">Only structured buffers can take T types that are structures.</span></span>



| <span data-ttu-id="62f23-108">Método</span><span class="sxs-lookup"><span data-stu-id="62f23-108">Method</span></span>                                                                    | <span data-ttu-id="62f23-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="62f23-109">Description</span></span>                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="62f23-110">**Consumo**</span><span class="sxs-lookup"><span data-stu-id="62f23-110">**Consume**</span></span>](sm5-object-consumestructuredbuffer-consume.md)             | <span data-ttu-id="62f23-111">Quita un valor del final del búfer.</span><span class="sxs-lookup"><span data-stu-id="62f23-111">Removes a value from the end of the buffer.</span></span> |
| [<span data-ttu-id="62f23-112">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="62f23-112">**GetDimensions**</span></span>](sm5-object-consumestructuredbuffer-getdimensions.md) | <span data-ttu-id="62f23-113">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="62f23-113">Gets the resource dimensions.</span></span>               |



 

<span data-ttu-id="62f23-114">El formato UAV enlazado a este recurso debe crearse con el formato de DXGI \_ \_ desconocido.</span><span class="sxs-lookup"><span data-stu-id="62f23-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="62f23-115">El UAV enlazado a este recurso se debe haber creado con la [**marca de D3D11 del \_ búfer \_ UAV \_ \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="62f23-115">The UAV bound to this resource must have been created with [**D3D11\_BUFFER\_UAV\_FLAG\_APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="62f23-116">Para obtener más información sobre el uso de búferes estructurados, vea ambas secciones: [Append y consume](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer y [buffer estructurado](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="62f23-116">For more info about consume structured buffers, see both sections: [append and consume buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and [structured buffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="62f23-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="62f23-117">Minimum Shader Model</span></span>

<span data-ttu-id="62f23-118">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="62f23-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="62f23-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="62f23-119">Shader Model</span></span>                                                                | <span data-ttu-id="62f23-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="62f23-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="62f23-121">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="62f23-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="62f23-122">sí</span><span class="sxs-lookup"><span data-stu-id="62f23-122">yes</span></span>       |



 

<span data-ttu-id="62f23-123">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="62f23-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="62f23-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="62f23-124">Vertex</span></span> | <span data-ttu-id="62f23-125">Casco</span><span class="sxs-lookup"><span data-stu-id="62f23-125">Hull</span></span> | <span data-ttu-id="62f23-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="62f23-126">Domain</span></span> | <span data-ttu-id="62f23-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="62f23-127">Geometry</span></span> | <span data-ttu-id="62f23-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="62f23-128">Pixel</span></span> | <span data-ttu-id="62f23-129">Compute</span><span class="sxs-lookup"><span data-stu-id="62f23-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="62f23-130">x</span><span class="sxs-lookup"><span data-stu-id="62f23-130">x</span></span>     | <span data-ttu-id="62f23-131">x</span><span class="sxs-lookup"><span data-stu-id="62f23-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="62f23-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="62f23-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f23-133">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="62f23-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 