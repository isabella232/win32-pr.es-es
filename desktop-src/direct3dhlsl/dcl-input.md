---
title: dcl_input (SM4-ASM)
description: '\_entrada de DCL (SM4-ASM)'
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996981"
---
# <a name="dcl_input-sm4---asm"></a><span data-ttu-id="98ce1-103">\_entrada de DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="98ce1-103">dcl\_input (sm4 - asm)</span></span>

<span data-ttu-id="98ce1-104">Declara un registro de entrada de sombreador.</span><span class="sxs-lookup"><span data-stu-id="98ce1-104">Declares a shader-input register.</span></span>



| <span data-ttu-id="98ce1-105">\_entrada de DCL v *N \[ . Mask \] \[ , \] interpolationMode*</span><span class="sxs-lookup"><span data-stu-id="98ce1-105">dcl\_input v *N\[.mask\]\[, interpolationMode\]*</span></span> |
|-------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98ce1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="98ce1-106">Item</span></span></th>
<th><span data-ttu-id="98ce1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="98ce1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98ce1-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. Mask]</em></span><span class="sxs-lookup"><span data-stu-id="98ce1-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="98ce1-109">de Un registro de datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="98ce1-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="98ce1-110"><em>N</em> es un entero que identifica el número de registro.</span><span class="sxs-lookup"><span data-stu-id="98ce1-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="98ce1-111"><em>[. Mask]</em> es una máscara de componente opcional (. xyzw) que especifica cuál de los componentes de registro se va a usar.</span><span class="sxs-lookup"><span data-stu-id="98ce1-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98ce1-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span><span class="sxs-lookup"><span data-stu-id="98ce1-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="98ce1-113">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="98ce1-113">[in] Optional.</span></span> <span data-ttu-id="98ce1-114">El modo de interpolación, que solo se admite en los registros de entrada del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="98ce1-114">The interpolation mode, which is only honored on pixel shader input registers.</span></span> <span data-ttu-id="98ce1-115">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="98ce1-115">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="98ce1-116">constante: no se interpola entre los valores de registro.</span><span class="sxs-lookup"><span data-stu-id="98ce1-116">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="98ce1-117">lineal: interpolación lineal entre valores de registro.</span><span class="sxs-lookup"><span data-stu-id="98ce1-117">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="98ce1-118">linearCentroid: igual que lineal, pero centroide en el muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="98ce1-118">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="98ce1-119">linearNoperspective: igual que lineal pero sin corrección de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="98ce1-119">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="98ce1-120">linearNoperspectiveCentroid: igual que lineal, centroide se fija al muestreo múltiple, sin corrección de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="98ce1-120">linearNoperspectiveCentroid - same as linear, centroid clamped when multisampling, no perspective correction.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a><span data-ttu-id="98ce1-121">Notas de interpolación</span><span class="sxs-lookup"><span data-stu-id="98ce1-121">Interpolation Notes</span></span>

<span data-ttu-id="98ce1-122">De forma predeterminada, los atributos de vértice se interpolan desde un centro de píxeles al realizar el suavizado de contorno de muestreo.</span><span class="sxs-lookup"><span data-stu-id="98ce1-122">By default, vertex attributes are interpolated from a pixel center when performing multisample antialiasing.</span></span> <span data-ttu-id="98ce1-123">Si no se trata de un centro de píxeles, se extrapola un atributo a un centro de píxeles antes de la interpolación.</span><span class="sxs-lookup"><span data-stu-id="98ce1-123">If a pixel center is not covered, an attribute is extrapolated to a pixel center before interpolation.</span></span>

<span data-ttu-id="98ce1-124">En el caso de un píxel que no esté totalmente cubierto o de un atributo que no cubra un centro de píxeles, puede especificar el muestreo centroide, que fuerza el muestreo para que se produzca en algún lugar dentro del área cubierta del píxel.</span><span class="sxs-lookup"><span data-stu-id="98ce1-124">For a pixel that is not fully covered or an attribute that does not cover a pixel center, you can specify centroid sampling which forces sampling to occur somewhere within the covered area of the pixel.</span></span> <span data-ttu-id="98ce1-125">Dado que se aplica una máscara de ejemplo (si se usa) antes de que se calcule centroide, cualquier ubicación de ejemplo enmascarada por la máscara de ejemplo no se puede elegir como una ubicación de centroide.</span><span class="sxs-lookup"><span data-stu-id="98ce1-125">Because a sample mask (if used) is applied before the centroid is computed, any sample location masked out by the sample mask cannot be chosen as a centroid location.</span></span>

<span data-ttu-id="98ce1-126">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="98ce1-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="98ce1-127">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="98ce1-127">Vertex Shader</span></span> | <span data-ttu-id="98ce1-128">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="98ce1-128">Geometry Shader</span></span> | <span data-ttu-id="98ce1-129">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="98ce1-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="98ce1-130">x</span><span class="sxs-lookup"><span data-stu-id="98ce1-130">x</span></span>             | <span data-ttu-id="98ce1-131">x</span><span class="sxs-lookup"><span data-stu-id="98ce1-131">x</span></span>               | <span data-ttu-id="98ce1-132">x</span><span class="sxs-lookup"><span data-stu-id="98ce1-132">x</span></span>            |



 

<span data-ttu-id="98ce1-133">Para identificar la entrada como un valor del sistema, use [DCL \_ Input \_ SV (SM4-ASM)](dcl-input-sv.md).</span><span class="sxs-lookup"><span data-stu-id="98ce1-133">To identify the input as a system value, use [dcl\_input\_sv (sm4 - asm)](dcl-input-sv.md).</span></span>

<span data-ttu-id="98ce1-134">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="98ce1-134">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="98ce1-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98ce1-135">Example</span></span>

<span data-ttu-id="98ce1-136">Estos son algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="98ce1-136">Here are some examples.</span></span>


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a><span data-ttu-id="98ce1-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="98ce1-137">Minimum Shader Model</span></span>

<span data-ttu-id="98ce1-138">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="98ce1-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="98ce1-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="98ce1-139">Shader Model</span></span>                                              | <span data-ttu-id="98ce1-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="98ce1-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="98ce1-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="98ce1-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="98ce1-142">sí</span><span class="sxs-lookup"><span data-stu-id="98ce1-142">yes</span></span>       |
| [<span data-ttu-id="98ce1-143">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="98ce1-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="98ce1-144">sí</span><span class="sxs-lookup"><span data-stu-id="98ce1-144">yes</span></span>       |
| [<span data-ttu-id="98ce1-145">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="98ce1-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="98ce1-146">sí</span><span class="sxs-lookup"><span data-stu-id="98ce1-146">yes</span></span>       |
| [<span data-ttu-id="98ce1-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98ce1-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="98ce1-148">no</span><span class="sxs-lookup"><span data-stu-id="98ce1-148">no</span></span>        |
| [<span data-ttu-id="98ce1-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98ce1-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="98ce1-150">no</span><span class="sxs-lookup"><span data-stu-id="98ce1-150">no</span></span>        |
| [<span data-ttu-id="98ce1-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98ce1-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="98ce1-152">no</span><span class="sxs-lookup"><span data-stu-id="98ce1-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="98ce1-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98ce1-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98ce1-154">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98ce1-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





