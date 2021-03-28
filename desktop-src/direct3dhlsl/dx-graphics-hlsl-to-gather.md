---
title: Recopilar (objeto de textura de HLSL de DirectX)
description: Obtiene los cuatro ejemplos (solo componente rojo) que se utilizarían para la interpolación bilineal al realizar el muestreo de una textura.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16c568afc3cfdc0d26472d50599abdf3dbd08301
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "104984123"
---
# <a name="gather-directx-hlsl-texture-object"></a>Recopilar (objeto de textura de HLSL de DirectX)

Obtiene los cuatro ejemplos (solo componente rojo) que se utilizarían para la interpolación bilineal al realizar el muestreo de una textura.



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| &lt;Tipo de plantilla &gt; 4 Object. Gather ( \_ Estado de muestra S, float2 \| 3 \| 4 ubicación \[ , desplazamiento de INT2 \] ); |



 

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
<td>Se admiten los siguientes tipos <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> : Texture2D, Texture2DArray, TextureCube, TextureCubeArray.<br/></td>
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
<td>Texture2D</td>
<td>float2</td>
</tr>
<tr class="even">
<td>Texture2DArray, TextureCube</td>
<td>float3</td>
</tr>
<tr class="odd">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Posición</em></p></td>
<td><p>de Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo. Los desplazamientos de textura deben ser estáticos. El tipo de argumento depende del tipo de objeto de textura. Para obtener más información, vea <a href="dx-graphics-hlsl-to-sample.md">aplicar desplazamientos de coordenadas de textura</a>.</p>

<table>
<thead>
<tr class="header">
<th>Tipo de Texture-Object</th>
<th>Tipo de parámetro</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
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

Un vector de cuatro componentes, con cuatro componentes de datos rojos, cuyo tipo es el mismo que el tipo de plantilla de la textura.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

1.  TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.
2.  El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.

## <a name="example"></a>Ejemplo


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texture-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





