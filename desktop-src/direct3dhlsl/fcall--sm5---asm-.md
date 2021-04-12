---
title: fcall (SM5-ASM)
description: Llamada de función de interfaz.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419979"
---
# <a name="fcall-sm5---asm"></a><span data-ttu-id="703a2-103">fcall (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="703a2-103">fcall (sm5 - asm)</span></span>

<span data-ttu-id="703a2-104">Llamada de función de interfaz.</span><span class="sxs-lookup"><span data-stu-id="703a2-104">Interface function call.</span></span>



| <span data-ttu-id="703a2-105">fcall FP \# \[ arrayIndex \] \[ llamada\]</span><span class="sxs-lookup"><span data-stu-id="703a2-105">fcall fp\#\[arrayIndex\]\[callSite\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="703a2-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="703a2-106">Item</span></span>                                                                                                           | <span data-ttu-id="703a2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="703a2-107">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="703a2-108"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="703a2-108"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/>                                                  | <span data-ttu-id="703a2-109">\[en \] el puntero de función.</span><span class="sxs-lookup"><span data-stu-id="703a2-109">\[in\] The function pointer.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="703a2-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span><span class="sxs-lookup"><span data-stu-id="703a2-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span></span><br/> | <span data-ttu-id="703a2-111">\[en \] opcional.</span><span class="sxs-lookup"><span data-stu-id="703a2-111">\[in\] Optional.</span></span> <span data-ttu-id="703a2-112">Especifica un desplazamiento en la matriz de puntero de función.</span><span class="sxs-lookup"><span data-stu-id="703a2-112">Specifies an offset into the function pointer array.</span></span> <span data-ttu-id="703a2-113">Este parámetro debe ser un entero sin signo literal si FP \# no se declaró como indexable.</span><span class="sxs-lookup"><span data-stu-id="703a2-113">This parameter must be a literal unsigned integer if fp\# was not declared as indexable.</span></span> <span data-ttu-id="703a2-114">De lo contrario, arrayIndex puede tener el formato literal base + offset de un registro del sombreador.</span><span class="sxs-lookup"><span data-stu-id="703a2-114">Otherwise, arrayIndex may be of the form literal base + offset from a shader register.</span></span> <span data-ttu-id="703a2-115">Por ejemplo, fcall FP1 \[ R1. w + 0 \] \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="703a2-115">For example, fcall fp1\[r1.w + 0\]\[0\] .</span></span><br/> |
| <span data-ttu-id="703a2-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*llamada*</span><span class="sxs-lookup"><span data-stu-id="703a2-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span> *callSite*</span></span><br/>     | <span data-ttu-id="703a2-117">\[en \] opcional.</span><span class="sxs-lookup"><span data-stu-id="703a2-117">\[in\] Optional.</span></span> <span data-ttu-id="703a2-118">Un desplazamiento de entero sin signo literal en la tabla de la función seleccionada, seleccionando el cuerpo de una función FB \# para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="703a2-118">A literal unsigned integer offset into the selected function table, selecting a function body fb\# to execute.</span></span> <br/>                                                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="703a2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="703a2-119">Remarks</span></span>

<span data-ttu-id="703a2-120">*FP \#* \[  \] \[ arrayIndex \] se resuelve como una tabla de función determinada, seleccionada de la API fuera del sombreador de las opciones de la tabla de funciones enumeradas en la declaración de *FP \#*.</span><span class="sxs-lookup"><span data-stu-id="703a2-120">*fp\#*\[*arrayIndex*\]\[\] resolves to a particular function table, selected from the API outside the shader from the function table choices listed in the declaration of *fp\#*.</span></span>

<span data-ttu-id="703a2-121">La suma de \# en *FP \#* y *arrayIndex* selecciona la tabla de funciones.</span><span class="sxs-lookup"><span data-stu-id="703a2-121">The sum of \# in *fp\#* and *arrayIndex* select the function table.</span></span> <span data-ttu-id="703a2-122">Por ejemplo, si una interfaz se declara como FP4 \[ 4 \] \[ 3 \] (tamaño de matriz de 4), los siguientes **fcall** s son equivalentes: fcall FP4 \[ 2 \] \[ 3 \] y FP5 \[ 1 \] \[ 3 \] , porque 4 + 2 = 5 + 1.</span><span class="sxs-lookup"><span data-stu-id="703a2-122">For example, if an interface is declared as fp4\[4\]\[3\] (array size of 4), the following **fcall** s are equivalent: fcall fp4\[2\]\[3\] and fp5\[1\]\[3\], because 4+2 = 5+1.</span></span>

### <a name="restrictions"></a><span data-ttu-id="703a2-123">Restricciones</span><span class="sxs-lookup"><span data-stu-id="703a2-123">Restrictions</span></span>

-   <span data-ttu-id="703a2-124">Si *arrayIndex* utiliza la indexación dinámica, el comportamiento es indefinido si *arrayIndex* difiere en las invocaciones de sombreador adyacentes, que podrían ejecutarse en lógico.</span><span class="sxs-lookup"><span data-stu-id="703a2-124">If *arrayIndex* uses dynamic indexing, behavior is undefined if *arrayIndex* diverges on adjacent shader invocations, which could be executing in lockstep.</span></span> <span data-ttu-id="703a2-125">El compilador de HLSL intentará no permitir este caso.</span><span class="sxs-lookup"><span data-stu-id="703a2-125">The HLSL compiler will attempt to disallow this case.</span></span>

    <span data-ttu-id="703a2-126">Las invocaciones adyacentes pueden estar inactivas debido al control de flujo, ya que no interrumpe la ejecución de lógico.</span><span class="sxs-lookup"><span data-stu-id="703a2-126">Adjacent invocations can be inactive due to flow control, because it doesn t break lockstep execution.</span></span>

-   <span data-ttu-id="703a2-127">Si *FP \#*  +  *arrayIndex* especifica un índice fuera del límite, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="703a2-127">If *fp\#* + *arrayIndex* specifies an out of bounds index, behavior is undefined.</span></span>
-   <span data-ttu-id="703a2-128">En el caso de los casos no definidos que se describen aquí, el comportamiento del dispositivo D3D actual queda indefinido, lo que incluye la posibilidad de que se pierda el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="703a2-128">For the undefined cases described here, it means the behavior of the current D3D device becomes undefined, including the possibility of Device Lost.</span></span> <span data-ttu-id="703a2-129">Sin embargo, no se tendrá acceso a la memoria fuera del dispositivo D3D actual ni se ejecutará como código.</span><span class="sxs-lookup"><span data-stu-id="703a2-129">However no memory outside the current D3D device will be accessed or executed as code.</span></span>

<span data-ttu-id="703a2-130">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="703a2-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="703a2-131">Vértice</span><span class="sxs-lookup"><span data-stu-id="703a2-131">Vertex</span></span> | <span data-ttu-id="703a2-132">Casco</span><span class="sxs-lookup"><span data-stu-id="703a2-132">Hull</span></span> | <span data-ttu-id="703a2-133">Dominio</span><span class="sxs-lookup"><span data-stu-id="703a2-133">Domain</span></span> | <span data-ttu-id="703a2-134">Geometría</span><span class="sxs-lookup"><span data-stu-id="703a2-134">Geometry</span></span> | <span data-ttu-id="703a2-135">Píxel</span><span class="sxs-lookup"><span data-stu-id="703a2-135">Pixel</span></span> | <span data-ttu-id="703a2-136">Compute</span><span class="sxs-lookup"><span data-stu-id="703a2-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="703a2-137">X</span><span class="sxs-lookup"><span data-stu-id="703a2-137">X</span></span>      | <span data-ttu-id="703a2-138">X</span><span class="sxs-lookup"><span data-stu-id="703a2-138">X</span></span>    | <span data-ttu-id="703a2-139">X</span><span class="sxs-lookup"><span data-stu-id="703a2-139">X</span></span>      | <span data-ttu-id="703a2-140">X</span><span class="sxs-lookup"><span data-stu-id="703a2-140">X</span></span>        | <span data-ttu-id="703a2-141">X</span><span class="sxs-lookup"><span data-stu-id="703a2-141">X</span></span>     | <span data-ttu-id="703a2-142">X</span><span class="sxs-lookup"><span data-stu-id="703a2-142">X</span></span>       |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="703a2-143">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="703a2-143">Minimum Shader Model</span></span>

<span data-ttu-id="703a2-144">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="703a2-144">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="703a2-145">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="703a2-145">Shader Model</span></span>                                              | <span data-ttu-id="703a2-146">Compatible</span><span class="sxs-lookup"><span data-stu-id="703a2-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="703a2-147">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="703a2-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="703a2-148">sí</span><span class="sxs-lookup"><span data-stu-id="703a2-148">yes</span></span>       |
| [<span data-ttu-id="703a2-149">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="703a2-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="703a2-150">no</span><span class="sxs-lookup"><span data-stu-id="703a2-150">no</span></span>        |
| [<span data-ttu-id="703a2-151">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="703a2-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="703a2-152">no</span><span class="sxs-lookup"><span data-stu-id="703a2-152">no</span></span>        |
| [<span data-ttu-id="703a2-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="703a2-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="703a2-154">no</span><span class="sxs-lookup"><span data-stu-id="703a2-154">no</span></span>        |
| [<span data-ttu-id="703a2-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="703a2-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="703a2-156">no</span><span class="sxs-lookup"><span data-stu-id="703a2-156">no</span></span>        |
| [<span data-ttu-id="703a2-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="703a2-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="703a2-158">no</span><span class="sxs-lookup"><span data-stu-id="703a2-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="703a2-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="703a2-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="703a2-160">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="703a2-160">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





