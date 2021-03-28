---
title: RWStructuredBuffer
description: Un búfer de lectura/escritura que puede tomar un tipo T que es una estructura.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- HLSL de RWStructuredBuffer
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420894"
---
# <a name="rwstructuredbuffer"></a><span data-ttu-id="0445c-104">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="0445c-104">RWStructuredBuffer</span></span>

<span data-ttu-id="0445c-105">Un búfer de lectura/escritura que puede tomar un tipo T que es una estructura.</span><span class="sxs-lookup"><span data-stu-id="0445c-105">A read/write buffer that can take a T type that is a structure.</span></span>



| <span data-ttu-id="0445c-106">Método</span><span class="sxs-lookup"><span data-stu-id="0445c-106">Method</span></span>                                                                     | <span data-ttu-id="0445c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0445c-107">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="0445c-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="0445c-108">**DecrementCounter**</span></span>](sm5-object-rwstructuredbuffer-decrementcounter.md) | <span data-ttu-id="0445c-109">Disminuye el contador oculto del objeto.</span><span class="sxs-lookup"><span data-stu-id="0445c-109">Decrements the object's hidden counter.</span></span> |
| [<span data-ttu-id="0445c-110">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="0445c-110">**GetDimensions**</span></span>](sm5-object-rwstructuredbuffer-getdimensions.md)       | <span data-ttu-id="0445c-111">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="0445c-111">Gets the resource dimensions.</span></span>           |
| [<span data-ttu-id="0445c-112">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="0445c-112">**IncrementCounter**</span></span>](sm5-object-rwstructuredbuffer-incrementcounter.md) | <span data-ttu-id="0445c-113">Incrementa el contador oculto del objeto.</span><span class="sxs-lookup"><span data-stu-id="0445c-113">Increments the object's hidden counter.</span></span> |
| [<span data-ttu-id="0445c-114">**Carga**</span><span class="sxs-lookup"><span data-stu-id="0445c-114">**Load**</span></span>](rwstructuredbuffer-load.md)                                    | <span data-ttu-id="0445c-115">Lee los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="0445c-115">Reads buffer data.</span></span>                      |
| <span data-ttu-id="0445c-116">[**Operador\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="0445c-116">[**Operator\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span></span>        | <span data-ttu-id="0445c-117">Devuelve una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="0445c-117">Returns a resource variable.</span></span>            |



 

<span data-ttu-id="0445c-118">También se puede pasar una variable de recurso a cualquier operación sin ordenar o interbloqueada.</span><span class="sxs-lookup"><span data-stu-id="0445c-118">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="0445c-119">Los objetos RWStructuredBuffer pueden ir precedidos de la clase de almacenamiento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="0445c-119">RWStructuredBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="0445c-120">Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras.</span><span class="sxs-lookup"><span data-stu-id="0445c-120">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="0445c-121">Sin este especificador, una barrera de memoria o una sincronización solo vaciará un UAV dentro del grupo actual.</span><span class="sxs-lookup"><span data-stu-id="0445c-121">Without this specifier, a memory barrier or sync will only flush a UAV within the current group.</span></span>

<span data-ttu-id="0445c-122">El formato UAV enlazado a este recurso debe crearse con el formato de DXGI \_ \_ desconocido.</span><span class="sxs-lookup"><span data-stu-id="0445c-122">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="0445c-123">Para obtener más información sobre los [búferes estructurados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consulte el material de información general.</span><span class="sxs-lookup"><span data-stu-id="0445c-123">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="0445c-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0445c-124">Minimum Shader Model</span></span>

<span data-ttu-id="0445c-125">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0445c-125">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="0445c-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0445c-126">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="0445c-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="0445c-127">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0445c-128">Sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponible a través de la API de Direct3D 11 mediante el nivel de características 10,0 o 10,1 ([**\_ \_ nivel de característica D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) en los dispositivos que admiten los sombreadores de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0445c-128">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="0445c-129">Para obtener más información sobre la compatibilidad del sombreador de cálculo en el hardware de nivel inferior, vea [sombreadores de cálculo en hardware de nivel inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).</span><span class="sxs-lookup"><span data-stu-id="0445c-129">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="0445c-130">sí</span><span class="sxs-lookup"><span data-stu-id="0445c-130">yes</span></span>       |



 

<span data-ttu-id="0445c-131">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="0445c-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0445c-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="0445c-132">Vertex</span></span> | <span data-ttu-id="0445c-133">Casco</span><span class="sxs-lookup"><span data-stu-id="0445c-133">Hull</span></span> | <span data-ttu-id="0445c-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="0445c-134">Domain</span></span> | <span data-ttu-id="0445c-135">Geometría</span><span class="sxs-lookup"><span data-stu-id="0445c-135">Geometry</span></span> | <span data-ttu-id="0445c-136">Píxel</span><span class="sxs-lookup"><span data-stu-id="0445c-136">Pixel</span></span> | <span data-ttu-id="0445c-137">Compute</span><span class="sxs-lookup"><span data-stu-id="0445c-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0445c-138">x</span><span class="sxs-lookup"><span data-stu-id="0445c-138">x</span></span>     | <span data-ttu-id="0445c-139">x</span><span class="sxs-lookup"><span data-stu-id="0445c-139">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0445c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0445c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0445c-141">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0445c-141">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

