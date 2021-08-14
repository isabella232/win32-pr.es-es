---
title: dcl_sampler (sm4 - asm)
description: dcl \_ sampler (sm4 - asm)
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e0e04558c9ca1c10f89e924605c8999a7f7346d2278850d7cd6449968fd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515544"
---
# <a name="dcl_sampler-sm4---asm"></a>dcl \_ sampler (sm4 - asm)

Declara un registro de sampler.



| dcl \_ sampler sN, mode |
|-----------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em><br/></td>
<td>[in] Registro de muestreador, donde <em>N</em> es un entero que denota el número de registro.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>Modo</em><br/></td>
<td>[in] Modo sampler, que restringe los estados del muestreador (enumerados en los miembros de <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) se respetan. Los modos y estados se enumeran en la tabla siguiente.<br/> 
<table>
<thead>
<tr class="header">
<th>Modo</th>
<th>Estados del muestreador que se respetan</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>default</td>
<td><em>Filtro</em> (no puede usar los valores _COMPARISON o _TEXT), <em>AddressU/V/W,</em> <em>MinLOD/MaxLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy,</em> <em>BorderColor[4]</em></td>
</tr>
<tr class="even">
<td>comparación</td>
<td><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W,</em> <em>MinLOD,MaxLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></td>
</tr>
<tr class="odd">
<td>mono</td>
<td><em>Filtro</em> (debe ser uno de los valores de _TEXT), <em>MonoFilterWidth,</em> <em>MonoFilterHeight</em> (estos dos estados son estado global del dispositivo), <em>MinLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

El modo restringe las instrucciones de ejemplo que se pueden usar; en esta tabla se enumeran los métodos de objeto de textura que se admiten para cada modo.



| Un sampler que funciona en este modo | Puede usar estos Texture-Object métodos                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| default                          | [Ejemplo,](dx-graphics-hlsl-to-sample.md) [SampleLevel,](dx-graphics-hlsl-to-samplelevel.md) [SampleGrad](dx-graphics-hlsl-to-samplegrad.md) |
| comparación                       | [SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| mono                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | X\*          |



 

\* - El uso de un muestreador en modo mono solo se admite en un sombreador de píxeles.

Esta instrucción se incluye para ayudar a depurar un sombreador en ensamblado; No se puede crear un sombreador en el lenguaje de ensamblado mediante El modelo de sombreador 4.

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo:


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

