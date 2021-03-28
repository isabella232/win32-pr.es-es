---
title: Ejemplo (objeto de textura HLSL de DirectX)
description: Muestrea una textura. | Ejemplo (objeto de textura de HLSL de DirectX)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ec80d296025684c1bb67642661a31d8cdc119a53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998016"
---
# <a name="sample-directx-hlsl-texture-object"></a>Ejemplo (objeto de textura HLSL de DirectX)

Muestrea una textura.

|                                                                                  |
|----------------------------------------------------------------------------------|
| &lt;Objeto de tipo de plantilla &gt; . ejemplo ( \_ Estado de muestra S, ubicación Float \[ , desplazamiento int \] ); |

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

## <a name="example"></a>Ejemplo

Este ejemplo de código parcial se basa en el archivo BasicHLSL11. FX en el [ejemplo BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a>Observaciones

El muestreo de textura usa la posición textura para buscar un valor textura. Se puede aplicar un desplazamiento a la posición antes de la búsqueda. El estado de muestra contiene las opciones de muestreo y filtrado. Este método se puede invocar dentro de un sombreador de píxeles, pero no se admite en un sombreador de vértices o un sombreador de geometría.

Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados diferentes en función de la implementación del hardware o de la configuración del controlador.

### <a name="calculating-texel-positions"></a>Calcular las posiciones de textura

Las coordenadas de textura son valores de punto flotante que hacen referencia a los datos de textura, lo que también se conoce como espacio de textura normalizado. Los modos de ajuste de direcciones se aplican en este orden (coordenadas de textura + desplazamientos + modo de ajuste) para modificar las coordenadas de textura fuera del \[ intervalo de 0... 1 \] .

En el caso de las matrices de textura, un valor adicional en el parámetro Location especifica un índice en una matriz de textura. Este índice se trata como un valor de punto flotante escalado (en lugar del espacio normalizado para las coordenadas de textura estándar). La conversión a un índice de entero se realiza en el orden siguiente (float + Round-to-Even Integer + Clamp al intervalo de la matriz).

### <a name="applying-texture-coordinate-offsets"></a>Aplicar desplazamientos de coordenadas de textura

El parámetro offset modifica las coordenadas de textura, en el espacio textura. Aunque las coordenadas de textura son números de punto flotante normalizados, el desplazamiento aplica un desplazamiento entero. Tenga en cuenta también que los desplazamientos de textura deben ser estáticos.

El formato de datos devuelto viene determinado por el formato de textura. Por ejemplo, si el recurso de textura se definió con el formato de DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, la operación de muestreo convierte textura muestreadas de gamma 2,0 a 1,0, filtrar y escribe el resultado como un valor de punto flotante en el intervalo \[ 0.. 1 \] .

## <a name="related-topics"></a>Temas relacionados

[Texture-objeto](dx-graphics-hlsl-to-type.md)
