---
title: StructuredBuffer
description: Un búfer de solo lectura, que puede tomar un tipo T que es una estructura.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- HLSL de StructuredBuffer
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997072"
---
# <a name="structuredbuffer"></a><span data-ttu-id="29870-104">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="29870-104">StructuredBuffer</span></span>

<span data-ttu-id="29870-105">Un búfer de solo lectura, que puede tomar un tipo T que es una estructura.</span><span class="sxs-lookup"><span data-stu-id="29870-105">A read-only buffer, which can take a T type that is a structure.</span></span>



| <span data-ttu-id="29870-106">Método</span><span class="sxs-lookup"><span data-stu-id="29870-106">Method</span></span>                                                             | <span data-ttu-id="29870-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="29870-107">Description</span></span>                            |
|--------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="29870-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="29870-108">**GetDimensions**</span></span>](sm5-object-structuredbuffer-getdimensions.md) | <span data-ttu-id="29870-109">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="29870-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="29870-110">**Carga**</span><span class="sxs-lookup"><span data-stu-id="29870-110">**Load**</span></span>](structuredbuffer-load.md)                              | <span data-ttu-id="29870-111">Lee los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="29870-111">Reads buffer data.</span></span>                     |
| <span data-ttu-id="29870-112">[**Operador\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="29870-112">[**Operator\[\]**](sm5-object-structuredbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="29870-113">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="29870-113">Returns a read-only resource variable.</span></span> |



 

<span data-ttu-id="29870-114">El formato UAV enlazado a este recurso debe crearse con el formato de DXGI \_ \_ desconocido.</span><span class="sxs-lookup"><span data-stu-id="29870-114">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="29870-115">Para obtener más información sobre los [búferes estructurados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consulte el material de información general.</span><span class="sxs-lookup"><span data-stu-id="29870-115">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="29870-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="29870-116">Minimum Shader Model</span></span>

<span data-ttu-id="29870-117">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="29870-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="29870-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="29870-118">Shader Model</span></span>                                                                                                                                                                                                            | <span data-ttu-id="29870-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="29870-119">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="29870-120">Sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador de mayor nivel modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponibles para los sombreadores de cálculo y de píxeles en Direct3D 11 en algunos dispositivos de Direct3D 10).</span><span class="sxs-lookup"><span data-stu-id="29870-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available for compute and pixel shaders in Direct3D 11 on some Direct3D 10 devices.)</span></span><br/> | <span data-ttu-id="29870-121">sí</span><span class="sxs-lookup"><span data-stu-id="29870-121">yes</span></span>       |



 

<span data-ttu-id="29870-122">Este objeto es compatible con los siguientes tipos de sombreadores.</span><span class="sxs-lookup"><span data-stu-id="29870-122">This object is supported for the following types of shaders.</span></span>



| <span data-ttu-id="29870-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="29870-123">Vertex</span></span> | <span data-ttu-id="29870-124">Casco</span><span class="sxs-lookup"><span data-stu-id="29870-124">Hull</span></span> | <span data-ttu-id="29870-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="29870-125">Domain</span></span> | <span data-ttu-id="29870-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="29870-126">Geometry</span></span> | <span data-ttu-id="29870-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="29870-127">Pixel</span></span> | <span data-ttu-id="29870-128">Compute</span><span class="sxs-lookup"><span data-stu-id="29870-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="29870-129">x</span><span class="sxs-lookup"><span data-stu-id="29870-129">x</span></span>      | <span data-ttu-id="29870-130">x</span><span class="sxs-lookup"><span data-stu-id="29870-130">x</span></span>    | <span data-ttu-id="29870-131">x</span><span class="sxs-lookup"><span data-stu-id="29870-131">x</span></span>      | <span data-ttu-id="29870-132">x</span><span class="sxs-lookup"><span data-stu-id="29870-132">x</span></span>        | <span data-ttu-id="29870-133">x</span><span class="sxs-lookup"><span data-stu-id="29870-133">x</span></span>     | <span data-ttu-id="29870-134">x</span><span class="sxs-lookup"><span data-stu-id="29870-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="29870-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="29870-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29870-136">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="29870-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

