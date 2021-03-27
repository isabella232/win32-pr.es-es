---
title: Objeto Texture
description: En Direct3D 10, los ejemplos y las texturas se especifican de forma independiente. el muestreo de textura se implementa mediante el uso de un objeto de textura con plantilla. Este objeto de textura con plantilla tiene un formato específico, devuelve un tipo específico e implementa varios métodos.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- HLSL de objeto de textura
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104280217"
---
# <a name="texture-object"></a>Objeto Texture

En Direct3D 10, los ejemplos y las texturas se especifican de forma independiente. el muestreo de textura se implementa mediante el uso de un objeto de textura con plantilla. Este objeto de textura con plantilla tiene un formato específico, devuelve un tipo específico e implementa varios métodos.




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D9 y Direct3D10: en Direct3D 9, los muestreadores se enlazan a texturas específicas; en Direct3D 10, las texturas y los muestreadores son objetos independientes. Cada objeto de textura con plantilla implementa métodos de muestreo de textura que toman la textura y la muestra como parámetros de entrada.<br/> |



 

Esta es la sintaxis para crear todos los objetos de textura (excepto los objetos multimuestreados).



| Nombre del \[ < *tipo* de Object1 > \] ; |
|------------------------------------|



 

Los objetos multimuestreados (Texture2DMS y Texture2DMSArray) requieren que el tamaño de la textura se indique explícitamente y se exprese como el número de muestras.



| Objeto2 \[ < *Type, samples* > \] *Name*; |
|---------------------------------------------|



 

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
<td>Objeto de textura. Debe ser uno de los tipos siguientes. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo de Object1</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Buffer</td>
<td>Buffer </td>
</tr>
<tr class="even">
<td>Texture1D</td>
<td>textura 1D</td>
</tr>
<tr class="odd">
<td>Texture1DArray</td>
<td>Matriz de texturas 1D</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>textura 2D</td>
</tr>
<tr class="odd">
<td>Texture2DArray</td>
<td>Matriz de texturas 2D</td>
</tr>
<tr class="even">
<td>Texture3D</td>
<td>textura 3D</td>
</tr>
<tr class="odd">
<td>TextureCube</td>
<td>Textura del cubo</td>
</tr>
<tr class="even">
<td>TextureCubeArray  </td>
<td>Matriz de texturas de cubo</td>
</tr>
<tr class="odd">
<td>Tipo objeto2</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>Texture2DMS</td>
<td>textura multimuestreada 2D</td>
</tr>
<tr class="odd">
<td>Texture2DMSArray</td>
<td>Matriz de texturas multimuestreadas en 2D</td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li>El tipo de búfer admite la mayoría de los métodos de objeto Texture excepto Getdimensions (.</li>
<li>TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.</li>
<li>El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Automáticamente</em></p></td>
<td><p>Opcional. Cualquier tipo HLSL <a href="dx-graphics-hlsl-scalar.md">escalar</a> o <a href="dx-graphics-hlsl-vector.md"><strong>tipo HLSL vectorial</strong></a>, rodeado de corchetes angulares. El tipo predeterminado es <strong>FLOAT4</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></p></td>
<td><p>Cadena ASCII que especifica el nombre del objeto de textura.</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Assembl</em></p></td>
<td><p>El número de muestras (oscila entre 1 y 128).</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>Ejemplo 1

Este es un ejemplo de cómo declarar un objeto Texture.


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>Métodos de objeto Texture

Cada objeto Texture implementa determinados métodos; Esta es la tabla en la que se enumeran todos los métodos. Vea la página de referencia de cada método para ver qué objetos pueden usar ese método.



| Texture (método)                                                                     | Descripción                                                                                                       | vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [CalculateLevelOfDetail](dx-graphics-hlsl-to-calculate-lod.md)                    | Calcule el LOD y devuelva un resultado de compresión.                                                                       |          |           |          | x         |          |           |
| [CalculateLevelOfDetailUnclamped](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | Calcule el LOD y devuelva un resultado desgarrado.                                                                    |          |           |          | x         |          |           |
| [Recopilar](dx-graphics-hlsl-to-gather.md)                                           | Obtiene los cuatro ejemplos (solo componente rojo) que se utilizarían para la interpolación bilineal al realizar el muestreo de una textura. |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | Obtiene la dimensión de textura para un nivel de mipmap especificado.                                                           | x        | x         | x        | x         | x        | x         |
| [Getdimensions ((Multimuestra)](dx-graphics-hlsl-to-getdimensions.md)               | Obtiene la dimensión de textura para un nivel de mipmap especificado.                                                           |          | x         |          | x         |          | x         |
| [GetSamplePosition](dx-graphics-hlsl-to-get-sample-position.md)                   | Obtiene la posición del ejemplo especificado.                                                                         |          | x         |          | x         |          | x         |
| [Cargar](dx-graphics-hlsl-to-load.md)                                               | Cargar datos sin ningún filtrado o muestreo.                                                                      | x        | x         | x        | x         | x        | x         |
| [Load (Multimuestra)](dx-graphics-hlsl-to-load.md)                                 | Cargar datos sin ningún filtrado o muestreo.                                                                      |          | x         | x        | x         |          | x         |
| [Ejemplo](dx-graphics-hlsl-to-sample.md)                                           | Muestra una textura.                                                                                                 |          |           | x        | x         |          |           |
| [SampleBias](dx-graphics-hlsl-to-samplebias.md)                                   | Muestra una textura, después de aplicar el valor de diferencia al nivel de mipmap.                                              |          |           | x        | x         |          |           |
| [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)                                     | Muestre una textura con un valor de comparación para rechazar ejemplos.                                                     |          |           | x        | x         |          |           |
| [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | Muestra una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar muestras.                               | x        | x         | x        | x         | x        | x         |
| [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)                                   | Muestra una textura con un degradado para influir en la forma en que se calcula la ubicación de ejemplo.                         | x        | x         | x        | x         | x        | x         |
| [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                 | Muestra una textura en el nivel de mipmap especificado.                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>Tipo de valor devuelto

El tipo de valor devuelto de un método de objeto Texture es FLOAT4, a menos que se especifique lo contrario, con la excepción de los objetos de textura con suavizado de contorno múltiple que siempre necesitan el tipo y el recuento de muestras especificado. El tipo de valor devuelto es el mismo que el tipo de recurso de textura ([**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). En otras palabras, puede ser cualquiera de los siguientes tipos.



| Tipo                       | Description                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FLOAT                      | 32 bits Float (vea [reglas de punto flotante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para conocer las diferencias de IEEE float)                            |
| int                        | Entero de 32 bits con signo                                                                                                                                                   |
| unsigned int               | Entero de 32 bits sin signo                                                                                                                                                 |
| snorm                      | 32 bits Float en el intervalo comprendido entre 1 y 1, ambos inclusive (vea [reglas de punto flotante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para conocer las diferencias de IEEE float) |
| unorm                      | 32 bits Float en el intervalo de 0 a 1, ambos inclusive (vea [reglas de punto flotante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para conocer las diferencias de IEEE float)  |
| cualquier tipo de textura o struct | El número de componentes devueltos debe estar entre 1 y 3, ambos inclusive.                                                                                                    |



 

Además, el tipo de valor devuelto puede ser cualquier tipo de textura, incluida una estructura, pero debe ser inferior a 4 componentes, como un tipo float1, que devuelve un componente.

## <a name="default-values-for-missing-components-in-a-texture"></a>Valores predeterminados para los componentes que faltan en una textura

El valor predeterminado para los componentes que faltan en un tipo de recurso de textura es cero para cualquier componente excepto el componente alfa (A); el valor predeterminado para el que falta un es uno. La forma en que este aparece en el sombreador depende del tipo de recurso de textura. Adopta la forma del primer componente con tipo que está realmente presente en el tipo de recurso de textura (a partir de la izquierda en el orden RGBA). Si este formulario es UNORM o FLOAT, el valor predeterminado para el que falta es 1,0 f. Si el formulario es SINT o UINT, el valor predeterminado para el que falta es 0x1.

Por ejemplo, cuando un sombreador lee el tipo de recurso de textura [**\_ \_ \_ \_ \_ sin tipo de formato DXGI R24 UNORM X8**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , los valores predeterminados para G y B son cero y el valor predeterminado para es 1,0 f; cuando un sombreador lee el tipo de recurso [**\_ \_ R16G16 \_ uint de formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , el valor predeterminado de B es cero y el valor predeterminado de un es 0x00000001; cuando un sombreador lee el tipo de recurso de textura [**\_ formato DXGI \_ R16 \_ San**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , los valores predeterminados para G y B son cero y el valor predeterminado para es 0x00000001.

## <a name="example-2"></a>Ejemplo 2

Este es un ejemplo de muestreo de textura mediante un método de textura.


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores | sí       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

