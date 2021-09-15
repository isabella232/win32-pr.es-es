---
title: SampleBias (objeto de textura HLSL de DirectX)
description: Muestrea una textura después de aplicar el sesgo de entrada al nivel de mapa mip.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a279a92db9d38c8f0a8e80edbd87ec667d580d05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573797"
---
# <a name="samplebias-directx-hlsl-texture-object"></a>SampleBias (objeto de textura HLSL de DirectX)

Muestrea una textura después de aplicar el sesgo de entrada al nivel de mapa mip.

&lt;Template Type &gt; Object.SampleBias( sampler \_ state S, float Location, float Bias \[ , int Offset \] );



 

## <a name="parameters"></a>Parámetros



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em><br/></td>
<td>Cualquier <a href="dx-graphics-hlsl-to-type.md">tipo de objeto de</a> textura (excepto Texture2DMS y Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>[in] Un <a href="dx-graphics-hlsl-sampler.md">estado sampler</a>. Se trata de un objeto declarado en un archivo de efecto que contiene asignaciones de estado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Ubicación</em><br/></td>
<td>[in] Coordenadas de textura. El tipo de argumento depende del tipo texture-object. <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object type</th>
<th>Tipo de parámetro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D</td>
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture1DArray, Texture2D</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture2DArray, Texture3D, TextureCube</td>
<td>float3</td>
</tr>
<tr class="even">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Predisposición</em></p></td>
<td><p>[in] El valor de sesgo, que es un número de punto flotante entre -16,0 y 15,99, se aplica a un nivel de mip antes del muestreo.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Compensar</em></p></td>
<td><p>[in] Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura; el desplazamiento se aplica a la ubicación antes del muestreo. Los desplazamientos de textura deben ser estáticos. El tipo de argumento depende del tipo texture-object. Para obtener más información, vea <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Aplicar desplazamientos de coordenadas de textura.</a></p>

<table>
<thead>
<tr class="header">
<th>Texture-Object type</th>
<th>Tipo de parámetro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>int</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>int3</td>
</tr>
<tr class="even">
<td>TextureCube, TextureCubeArray </td>
<td>no admitido</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Valor devuelto

El tipo de plantilla de la textura, que puede ser un vector de uno o varios componentes. El formato se basa en EL [**FORMATO DXGI de la \_ textura.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x        | x         |          |           |



 

1.  TextureCubeArray está disponible en Shader Model 4.1 o superior.
2.  El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o posterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

