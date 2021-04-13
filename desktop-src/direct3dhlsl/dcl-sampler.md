---
title: dcl_sampler (SM4-ASM)
description: '\_muestrario de DCL (SM4-ASM)'
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104421512"
---
# <a name="dcl_sampler-sm4---asm"></a><span data-ttu-id="31b39-103">\_muestrario de DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="31b39-103">dcl\_sampler (sm4 - asm)</span></span>

<span data-ttu-id="31b39-104">Declara un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="31b39-104">Declares a sampler register.</span></span>



| <span data-ttu-id="31b39-105">\_muestra SN de DCL, modo</span><span class="sxs-lookup"><span data-stu-id="31b39-105">dcl\_sampler sN, mode</span></span> |
|-----------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31b39-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="31b39-106">Item</span></span></th>
<th><span data-ttu-id="31b39-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="31b39-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31b39-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span><span class="sxs-lookup"><span data-stu-id="31b39-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span></span><br/></td>
<td><span data-ttu-id="31b39-109">de Un registro de muestra, donde <em>N</em> es un entero que denota el número de registro.</span><span class="sxs-lookup"><span data-stu-id="31b39-109">[in] A sampler register, where <em>N</em> is an integer that denotes the register number.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31b39-110"><span id="mode"></span><span id="MODE"></span><em>modo</em></span><span class="sxs-lookup"><span data-stu-id="31b39-110"><span id="mode"></span><span id="MODE"></span><em>mode</em></span></span><br/></td>
<td><span data-ttu-id="31b39-111">de Un modo de muestra, que restringe qué Estados de muestra (enumerados en los miembros de <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) se admiten.</span><span class="sxs-lookup"><span data-stu-id="31b39-111">[in] A sampler mode, which constrains which sampler states (listed in the members of <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) are honored.</span></span> <span data-ttu-id="31b39-112">En la tabla siguiente se enumeran los modos y los Estados.</span><span class="sxs-lookup"><span data-stu-id="31b39-112">The modes and states are listed in the following table.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="31b39-113">Mode</span><span class="sxs-lookup"><span data-stu-id="31b39-113">Mode</span></span></th>
<th><span data-ttu-id="31b39-114">Estados de muestra admitidos</span><span class="sxs-lookup"><span data-stu-id="31b39-114">Sampler States Honored</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31b39-115">default</span><span class="sxs-lookup"><span data-stu-id="31b39-115">default</span></span></td>
<td><span data-ttu-id="31b39-116"><em>Filtro</em> (no puede usar los valores _COMPARISON o _TEXT), <em>AddressU/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="31b39-116"><em>Filter</em> (may not use the _COMPARISON or _TEXT values), <em>AddressU/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31b39-117">comparación</span><span class="sxs-lookup"><span data-stu-id="31b39-117">comparison</span></span></td>
<td><span data-ttu-id="31b39-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD, MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="31b39-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD,MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31b39-119">monocromo</span><span class="sxs-lookup"><span data-stu-id="31b39-119">mono</span></span></td>
<td><span data-ttu-id="31b39-120"><em>Filter</em> (debe ser uno de los valores _TEXT), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (estos dos Estados son estado de dispositivo global), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span><span class="sxs-lookup"><span data-stu-id="31b39-120"><em>Filter</em> (must be one of the _TEXT values), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (these two states are global device state), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="31b39-121">El modo restringe las instrucciones de ejemplo que se pueden usar; en esta tabla se enumeran los métodos de objeto de textura que se admiten para cada modo.</span><span class="sxs-lookup"><span data-stu-id="31b39-121">The mode restricts the sample instructions that can be used; this table lists the texture-object methods that are supported for each mode.</span></span>



| <span data-ttu-id="31b39-122">Un muestreador que funciona en este modo</span><span class="sxs-lookup"><span data-stu-id="31b39-122">A Sampler Operating in this Mode</span></span> | <span data-ttu-id="31b39-123">Puede utilizar estos métodos Texture-Object</span><span class="sxs-lookup"><span data-stu-id="31b39-123">Can Use these Texture-Object Methods</span></span>                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31b39-124">default</span><span class="sxs-lookup"><span data-stu-id="31b39-124">default</span></span>                          | <span data-ttu-id="31b39-125">[Ejemplo](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span><span class="sxs-lookup"><span data-stu-id="31b39-125">[Sample](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span></span> |
| <span data-ttu-id="31b39-126">comparación</span><span class="sxs-lookup"><span data-stu-id="31b39-126">comparison</span></span>                       | <span data-ttu-id="31b39-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span><span class="sxs-lookup"><span data-stu-id="31b39-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span></span>                               |
| <span data-ttu-id="31b39-128">monocromo</span><span class="sxs-lookup"><span data-stu-id="31b39-128">mono</span></span>                             | [<span data-ttu-id="31b39-129">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="31b39-129">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

<span data-ttu-id="31b39-130">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="31b39-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="31b39-131">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="31b39-131">Vertex Shader</span></span> | <span data-ttu-id="31b39-132">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="31b39-132">Geometry Shader</span></span> | <span data-ttu-id="31b39-133">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="31b39-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="31b39-134">x</span><span class="sxs-lookup"><span data-stu-id="31b39-134">x</span></span>             | <span data-ttu-id="31b39-135">x</span><span class="sxs-lookup"><span data-stu-id="31b39-135">x</span></span>               | <span data-ttu-id="31b39-136">x1\*</span><span class="sxs-lookup"><span data-stu-id="31b39-136">x\*</span></span>          |



 

<span data-ttu-id="31b39-137">\* -El uso de una muestra en modo mono solo se admite en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="31b39-137">\* - Using a sampler in mono mode is supported only in a pixel shader.</span></span>

<span data-ttu-id="31b39-138">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="31b39-138">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="31b39-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31b39-139">Example</span></span>

<span data-ttu-id="31b39-140">A continuación se muestra un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="31b39-140">Here is an example.</span></span>


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a><span data-ttu-id="31b39-141">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="31b39-141">Minimum Shader Model</span></span>

<span data-ttu-id="31b39-142">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="31b39-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="31b39-143">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="31b39-143">Shader Model</span></span>                                              | <span data-ttu-id="31b39-144">Compatible</span><span class="sxs-lookup"><span data-stu-id="31b39-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="31b39-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="31b39-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="31b39-146">sí</span><span class="sxs-lookup"><span data-stu-id="31b39-146">yes</span></span>       |
| [<span data-ttu-id="31b39-147">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="31b39-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="31b39-148">sí</span><span class="sxs-lookup"><span data-stu-id="31b39-148">yes</span></span>       |
| [<span data-ttu-id="31b39-149">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="31b39-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="31b39-150">sí</span><span class="sxs-lookup"><span data-stu-id="31b39-150">yes</span></span>       |
| [<span data-ttu-id="31b39-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31b39-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="31b39-152">no</span><span class="sxs-lookup"><span data-stu-id="31b39-152">no</span></span>        |
| [<span data-ttu-id="31b39-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31b39-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="31b39-154">no</span><span class="sxs-lookup"><span data-stu-id="31b39-154">no</span></span>        |
| [<span data-ttu-id="31b39-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31b39-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="31b39-156">no</span><span class="sxs-lookup"><span data-stu-id="31b39-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="31b39-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31b39-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31b39-158">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="31b39-158">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

