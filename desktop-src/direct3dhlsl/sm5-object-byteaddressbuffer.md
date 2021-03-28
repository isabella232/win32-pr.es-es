---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- HLSL de ByteAddressBuffer
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984074"
---
# <a name="byteaddressbuffer"></a><span data-ttu-id="766f5-104">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="766f5-104">ByteAddressBuffer</span></span>

<span data-ttu-id="766f5-105">Un búfer de solo lectura que se indiza en bytes.</span><span class="sxs-lookup"><span data-stu-id="766f5-105">A read-only buffer that is indexed in bytes.</span></span>



| <span data-ttu-id="766f5-106">Método</span><span class="sxs-lookup"><span data-stu-id="766f5-106">Method</span></span>                                                              | <span data-ttu-id="766f5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="766f5-107">Description</span></span>                   |
|---------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="766f5-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="766f5-108">**GetDimensions**</span></span>](sm5-object-byteaddressbuffer-getdimensions.md) | <span data-ttu-id="766f5-109">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="766f5-109">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="766f5-110">**Carga**</span><span class="sxs-lookup"><span data-stu-id="766f5-110">**Load**</span></span>](byteaddressbuffer-load.md)                              | <span data-ttu-id="766f5-111">Obtiene un valor.</span><span class="sxs-lookup"><span data-stu-id="766f5-111">Gets one value.</span></span>               |
| [<span data-ttu-id="766f5-112">**Load2**</span><span class="sxs-lookup"><span data-stu-id="766f5-112">**Load2**</span></span>](byteaddressbuffer-load2.md)                            | <span data-ttu-id="766f5-113">Obtiene dos valores.</span><span class="sxs-lookup"><span data-stu-id="766f5-113">Gets two values.</span></span>              |
| [<span data-ttu-id="766f5-114">**Load3**</span><span class="sxs-lookup"><span data-stu-id="766f5-114">**Load3**</span></span>](byteaddressbuffer-load3.md)                            | <span data-ttu-id="766f5-115">Obtiene tres valores.</span><span class="sxs-lookup"><span data-stu-id="766f5-115">Gets three values.</span></span>            |
| [<span data-ttu-id="766f5-116">**Load4**</span><span class="sxs-lookup"><span data-stu-id="766f5-116">**Load4**</span></span>](byteaddressbuffer-load4.md)                            | <span data-ttu-id="766f5-117">Obtiene cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="766f5-117">Gets four values.</span></span>             |



 

<span data-ttu-id="766f5-118">Puede usar el tipo de objeto **ByteAddressBuffer** cuando trabaje con búferes sin procesar.</span><span class="sxs-lookup"><span data-stu-id="766f5-118">You can use the **ByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="766f5-119">Para obtener más información sobre la visualización sin formato de los búferes, consulte [vistas sin formato de búferes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="766f5-119">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="766f5-120">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="766f5-120">Minimum Shader Model</span></span>

<span data-ttu-id="766f5-121">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="766f5-121">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="766f5-122">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="766f5-122">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="766f5-123">Compatible</span><span class="sxs-lookup"><span data-stu-id="766f5-123">Supported</span></span> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="766f5-124">Sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponible a través de la API de Direct3D 11 mediante el nivel de características 10,0 o 10,1 ([**\_ \_ nivel de característica D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) en los dispositivos que admiten los sombreadores de cálculo.</span><span class="sxs-lookup"><span data-stu-id="766f5-124">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="766f5-125">Para obtener más información sobre la compatibilidad del sombreador de cálculo en el hardware de nivel inferior, vea [sombreadores de cálculo en hardware de nivel inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)).</span><span class="sxs-lookup"><span data-stu-id="766f5-125">For more info about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="766f5-126">sí</span><span class="sxs-lookup"><span data-stu-id="766f5-126">yes</span></span>       |



 

<span data-ttu-id="766f5-127">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="766f5-127">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="766f5-128">Vértice</span><span class="sxs-lookup"><span data-stu-id="766f5-128">Vertex</span></span> | <span data-ttu-id="766f5-129">Casco</span><span class="sxs-lookup"><span data-stu-id="766f5-129">Hull</span></span> | <span data-ttu-id="766f5-130">Dominio</span><span class="sxs-lookup"><span data-stu-id="766f5-130">Domain</span></span> | <span data-ttu-id="766f5-131">Geometría</span><span class="sxs-lookup"><span data-stu-id="766f5-131">Geometry</span></span> | <span data-ttu-id="766f5-132">Píxel</span><span class="sxs-lookup"><span data-stu-id="766f5-132">Pixel</span></span> | <span data-ttu-id="766f5-133">Compute</span><span class="sxs-lookup"><span data-stu-id="766f5-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="766f5-134">x</span><span class="sxs-lookup"><span data-stu-id="766f5-134">x</span></span>      | <span data-ttu-id="766f5-135">x</span><span class="sxs-lookup"><span data-stu-id="766f5-135">x</span></span>    | <span data-ttu-id="766f5-136">x</span><span class="sxs-lookup"><span data-stu-id="766f5-136">x</span></span>      | <span data-ttu-id="766f5-137">x</span><span class="sxs-lookup"><span data-stu-id="766f5-137">x</span></span>        | <span data-ttu-id="766f5-138">x</span><span class="sxs-lookup"><span data-stu-id="766f5-138">x</span></span>     | <span data-ttu-id="766f5-139">x</span><span class="sxs-lookup"><span data-stu-id="766f5-139">x</span></span>       |



 

<span data-ttu-id="766f5-140">Para obtener más información sobre un búfer de direcciones de bytes, consulte el [tipo de recurso byte direccionable](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="766f5-140">For more info about a byte address buffer, see the [byte addressable resource type](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

<span data-ttu-id="766f5-141">El modelo de sombreador 5 también implementa un [búfer de direcciones de bytes de lectura y escritura](sm5-object-rwbyteaddressbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="766f5-141">Shader Model 5 also implements a [read-write byte address buffer](sm5-object-rwbyteaddressbuffer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="766f5-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="766f5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="766f5-143">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="766f5-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

