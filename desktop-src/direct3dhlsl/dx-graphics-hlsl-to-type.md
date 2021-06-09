---
title: Objeto Texture
description: En Direct3D 10, se especifican los muestreadores y las texturas de forma independiente. el muestreo de textura se implementa mediante un objeto templated-texture. Este objeto templated-texture tiene un formato específico, devuelve un tipo específico e implementa varios métodos.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Objeto de textura HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1881ba4a88e97e978e2646c92d276bb9763ffd
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825775"
---
# <a name="texture-object"></a>Objeto Texture

En Direct3D 10, se especifican los muestreadores y las texturas de forma independiente. el muestreo de textura se implementa mediante un objeto templated-texture. Este objeto templated-texture tiene un formato específico, devuelve un tipo específico e implementa varios métodos.

Diferencias entre Direct3D9 y Direct3D10:

- En Direct3D 9, los muestreadores se enlazan a texturas específicas.
- En Direct3D 10, las texturas y los muestreadores son objetos independientes. Cada objeto templated-texture implementa métodos de muestreo de textura que toman la textura y el muestreador como parámetros de entrada.



 

Esta es la sintaxis para crear todos los objetos de textura (excepto los objetos multimuestreo).



| Object1 \[ < *Nombre de* > \] *tipo*; |
|------------------------------------|



 

Los objetos multimuestreo (Texture2DMS y Texture2DMSArray) requieren que el tamaño de la textura se especifique explícitamente y se exprese como el número de muestras.



| Object2 \[ < *Type, Samples* > \] *Name*; |
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
<th>Tipo Object1</th>
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
<td>Textura 1D</td>
</tr>
<tr class="odd">
<td>Texture1DArray</td>
<td>Matriz de texturas 1D</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>Textura 2D</td>
</tr>
<tr class="odd">
<td>Texture2DArray</td>
<td>Matriz de texturas 2D</td>
</tr>
<tr class="even">
<td>Texture3D</td>
<td>Textura 3D</td>
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
<td>Tipo Object2</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>Texture2DMS</td>
<td>Textura multimuestreo 2D</td>
</tr>
<tr class="odd">
<td>Texture2DMSArray</td>
<td>Matriz de texturas multimuestreo 2D</td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li>El tipo Buffer admite la mayoría de los métodos de objeto de textura, excepto GetDimensions.</li>
<li>TextureCubeArray está disponible en el modelo de sombreador 4.1 o superior.</li>
<li>El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o posterior.</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Tipo</em></p></td>
<td><p>Opcional. Cualquier <a href="dx-graphics-hlsl-scalar.md">tipo HLSL escalar o</a> tipo <a href="dx-graphics-hlsl-vector.md"><strong>HLSL vectorial,</strong></a>entre corchetes angulares. El tipo predeterminado es <strong>float4.</strong></p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nombre</em></p></td>
<td><p>Cadena ASCII que especifica el nombre del objeto de textura.</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Muestras</em></p></td>
<td><p>Número de muestras (intervalos entre 1 y 128).</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>Ejemplo 1

Este es un ejemplo de declaración de un objeto de textura.


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>Métodos de objeto texture

Cada objeto de textura implementa determinados métodos; esta es la tabla que enumera todos los métodos. Consulte la página de referencia de cada método para ver qué objetos pueden usar ese método.



| Método texture                                                                     | Descripción                                                                                                       | vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [CalculateLevelOfDetail](dx-graphics-hlsl-to-calculate-lod.md)                    | Calcule el LOD y devuelva un resultado de fijación.                                                                       |          |           |          | x         |          |           |
| [CalculateLevelOfDetailUnclamped](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | Calcule el LOD y devuelva un resultado no reclamado.                                                                    |          |           |          | x         |          |           |
| [Reunir](dx-graphics-hlsl-to-gather.md)                                           | Obtiene las cuatro muestras (solo componente rojo) que se usarían para la interpolación bilineal al muestrear una textura. |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | Obtiene la dimensión de textura para un nivel de mapa mip especificado.                                                           | x        | x         | x        | x         | x        | x         |
| [GetDimensions (MultiSample)](dx-graphics-hlsl-to-getdimensions.md)               | Obtiene la dimensión de textura para un nivel de mapa mip especificado.                                                           |          | x         |          | x         |          | x         |
| [GetSamplePosition](dx-graphics-hlsl-to-get-sample-position.md)                   | Obtiene la posición del ejemplo especificado.                                                                         |          | x         |          | x         |          | x         |
| [Cargar](dx-graphics-hlsl-to-load.md)                                               | Cargar datos sin ningún filtrado ni muestreo.                                                                      | x        | x         | x        | x         | x        | x         |
| [Carga (multimuestreo)](dx-graphics-hlsl-to-load.md)                                 | Cargar datos sin ningún filtrado ni muestreo.                                                                      |          | x         | x        | x         |          | x         |
| [Ejemplo](dx-graphics-hlsl-to-sample.md)                                           | Muestrear una textura.                                                                                                 |          |           | x        | x         |          |           |
| [SampleBias](dx-graphics-hlsl-to-samplebias.md)                                   | Muestrear una textura, después de aplicar el valor de sesgo al nivel de mapa mip.                                              |          |           | x        | x         |          |           |
| [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)                                     | Muestrear una textura mediante un valor de comparación para rechazar muestras.                                                     |          |           | x        | x         |          |           |
| [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | Muestrear una textura (solo mipmap nivel 0), usando un valor de comparación para rechazar muestras.                               | x        | x         | x        | x         | x        | x         |
| [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)                                   | Muestrear una textura mediante un degradado para influir en la forma en que se calcula la ubicación de la muestra.                         | x        | x         | x        | x         | x        | x         |
| [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                 | Muestrear una textura en el nivel de mapa mip especificado.                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>Tipo de valor devuelto

El tipo de valor devuelto de un método de objeto de textura es float4 a menos que se especifique lo contrario, a excepción de los objetos de textura con suavizado de alias multimuestreo que siempre necesitan el tipo y el recuento de muestras especificados. El tipo de valor devuelto es el mismo que el tipo de recurso de textura [**(DXGI \_ FORMAT).**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) En otras palabras, puede ser cualquiera de los tipos siguientes.



| Tipo                       | Description                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FLOAT                      | Float de 32 bits (consulte [Reglas de punto flotante para](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) ver las diferencias con respecto a IEEE float).                            |
| int                        | Entero de 32 bits con signo                                                                                                                                                   |
| unsigned int               | Entero de 32 bits sin signo                                                                                                                                                 |
| snorm                      | Float de 32 bits en el intervalo de -1 a 1 inclusivo (consulte [Reglas](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) de punto flotante para ver las diferencias con respecto a IEEE float). |
| unorm                      | Float de 32 bits en el intervalo 0 a 1 inclusivo (consulte [Reglas](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) de punto flotante para ver las diferencias con respecto a IEEE float).  |
| cualquier tipo de textura o estructura | El número de componentes devueltos debe estar entre 1 y 3 inclusive.                                                                                                    |



 

Además, el tipo de valor devuelto puede ser cualquier tipo de textura, incluida una estructura, pero debe ser menor que 4 componentes, como un tipo float1 que devuelve un componente.

## <a name="default-values-for-missing-components-in-a-texture"></a>Valores predeterminados para los componentes que faltan en una textura

El valor predeterminado de los componentes que faltan en un tipo de recurso de textura es cero para cualquier componente excepto el componente alfa (A); El valor predeterminado de la A que falta es uno. La forma en que este aparece en el sombreador depende del tipo de recurso de textura. Toma la forma del primer componente con tipo que realmente está presente en el tipo de recurso de textura (empezando por la izquierda en orden RGBA). Si este formulario es UNORM o FLOAT, el valor predeterminado de la A que falta es 1,0f. Si el formulario es SINT o UINT, el valor predeterminado de la A que falta es 0x1.

Por ejemplo, cuando un sombreador lee el tipo de recurso de textura [**DXGI \_ FORMAT \_ R24 \_ UNORM \_ X8 \_ TYPELESS,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Los valores predeterminados de G y B son cero y el valor predeterminado de A es 1,0f; cuando un sombreador lee el tipo de recurso de textura [**UINT DXGI \_ FORMAT \_ R16G16, \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) el valor predeterminado para B es cero y el valor predeterminado para A es 0x00000001; cuando un sombreador lee el tipo de recurso de textura [**\_ DXGI FORMAT \_ R16 \_ SINT,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) los valores predeterminados para G y B son cero y el valor predeterminado para A es 0x00000001.

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



## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Modelos de sombreador 4](dx-graphics-hlsl-sm4.md) y superiores | sí       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Shader Model 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

