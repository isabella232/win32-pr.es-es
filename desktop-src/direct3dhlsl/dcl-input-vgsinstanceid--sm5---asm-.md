---
title: dcl_input vGSInstanceID (SM5-ASM)
description: Habilitar la creación de instancias del sombreador de geometría.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358514"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a><span data-ttu-id="6f2be-103">\_vGSInstanceID de entrada de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6f2be-103">dcl\_input vGSInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="6f2be-104">Habilitar la creación de instancias del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="6f2be-104">Enable geometry shader instancing.</span></span>



| <span data-ttu-id="6f2be-105">\_entrada de DCL vGSInstanceID, instanceCount</span><span class="sxs-lookup"><span data-stu-id="6f2be-105">dcl\_input vGSInstanceID, instanceCount</span></span> |
|-----------------------------------------|



 



| <span data-ttu-id="6f2be-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="6f2be-106">Item</span></span>                                                                                                                       | <span data-ttu-id="6f2be-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f2be-107">Description</span></span>                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="6f2be-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span><span class="sxs-lookup"><span data-stu-id="6f2be-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span></span><br/> | <span data-ttu-id="6f2be-109">\[en \] el ID. de instancia.</span><span class="sxs-lookup"><span data-stu-id="6f2be-109">\[in\] The instance ID.</span></span><br/>    |
| <span data-ttu-id="6f2be-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span><span class="sxs-lookup"><span data-stu-id="6f2be-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span></span><br/> | <span data-ttu-id="6f2be-111">\[en \] el recuento de instancias.</span><span class="sxs-lookup"><span data-stu-id="6f2be-111">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6f2be-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f2be-112">Remarks</span></span>

<span data-ttu-id="6f2be-113">El parámetro *instanceCount* de la declaración especifica el número de instancias que el sombreador de geometría debe ejecutar para cada primitiva de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f2be-113">The *instanceCount* parameter of the declaration specifies how many instances the geometry shader should execute for each input primitive.</span></span> <span data-ttu-id="6f2be-114">El valor máximo de *instanceCount* es 32.</span><span class="sxs-lookup"><span data-stu-id="6f2be-114">The maximum value for *instanceCount* is 32.</span></span>

<span data-ttu-id="6f2be-115">El número máximo de vértices declarado para la salida, a través de [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), se aplica individualmente a cada instancia.</span><span class="sxs-lookup"><span data-stu-id="6f2be-115">The maximum number of vertices declared for output, via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), applies individually to each instance.</span></span>

<span data-ttu-id="6f2be-116">El recuento de instancias en esta declaración, multiplicado por el número máximo de vértices por instancia a través de [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), debe ser <= 1024.</span><span class="sxs-lookup"><span data-stu-id="6f2be-116">The instance count in this declaration, multiplied by the maximum vertex count per instance via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), must be <= 1024.</span></span>

<span data-ttu-id="6f2be-117">La cantidad de datos que puede emitir una instancia de sombreador de geometría determinada es 1024 escalares máximos, validados por el recuento de todos los escalares declarados para la entrada y la multiplicación por el número de vértices de salida declarado.</span><span class="sxs-lookup"><span data-stu-id="6f2be-117">The amount of data that a given geometry shader instance can emit is 1024 scalars maximum, validated by counting up all scalars declared for input and multiplying by the declared output vertex count.</span></span>

<span data-ttu-id="6f2be-118">El uso de la creación de instancias del sombreador de geometría aumenta de forma eficaz la cantidad total de datos que se pueden emitir por primitiva de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f2be-118">Use of geometry shader instancing effectively increases the total amount of data that can be emitted per input primitive.</span></span> <span data-ttu-id="6f2be-119">1024 escalares para una instancia única produce hasta 1024 \* 32 escalares de datos de salida en todas las instancias de sombreador de geometría para un único primitivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f2be-119">1024 scalars for a single instance yields up to 1024\*32 scalars of output data across all geometry shader instances for a single input primitive.</span></span> <span data-ttu-id="6f2be-120">Sin embargo, cuantas más instancias haya, menos vértices podrá emitir cada instancia.</span><span class="sxs-lookup"><span data-stu-id="6f2be-120">However the more instances, the fewer vertices each instance can emit.</span></span> <span data-ttu-id="6f2be-121">Una sola instancia (sin creación de instancias) puede emitir vértices 1024.</span><span class="sxs-lookup"><span data-stu-id="6f2be-121">A single instance (no instancing) can emit 1024 vertices.</span></span> <span data-ttu-id="6f2be-122">Si declara \* 32 instancias, significa que cada instancia solo puede generar los vértices 1024/32 = 32.</span><span class="sxs-lookup"><span data-stu-id="6f2be-122">If you declare \*32 instances it means each instance can only output 1024/32 = 32 vertices.</span></span>

<span data-ttu-id="6f2be-123">La declaración de creación de instancias del sombreador de geometría pone a disposición del programa un registro de entrada entero de 32 bits independiente, *vGSInstanceID*.</span><span class="sxs-lookup"><span data-stu-id="6f2be-123">The geometry shader instancing declaration makes available to the program a standalone 32-bit integer input register, *vGSInstanceID*.</span></span> <span data-ttu-id="6f2be-124">Cada instancia del sombreador de geometría se identifica mediante el valor contenido en *vGSInstanceID* \[ 0, 1, 2... \] .</span><span class="sxs-lookup"><span data-stu-id="6f2be-124">Each geometry shader instance is identified by the value contained in *vGSInstanceID* \[0,1,2...\].</span></span>

<span data-ttu-id="6f2be-125">*vGSInstanceID* no forma parte de la matriz de vértices de entrada del sombreador de geometría (por ejemplo, 3 vértices al insertar un triángulo).</span><span class="sxs-lookup"><span data-stu-id="6f2be-125">*vGSInstanceID* is not part of the geometry shader input vertex array (e.g. 3 vertices when inputting a triangle).</span></span> <span data-ttu-id="6f2be-126">El registro *vGSInstanceID* es propio, como vPrimitiveID.</span><span class="sxs-lookup"><span data-stu-id="6f2be-126">The *vGSInstanceID* register stands on its own, like vPrimitiveID.</span></span>

<span data-ttu-id="6f2be-127">Cuando finaliza cada instancia de sombreador de geometría, hay un corte implícito en la topología de salida, por lo que las instancias consecutivas no dependen unas de otras.</span><span class="sxs-lookup"><span data-stu-id="6f2be-127">When each geometry shader instance ends, there is an implicit cut in the output topology, so consecutive instances do not depend on each other.</span></span>

<span data-ttu-id="6f2be-128">Aunque el hardware puede ejecutar cada instancia del sombreador de geometría en paralelo, la salida de todas las instancias del extremo se serializa como si todas las invocaciones del sombreador de geometría con instancias se ejecutaran secuencialmente en un bucle que recorre *vGSInstanceID* de 0 a *instanceCount*-1, con cortes de topología de salida implícitos al final de cada instancia.</span><span class="sxs-lookup"><span data-stu-id="6f2be-128">Although hardware may execute each geometry shader instance in parallel, the output of all instances at the end is serialized as if all the instanced geometry shader invocations ran sequentially in a loop iterating *vGSInstanceID* from 0 to *instanceCount*-1, with implicit output topology cuts at the end of each instance.</span></span>

<span data-ttu-id="6f2be-129">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="6f2be-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6f2be-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="6f2be-130">Vertex</span></span> | <span data-ttu-id="6f2be-131">Casco</span><span class="sxs-lookup"><span data-stu-id="6f2be-131">Hull</span></span> | <span data-ttu-id="6f2be-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="6f2be-132">Domain</span></span> | <span data-ttu-id="6f2be-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="6f2be-133">Geometry</span></span> | <span data-ttu-id="6f2be-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="6f2be-134">Pixel</span></span> | <span data-ttu-id="6f2be-135">Compute</span><span class="sxs-lookup"><span data-stu-id="6f2be-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="6f2be-136">X</span><span class="sxs-lookup"><span data-stu-id="6f2be-136">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6f2be-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6f2be-137">Minimum Shader Model</span></span>

<span data-ttu-id="6f2be-138">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6f2be-138">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6f2be-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6f2be-139">Shader Model</span></span>                                              | <span data-ttu-id="6f2be-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="6f2be-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6f2be-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6f2be-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6f2be-142">sí</span><span class="sxs-lookup"><span data-stu-id="6f2be-142">yes</span></span>       |
| [<span data-ttu-id="6f2be-143">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6f2be-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6f2be-144">no</span><span class="sxs-lookup"><span data-stu-id="6f2be-144">no</span></span>        |
| [<span data-ttu-id="6f2be-145">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6f2be-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6f2be-146">no</span><span class="sxs-lookup"><span data-stu-id="6f2be-146">no</span></span>        |
| [<span data-ttu-id="6f2be-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f2be-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6f2be-148">no</span><span class="sxs-lookup"><span data-stu-id="6f2be-148">no</span></span>        |
| [<span data-ttu-id="6f2be-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f2be-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6f2be-150">no</span><span class="sxs-lookup"><span data-stu-id="6f2be-150">no</span></span>        |
| [<span data-ttu-id="6f2be-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f2be-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6f2be-152">no</span><span class="sxs-lookup"><span data-stu-id="6f2be-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6f2be-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6f2be-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f2be-154">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f2be-154">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





