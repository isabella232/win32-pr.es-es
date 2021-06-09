---
title: Ejemplo (objeto de textura HLSL de DirectX)
description: Muestrea una textura. | Ejemplo (objeto de textura HLSL de DirectX)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2374063d222d06576f720fed2aa7fb714bcccf04
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825752"
---
# <a name="sample-directx-hlsl-texture-object"></a>Ejemplo (objeto de textura HLSL de DirectX)

Muestrea una textura.

&lt;Template Type &gt; Object.Sample( sampler \_ state S, float Location \[ , int Offset \] );

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

## <a name="example"></a>Ejemplo

Este ejemplo de código parcial se basa en el archivo BasicHLSL11.fx del [ejemplo BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).

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

## <a name="remarks"></a>Comentarios

El muestreo de textura usa la posición del texel para buscar un valor de texel. Se puede aplicar un desplazamiento a la posición antes de la búsqueda. El estado del muestreador contiene las opciones de muestreo y filtrado. Este método se puede invocar dentro de un sombreador de píxeles, pero no se admite en un sombreador de vértices o un sombreador de geometría.

Use un desplazamiento solo en un miplevel entero; De lo contrario, puede obtener resultados diferentes en función de la implementación de hardware o la configuración del controlador.

### <a name="calculating-texel-positions"></a>Cálculo de posiciones de textura

Las coordenadas de textura son valores de punto flotante que hacen referencia a los datos de textura, lo que también se conoce como espacio de textura normalizado. Los modos de ajuste de direcciones se aplican en este orden (coordenadas de textura + desplazamientos + modo de ajuste) para modificar las coordenadas de textura fuera del \[ intervalo 0...1. \]

Para las matrices de textura, un valor adicional en el parámetro location especifica un índice en una matriz de texturas. Este índice se trata como un valor float escalado (en lugar del espacio normalizado para coordenadas de textura estándar). La conversión a un índice entero se realiza en el orden siguiente (float + round-to-nearest-even integer + clamp to the array range).

### <a name="applying-texture-coordinate-offsets"></a>Aplicar desplazamientos de coordenadas de textura

El parámetro offset modifica las coordenadas de textura, en el espacio de textura. Aunque las coordenadas de textura son números de punto flotante normalizados, el desplazamiento aplica un desplazamiento entero. Tenga en cuenta también que los desplazamientos de textura deben ser estáticos.

El formato de datos devuelto viene determinado por el formato de textura. Por ejemplo, si el recurso de textura se definió con el formato DXGI FORMAT A8B8G8R8 UNORM SRGB, la operación de muestreo convierte los elementos de textura muestreados de \_ \_ gamma \_ 2.0 a 1.0, filtra y escribe el resultado como un valor de punto flotante en el \_ \[ intervalo 0..1. \]

## <a name="related-topics"></a>Temas relacionados

[Texture-Object](dx-graphics-hlsl-to-type.md)
