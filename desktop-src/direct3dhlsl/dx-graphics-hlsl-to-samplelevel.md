---
title: SampleLevel (objeto de textura de HLSL de DirectX)
description: Muestrea una textura mediante un desplazamiento de nivel de mipmap.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73cf7bc0c13987099540cecd49519de35b4b7de1
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "104149748"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a>SampleLevel (objeto de textura de HLSL de DirectX)

Muestrea una textura mediante un desplazamiento de nivel de mipmap.



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| &lt;Tipo &gt; de plantilla Object. SampleLevel ( \_ Estado de muestra S, ubicación Float, Float LOD \[ , int offset \] ); |



 

Esta función es similar a [Sample](dx-graphics-hlsl-to-sample.md) , salvo que usa el nivel LOD (en el último componente del parámetro Location) para elegir el nivel de mipmap. Por ejemplo, una textura 2D usa los dos primeros componentes para las coordenadas UV y el tercer componente para el nivel de mipmap.

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

<p> </p>
<p>Si el objeto Texture es una matriz, el último componente es el índice de la matriz.</p></td>
</tr>
<tr class="even">
<td><p><span id="LOD"></span><span id="lod"></span><em>LOD</em></p></td>
<td><p>de Número que especifica el nivel de mipmap. Si el valor es = 0, se usa zero'th (el mapa más grande). El valor fraccionario (si se proporciona) se usa para interpolar entre dos niveles de mipmap.</p></td>
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
| x        | x         | x        | x         | x        | x         |



 

1.  TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.
2.  El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.

## <a name="example"></a>Ejemplo

Este ejemplo de código parcial procede del archivo Instancing. FX en el [ejemplo Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texture-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

