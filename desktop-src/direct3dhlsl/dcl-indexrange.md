---
title: dcl_indexRange (SM4-ASM)
description: DCL \_ indexRange (SM4-ASM)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983910"
---
# <a name="dcl_indexrange-sm4---asm"></a><span data-ttu-id="a7bca-103">DCL \_ indexRange (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a7bca-103">dcl\_indexRange (sm4 - asm)</span></span>

<span data-ttu-id="a7bca-104">Declara un intervalo de registros al que se tendrá acceso mediante el índice (un entero calculado en el sombreador).</span><span class="sxs-lookup"><span data-stu-id="a7bca-104">Declares a range of registers that will be accessed by index (an integer computed in the shader).</span></span>



| <span data-ttu-id="a7bca-105">DCL \_ IndexRange *minRegisterM*, *maxRegisterN*</span><span class="sxs-lookup"><span data-stu-id="a7bca-105">dcl\_indexRange *minRegisterM*, *maxRegisterN*</span></span> |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7bca-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a7bca-106">Item</span></span></th>
<th><span data-ttu-id="a7bca-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bca-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7bca-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span><span class="sxs-lookup"><span data-stu-id="a7bca-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span></span><br/></td>
<td><span data-ttu-id="a7bca-109">de Primer registro al que se va a obtener acceso por índice.</span><span class="sxs-lookup"><span data-stu-id="a7bca-109">[in] The first register to access by index.</span></span> <br/>
<ul>
<li><span data-ttu-id="a7bca-110"><em>minRegister</em> es <strong>v</strong> para un registro de entrada del sombreador de píxeles o vértices <strong>, o o</strong> para un registro de salida del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="a7bca-110"><em>minRegister</em> is either <strong>v</strong> for a vertex or pixel shader input register, or <strong>o</strong> for a vertex shader output register.</span></span></li>
<li><span data-ttu-id="a7bca-111"><em>M</em> es un entero que denota el número de registro.</span><span class="sxs-lookup"><span data-stu-id="a7bca-111"><em>M</em> is an integer that denotes the register number.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bca-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span><span class="sxs-lookup"><span data-stu-id="a7bca-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span></span><br/></td>
<td><span data-ttu-id="a7bca-113">de Último registro al que obtener acceso por índice.</span><span class="sxs-lookup"><span data-stu-id="a7bca-113">[in] The last register to access by index.</span></span> <span data-ttu-id="a7bca-114">La misma forma que <em>minRegister</em> , excepto <em>N</em> , es el número de registro.</span><span class="sxs-lookup"><span data-stu-id="a7bca-114">Same form as <em>minRegister</em> except <em>N</em> is the register number.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a7bca-115">Se aplican las restricciones siguientes a todos los registros:</span><span class="sxs-lookup"><span data-stu-id="a7bca-115">The following restrictions apply to all registers:</span></span>

-   <span data-ttu-id="a7bca-116">Los registros min y Max deben ser del mismo tipo y tener las mismas máscaras de componentes (si se declaran máscaras).</span><span class="sxs-lookup"><span data-stu-id="a7bca-116">The min and max registers must be the same type and have the same component masks (if masks are declared).</span></span>
-   <span data-ttu-id="a7bca-117">Un registro puede tener varios intervalos de índice, siempre y cuando no se superpongan.</span><span class="sxs-lookup"><span data-stu-id="a7bca-117">A register may have multiple index ranges, as long as they do no not overlap.</span></span>
-   <span data-ttu-id="a7bca-118">El número de registro mínimo debe ser menor que el número de registro máximo.</span><span class="sxs-lookup"><span data-stu-id="a7bca-118">The min register number must be less than the max register number.</span></span>
-   <span data-ttu-id="a7bca-119">Un registro de índice no puede contener un [valor del sistema](dx-graphics-hlsl-semantics.md).</span><span class="sxs-lookup"><span data-stu-id="a7bca-119">An index register cannot contain a [system-value](dx-graphics-hlsl-semantics.md).</span></span>
-   <span data-ttu-id="a7bca-120">La indización de un registro fuera de la declaración de índice máximo genera resultados no definidos.</span><span class="sxs-lookup"><span data-stu-id="a7bca-120">Indexing a register outside of the max index declaration produces undefined results.</span></span>

<span data-ttu-id="a7bca-121">Los registros de entrada del sombreador de píxeles deben usar el mismo modo de interpolación; los registros de salida del sombreador de píxeles no se pueden indexar.</span><span class="sxs-lookup"><span data-stu-id="a7bca-121">Pixel shader input registers must use the same interpolation mode; pixel shader output registers are not indexable.</span></span>

<span data-ttu-id="a7bca-122">Un registro de entrada del sombreador de geometría tiene dos dimensiones (eje de vértices, eje de atributo); el intervalo de índice solo se aplica al eje de atributo porque el eje del vértice siempre es totalmente indexable.</span><span class="sxs-lookup"><span data-stu-id="a7bca-122">A geometry shader input register has two dimensions (vertex axis, attribute axis); the index range applies only to the attribute axis because the vertex axis is always fully indexable.</span></span>

<span data-ttu-id="a7bca-123">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a7bca-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a7bca-124">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a7bca-124">Vertex Shader</span></span> | <span data-ttu-id="a7bca-125">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="a7bca-125">Geometry Shader</span></span> | <span data-ttu-id="a7bca-126">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a7bca-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a7bca-127">x</span><span class="sxs-lookup"><span data-stu-id="a7bca-127">x</span></span>             | <span data-ttu-id="a7bca-128">x</span><span class="sxs-lookup"><span data-stu-id="a7bca-128">x</span></span>               | <span data-ttu-id="a7bca-129">x</span><span class="sxs-lookup"><span data-stu-id="a7bca-129">x</span></span>            |



 

<span data-ttu-id="a7bca-130">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="a7bca-130">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="a7bca-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7bca-131">Example</span></span>

<span data-ttu-id="a7bca-132">A continuación se muestra un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a7bca-132">Here is an example.</span></span>


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="a7bca-133">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a7bca-133">Minimum Shader Model</span></span>

<span data-ttu-id="a7bca-134">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a7bca-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a7bca-135">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a7bca-135">Shader Model</span></span>                                              | <span data-ttu-id="a7bca-136">Compatible</span><span class="sxs-lookup"><span data-stu-id="a7bca-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a7bca-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a7bca-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a7bca-138">sí</span><span class="sxs-lookup"><span data-stu-id="a7bca-138">yes</span></span>       |
| [<span data-ttu-id="a7bca-139">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a7bca-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a7bca-140">sí</span><span class="sxs-lookup"><span data-stu-id="a7bca-140">yes</span></span>       |
| [<span data-ttu-id="a7bca-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a7bca-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a7bca-142">sí</span><span class="sxs-lookup"><span data-stu-id="a7bca-142">yes</span></span>       |
| [<span data-ttu-id="a7bca-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7bca-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a7bca-144">no</span><span class="sxs-lookup"><span data-stu-id="a7bca-144">no</span></span>        |
| [<span data-ttu-id="a7bca-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7bca-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a7bca-146">no</span><span class="sxs-lookup"><span data-stu-id="a7bca-146">no</span></span>        |
| [<span data-ttu-id="a7bca-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7bca-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a7bca-148">no</span><span class="sxs-lookup"><span data-stu-id="a7bca-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a7bca-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7bca-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7bca-150">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7bca-150">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





