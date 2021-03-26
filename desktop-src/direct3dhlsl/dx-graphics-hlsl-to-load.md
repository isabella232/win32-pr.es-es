---
title: Load (objeto de textura de HLSL de DirectX)
description: Lee los datos de textura sin ningún filtrado ni muestreo.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/05/2021
ms.locfileid: "104151935"
---
# <a name="load-directx-hlsl-texture-object"></a>Load (objeto de textura de HLSL de DirectX)

Lee los datos de textura sin ningún filtrado ni muestreo.



<table>
<tbody>
<tr class="odd">
<td>RET Object. Load (<dl> Ubicación typeX,<br />
[typeX SampleIndex, ]<br />
[desplazamiento de typeX]<br />
</dl>);</td>
</tr>
</tbody>
</table>

typeX denota que hay cuatro tipos posibles: **int**, **INT2**, **INT3** o **INT4**.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*
</dt> <dd>

Un tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) (excepto TextureCube o TextureCubeArray).

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Cód*
</dt> <dd>

\[en \] las coordenadas de textura; el último componente especifica el nivel de mipmap. Este método usa un sistema de coordenadas basado en 0 y no un sistema UV 0,0-1,0. El tipo de argumento depende del tipo de objeto de textura.



| Tipo de objeto                                  | Tipo de parámetro |
|----------------------------------------------|----------------|
| Buffer                                       | int            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray, Texture 2D, Texture2DMSArray | int3           |
| Texture2DArray, Texture3D                    | int4           |



 

Por ejemplo, para tener acceso a una textura 2D, proporcione coordenadas UV para los dos primeros componentes y un nivel de mipmap para el tercer componente.

> [!Note]  
> Cuando una o varias de las coordenadas de la *Ubicación* superan las dimensiones del nivel de mipmap u, v o w de la textura, **Load** devuelve cero en todos los componentes. Direct3D garantiza que se devuelva cero para cualquier recurso al que se tenga acceso fuera de los límites.

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*
</dt> <dd>

\[en \] un índice de muestreo opcional.



| Tipo de textura                                                                                                   | Tipo de parámetro |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray | no admitido  |
| Texture2DMS, Texture2DMSArray ¹                                                                                 | int            |



 

> [!Note]  
> *SampleIndex* solo está disponible para las texturas de varios ejemplos.

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Posición*
</dt> <dd>

\[en \] un desplazamiento opcional aplicado a las coordenadas de textura antes del muestreo. El tipo de desplazamiento depende del tipo de objeto de textura y debe ser estático.



| Tipo de textura                                             | Tipo de parámetro |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | int            |
| Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | int3           |



 

> [!Note]  
> Si usa *offset* con texturas de varios ejemplos, también debe especificar *SampleIndex*.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El tipo de valor devuelto coincide con el tipo en la declaración del *objeto* . Por ejemplo, un objeto Texture2D que se declaró como "Texture2d <uint4> de la cartexture;" tiene un valor devuelto de tipo **uint4**.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ¹ | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ¹ | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ¹ |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.

## <a name="example"></a>Ejemplo

Este ejemplo de código parcial procede del archivo Paint. FX en el [ejemplo AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).


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

[Texture-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




