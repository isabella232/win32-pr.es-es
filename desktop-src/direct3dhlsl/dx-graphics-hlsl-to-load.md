---
title: Cargar (objeto de textura HLSL de DirectX)
description: Lee datos de textura sin ningún filtrado ni muestreo.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01e8fccbf461befd8016d813098a542a98cdc858
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887221"
---
# <a name="load-directx-hlsl-texture-object"></a>Cargar (objeto de textura HLSL de DirectX)

Lee datos de textura sin ningún filtrado ni muestreo.



<table>
<tbody>
<tr class="odd">
<td>ret Object.Load(<dl> typeX Location,<br />
[typeX SampleIndex, ]<br />
[typeX Offset ]<br />
</dl>);</td>
</tr>
</tbody>
</table>

typeX indica que hay cuatro tipos posibles: **int**, **int2,** **int3** o **int4.**

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*
</dt> <dd>

Un [tipo de objeto de](dx-graphics-hlsl-to-type.md) textura (excepto TextureCube o TextureCubeArray).

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Ubicación*
</dt> <dd>

\[en \] Coordenadas de textura; el último componente especifica el nivel de mapa mip. Este método usa un sistema de coordenadas basado en 0 y no un sistema UV 0.0-1.0. El tipo de argumento depende del tipo texture-object.



| Tipo de objeto                                  | Tipo de parámetro |
|----------------------------------------------|----------------|
| Buffer                                       | int            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray, Texture 2D, Texture2DMSArray | int3           |
| Texture2DArray, Texture3D                    | int4           |



 

Por ejemplo, para acceder a una textura 2D, proporcione coordenadas UV para los dos primeros componentes y un nivel de mapa mip para el tercer componente.

> [!Note]  
> Cuando una o varias de las coordenadas de *Ubicación* superan las dimensiones de nivel mipmap u, v o w de la textura, **Load** devuelve cero en todos los componentes. Direct3D garantiza que se devuelva cero para cualquier recurso al que se acceda fuera de los límites.

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*
</dt> <dd>

\[en \] Un índice de muestreo opcional.



| Tipo de textura                                                                                                   | Tipo de parámetro |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray | no admitido  |
| Texture2DMS, Texture2DMSArray¹                                                                                 | int            |



 

> [!Note]  
> *SampleIndex* solo está disponible para texturas de varias muestras.

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Compensar*
</dt> <dd>

\[en \] Un desplazamiento opcional aplicado a las coordenadas de textura antes del muestreo. El tipo de desplazamiento depende del tipo de objeto de textura y debe ser estático.



| Tipo de textura                                             | Tipo de parámetro |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | int            |
| Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | int3           |



 

> [!Note]  
> Si usa Offset *con* texturas de varias muestras, también debe especificar *SampleIndex*.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El tipo de valor devuelto coincide con el tipo de la *declaración object.* Por ejemplo, un objeto Texture2D que se declaró como "Texture2d &lt; uint4 myTexture;" tiene un valor devuelto de &gt; **tipo uint4**.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1¹ | ps \_ 4 \_ 0 | ps \_ 4 \_ 1¹ | gs \_ 4 \_ 0 | gs \_ 4 \_ 1¹ |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o superior.

## <a name="example"></a>Ejemplo

Este ejemplo de código parcial es del archivo Paint.fx del [ejemplo AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




