---
title: SampleBias (objeto de textura de HLSL de DirectX)
description: Muestrea una textura, después de aplicar la diferencia de entrada al nivel de mipmap.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e710b8a6c7dd2983c6d0c635d16356f95d0b4fe7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "104421684"
---
# <a name="samplebias-directx-hlsl-texture-object"></a>SampleBias (objeto de textura de HLSL de DirectX)

Muestrea una textura, después de aplicar la diferencia de entrada al nivel de mipmap.



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| &lt;Tipo &gt; de plantilla Object. SampleBias ( \_ Estado de muestra S, ubicación Float, inclinación Float \[ , desplazamiento int \] ); |



 

## <a name="parameters"></a>Parámetros



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
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em><br/></td>
<td>Cualquier tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (excepto Texture2DMS y Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>Seg</em><br/></td>
<td>de Un <a href="dx-graphics-hlsl-sampler.md">Estado de muestra</a>. Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Cód</em><br/></td>
<td>de Coordenadas de textura. El tipo de argumento depende del tipo de objeto de textura. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo de Texture-Object</th>
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
<td><p><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Parcial</em></p></td>
<td><p>de El valor de diferencia, que es un número de punto flotante entre-16,0 y 15,99, se aplica a un nivel de MIP antes del muestreo.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Posición</em></p></td>
<td><p>de Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo. Los desplazamientos de textura deben ser estáticos. El tipo de argumento depende del tipo de objeto de textura. Para obtener más información, vea <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">aplicar desplazamientos de coordenadas de textura</a>.</p>

<table>
<thead>
<tr class="header">
<th>Tipo de Texture-Object</th>
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

Tipo de plantilla de la textura, que puede ser un vector de un solo componente o de varios componentes. El formato se basa en el formato de [**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)de la textura.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x        | x         |          |           |



 

1.  TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.
2.  El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texture-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

