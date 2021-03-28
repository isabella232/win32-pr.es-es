---
title: RWByteAddressBuffer
description: Un búfer de lectura/escritura que indexa en bytes.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- HLSL de RWByteAddressBuffer
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420742"
---
# <a name="rwbyteaddressbuffer"></a><span data-ttu-id="4cf7e-104">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="4cf7e-104">RWByteAddressBuffer</span></span>

<span data-ttu-id="4cf7e-105">Un búfer de lectura/escritura que indexa en bytes.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-105">A read/write buffer that indexes in bytes.</span></span>



| <span data-ttu-id="4cf7e-106">Método</span><span class="sxs-lookup"><span data-stu-id="4cf7e-106">Method</span></span>                                                                                          | <span data-ttu-id="4cf7e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cf7e-107">Description</span></span>                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="4cf7e-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-108">**GetDimensions**</span></span>](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | <span data-ttu-id="4cf7e-109">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="4cf7e-110">**InterlockedAdd**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-110">**InterlockedAdd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | <span data-ttu-id="4cf7e-111">Agrega, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-111">Adds, atomically.</span></span>                   |
| [<span data-ttu-id="4cf7e-112">**InterlockedAnd**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-112">**InterlockedAnd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | <span data-ttu-id="4cf7e-113">And, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-113">ANDs, atomically.</span></span>                   |
| [<span data-ttu-id="4cf7e-114">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-114">**InterlockedCompareExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | <span data-ttu-id="4cf7e-115">Compara e intercambia, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-115">Compares and exchanges, atomically.</span></span> |
| [<span data-ttu-id="4cf7e-116">**InterlockedCompareStore**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-116">**InterlockedCompareStore**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | <span data-ttu-id="4cf7e-117">Compara y almacena, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-117">Compares and stores, atomically.</span></span>    |
| [<span data-ttu-id="4cf7e-118">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-118">**InterlockedExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | <span data-ttu-id="4cf7e-119">Intercambios, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-119">Exchanges, atomically.</span></span>              |
| [<span data-ttu-id="4cf7e-120">**InterlockedMax**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-120">**InterlockedMax**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | <span data-ttu-id="4cf7e-121">Busca el máximo, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-121">Finds the max, atomically.</span></span>          |
| [<span data-ttu-id="4cf7e-122">**InterlockedMin**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-122">**InterlockedMin**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | <span data-ttu-id="4cf7e-123">Busque min, atomicly.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-123">Find the min, atomically.</span></span>           |
| [<span data-ttu-id="4cf7e-124">**Interbloqueo**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-124">**InterlockedOr**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | <span data-ttu-id="4cf7e-125">ORs, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-125">ORs, atomically.</span></span>                    |
| [<span data-ttu-id="4cf7e-126">**InterlockedXor**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-126">**InterlockedXor**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | <span data-ttu-id="4cf7e-127">XORs, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-127">XORs, atomically.</span></span>                   |
| [<span data-ttu-id="4cf7e-128">**Carga**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-128">**Load**</span></span>](rwbyteaddressbuffer-load.md)                                                        | <span data-ttu-id="4cf7e-129">Obtiene un valor.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-129">Gets one value.</span></span>                     |
| [<span data-ttu-id="4cf7e-130">**Load2**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-130">**Load2**</span></span>](rwbyteaddressbuffer-load2.md)                                                      | <span data-ttu-id="4cf7e-131">Obtiene dos valores.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-131">Gets two values.</span></span>                    |
| [<span data-ttu-id="4cf7e-132">**Load3**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-132">**Load3**</span></span>](rwbyteaddressbuffer-load3.md)                                                      | <span data-ttu-id="4cf7e-133">Obtiene tres valores.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-133">Gets three values.</span></span>                  |
| [<span data-ttu-id="4cf7e-134">**Load4**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-134">**Load4**</span></span>](rwbyteaddressbuffer-load4.md)                                                      | <span data-ttu-id="4cf7e-135">Obtiene cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-135">Gets four values.</span></span>                   |
| [<span data-ttu-id="4cf7e-136">**Store**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-136">**Store**</span></span>](sm5-object-rwbyteaddressbuffer-store.md)                                           | <span data-ttu-id="4cf7e-137">Establece un valor.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-137">Sets one value.</span></span>                     |
| [<span data-ttu-id="4cf7e-138">**2**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-138">**Store2**</span></span>](sm5-object-rwbyteaddressbuffer-store2.md)                                         | <span data-ttu-id="4cf7e-139">Establece dos valores.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-139">Sets two values.</span></span>                    |
| [<span data-ttu-id="4cf7e-140">**Store3**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-140">**Store3**</span></span>](sm5-object-rwbyteaddressbuffer-store3.md)                                         | <span data-ttu-id="4cf7e-141">Establece tres valores.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-141">Sets three values.</span></span>                  |
| [<span data-ttu-id="4cf7e-142">**Store4**</span><span class="sxs-lookup"><span data-stu-id="4cf7e-142">**Store4**</span></span>](sm5-object-rwbyteaddressbuffer-store4.md)                                         | <span data-ttu-id="4cf7e-143">Establece cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-143">Sets four values.</span></span>                   |



 

<span data-ttu-id="4cf7e-144">Los objetos RWByteAddressBuffer pueden ir precedidos de la clase de almacenamiento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-144">RWByteAddressBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="4cf7e-145">Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-145">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="4cf7e-146">Sin este especificador, una barrera de memoria o una sincronización vaciará un UAV solo dentro del grupo actual.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-146">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="4cf7e-147">El formato UAV enlazado a este recurso debe crearse con el formato DXGI sin \_ \_ \_ tipo R32.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-147">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_R32\_TYPELESS format.</span></span>

<span data-ttu-id="4cf7e-148">El UAV enlazado a este recurso se debe haber creado con [**el \_ búfer de D3D11 UAV de \_ \_ marca \_ sin formato**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="4cf7e-148">The UAV bound to this resource must have been created with the [**D3D11\_BUFFER\_UAV\_FLAG\_RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="4cf7e-149">Puede usar el tipo de objeto **RWByteAddressBuffer** cuando trabaje con búferes sin procesar.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-149">You can use the **RWByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="4cf7e-150">Para obtener más información sobre la visualización sin formato de los búferes, consulte [vistas sin formato de búferes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="4cf7e-150">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="4cf7e-151">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="4cf7e-151">Minimum Shader Model</span></span>

<span data-ttu-id="4cf7e-152">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-152">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="4cf7e-153">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4cf7e-153">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="4cf7e-154">Compatible</span><span class="sxs-lookup"><span data-stu-id="4cf7e-154">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4cf7e-155">Sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponible a través de la API de Direct3D 11 mediante el nivel de características 10,0 o 10,1 ([**\_ \_ nivel de característica D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) en los dispositivos que admiten los sombreadores de cálculo.</span><span class="sxs-lookup"><span data-stu-id="4cf7e-155">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="4cf7e-156">Para obtener más información sobre la compatibilidad del sombreador de cálculo en el hardware de nivel inferior, vea [sombreadores de cálculo en hardware de nivel inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).</span><span class="sxs-lookup"><span data-stu-id="4cf7e-156">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="4cf7e-157">sí</span><span class="sxs-lookup"><span data-stu-id="4cf7e-157">yes</span></span>       |



 

<span data-ttu-id="4cf7e-158">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4cf7e-158">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4cf7e-159">Vértice</span><span class="sxs-lookup"><span data-stu-id="4cf7e-159">Vertex</span></span> | <span data-ttu-id="4cf7e-160">Casco</span><span class="sxs-lookup"><span data-stu-id="4cf7e-160">Hull</span></span> | <span data-ttu-id="4cf7e-161">Dominio</span><span class="sxs-lookup"><span data-stu-id="4cf7e-161">Domain</span></span> | <span data-ttu-id="4cf7e-162">Geometría</span><span class="sxs-lookup"><span data-stu-id="4cf7e-162">Geometry</span></span> | <span data-ttu-id="4cf7e-163">Píxel</span><span class="sxs-lookup"><span data-stu-id="4cf7e-163">Pixel</span></span> | <span data-ttu-id="4cf7e-164">Compute</span><span class="sxs-lookup"><span data-stu-id="4cf7e-164">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4cf7e-165">x</span><span class="sxs-lookup"><span data-stu-id="4cf7e-165">x</span></span>     | <span data-ttu-id="4cf7e-166">x</span><span class="sxs-lookup"><span data-stu-id="4cf7e-166">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4cf7e-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cf7e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf7e-168">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4cf7e-168">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

