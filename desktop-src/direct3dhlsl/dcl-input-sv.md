---
title: dcl_input_sv (SM4-ASM)
description: '\_ \_ SV de entrada de DCL (SM4-ASM)'
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785021"
---
# <a name="dcl_input_sv-sm4---asm"></a><span data-ttu-id="80a76-103">\_ \_ SV de entrada de DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="80a76-103">dcl\_input\_sv (sm4 - asm)</span></span>

<span data-ttu-id="80a76-104">Declara un registro de entrada de sombreador que espera que se proporcione un [valor del sistema](dx-graphics-hlsl-semantics.md) desde una fase anterior.</span><span class="sxs-lookup"><span data-stu-id="80a76-104">Declares a shader-input register that expects a [system-value](dx-graphics-hlsl-semantics.md) to be provided from a preceding stage.</span></span>



| <span data-ttu-id="80a76-105">\_entrada \_ de DCL SV v *N \[ . \] Mask*, *systemValueName \[ , \] interpolationMode*</span><span class="sxs-lookup"><span data-stu-id="80a76-105">dcl\_input\_sv v *N\[.mask\]*, *systemValueName\[, interpolationMode\]*</span></span> |
|------------------------------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80a76-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="80a76-106">Item</span></span></th>
<th><span data-ttu-id="80a76-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="80a76-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80a76-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. Mask]</em></span><span class="sxs-lookup"><span data-stu-id="80a76-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="80a76-109">de Un registro de datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="80a76-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="80a76-110"><em>N</em> es un entero que identifica el número de registro.</span><span class="sxs-lookup"><span data-stu-id="80a76-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="80a76-111"><em>[. Mask]</em> es una máscara de componente opcional (. xyzw) que especifica cuál de los componentes de registro se va a usar.</span><span class="sxs-lookup"><span data-stu-id="80a76-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80a76-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span><span class="sxs-lookup"><span data-stu-id="80a76-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span></span><br/></td>
<td><span data-ttu-id="80a76-113">de Nombre del valor del sistema que es una cadena (vea <a href="dx-graphics-hlsl-semantics.md">semántica de valor del sistema</a>) sin el &quot; &quot; prefijo SV_.</span><span class="sxs-lookup"><span data-stu-id="80a76-113">[in] The system-value name which is a string (see <a href="dx-graphics-hlsl-semantics.md">system-value semantics</a>) without the &quot;SV_&quot; prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80a76-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="80a76-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="80a76-115">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="80a76-115">[in] Optional.</span></span> <span data-ttu-id="80a76-116">El modo de interpolación que afecta al modo en que se calculan los valores durante la rasterización; el modo solo lo usa un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="80a76-116">The interpolation mode which affects how values are calculated during rasterization; the mode is only used by a pixel shader.</span></span> <span data-ttu-id="80a76-117">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="80a76-117">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="80a76-118">constante: no se interpola entre los valores de registro.</span><span class="sxs-lookup"><span data-stu-id="80a76-118">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="80a76-119">lineal: interpolación lineal entre valores de registro.</span><span class="sxs-lookup"><span data-stu-id="80a76-119">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="80a76-120">linearCentroid: igual que lineal, pero centroide en el muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="80a76-120">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="80a76-121">linearNoperspective: igual que lineal pero sin corrección de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="80a76-121">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="80a76-122">linearNoperspectiveCentroid: igual que lineal, pero sin corrección de la perspectiva y centroide en el muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="80a76-122">linearNoperspectiveCentroid - same as linear but with no perspective correction and centroid clamped when multisampling.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="80a76-123">Una máscara de componente para una declaración de valor del sistema puede ser cualquier subconjunto adecuado de \[ xyzw \] ; las declaraciones no pueden superponerse (cada declaración debe seguir a la secuencia xyzw).</span><span class="sxs-lookup"><span data-stu-id="80a76-123">A component mask for a system-value declaration can be any appropriate subset of \[xyzw\]; declarations may not overlap (each declaration must follow the sequence xyzw).</span></span> <span data-ttu-id="80a76-124">Al declarar valores del sistema escalares (distancia de clip y distancia de selección, por ejemplo), puede declarar varios valores del sistema en un solo registro.</span><span class="sxs-lookup"><span data-stu-id="80a76-124">When declaring scalar system values (clip distance and cull distance for example), you can declare multiple system values in a single register.</span></span> <span data-ttu-id="80a76-125">Si lo hace, asegúrese de que otros modificadores, como los modos de interpolación coinciden.</span><span class="sxs-lookup"><span data-stu-id="80a76-125">If you do so, make sure other modifiers like the interpolation modes match.</span></span>

<span data-ttu-id="80a76-126">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="80a76-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="80a76-127">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="80a76-127">Vertex Shader</span></span> | <span data-ttu-id="80a76-128">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="80a76-128">Geometry Shader</span></span> | <span data-ttu-id="80a76-129">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="80a76-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="80a76-130">x</span><span class="sxs-lookup"><span data-stu-id="80a76-130">x</span></span>             | <span data-ttu-id="80a76-131">x</span><span class="sxs-lookup"><span data-stu-id="80a76-131">x</span></span>               | <span data-ttu-id="80a76-132">x</span><span class="sxs-lookup"><span data-stu-id="80a76-132">x</span></span>            |



 

<span data-ttu-id="80a76-133">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="80a76-133">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="80a76-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="80a76-134">Example</span></span>

<span data-ttu-id="80a76-135">A continuación se muestran algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="80a76-135">Here are some examples:</span></span>


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a><span data-ttu-id="80a76-136">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="80a76-136">Minimum Shader Model</span></span>

<span data-ttu-id="80a76-137">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="80a76-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="80a76-138">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="80a76-138">Shader Model</span></span>                                              | <span data-ttu-id="80a76-139">Compatible</span><span class="sxs-lookup"><span data-stu-id="80a76-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="80a76-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="80a76-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="80a76-141">sí</span><span class="sxs-lookup"><span data-stu-id="80a76-141">yes</span></span>       |
| [<span data-ttu-id="80a76-142">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="80a76-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="80a76-143">sí</span><span class="sxs-lookup"><span data-stu-id="80a76-143">yes</span></span>       |
| [<span data-ttu-id="80a76-144">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="80a76-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="80a76-145">sí</span><span class="sxs-lookup"><span data-stu-id="80a76-145">yes</span></span>       |
| [<span data-ttu-id="80a76-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80a76-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="80a76-147">no</span><span class="sxs-lookup"><span data-stu-id="80a76-147">no</span></span>        |
| [<span data-ttu-id="80a76-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80a76-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="80a76-149">no</span><span class="sxs-lookup"><span data-stu-id="80a76-149">no</span></span>        |
| [<span data-ttu-id="80a76-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80a76-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="80a76-151">no</span><span class="sxs-lookup"><span data-stu-id="80a76-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="80a76-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80a76-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80a76-153">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80a76-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





