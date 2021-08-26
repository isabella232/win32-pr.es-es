---
title: sample_c (sm4 - asm)
description: Realiza un filtro de comparación.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2656f70a95487ce98aadc30a028fccaed00cb1c8d6324d64bb22c9672543d5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067735"
---
# <a name="sample_c-sm4---asm"></a>ejemplo \_ c (sm4 - asm)

Realiza un filtro de comparación.



| sample \_ c \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swprendle \] , srcResource.r, // debe ser .r swlinole srcSampler, srcReferenceValue // un solo componente seleccionado |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[en \] La dirección de los resultados de la operación.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[en \] Un conjunto de coordenadas de textura. Para más información, consulte la [instrucción de](sample--sm4---asm-.md) ejemplo.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[en \] Un registro de textura. Para más información, consulte la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[en \] Un registro de sampler. Para más información, consulte la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[en \] Un registro con un único componente seleccionado, que se usa en la comparación.<br/>                            |



 

## <a name="remarks"></a>Comentarios

El propósito principal de esta instrucción es proporcionar un bloque de creación para el filtrado Percentage-Closer profundidad. La "c" del **ejemplo \_ c** significa Comparación.

Los operandos para muestrear **\_ c** son idénticos a la instrucción de ejemplo, salvo que hay un operando de origen float32 adicional, [](sample--sm4---asm-.md) *srcReferenceValue*, que debe ser un registro con un solo componente seleccionado o un literal escalar.

El *parámetro srcResource* debe tener un swzzle .r (rojo). **El \_ ejemplo c** funciona exclusivamente en el componente rojo y devuelve un valor único. El archivo .r swzzle en *srcResource* indica que el resultado escalar se replica en todos los componentes.

Cuando un búfer de profundidad se establece como una textura de entrada, el valor de profundidad se muestra en el componente rojo.

Si esta instrucción se usa con un recurso que no es Texture1D/2D/2DArray/Cube/CubeArray, genera resultados no definidos.

Cuando se ejecuta esta instrucción, el hardware de muestreo usa comparisonFunction del sampler actual para comparar *srcReferenceValue* con el valor del componente Rojo del recurso de origen en cada ubicación de "pulsar" (texel) de filtro que cubre el filtro de textura configurado actualmente, en función de las coordenadas proporcionadas en *srcAddress*.

La comparación se produce después de que *srcReferenceValue* se haya cuantificado en la precisión del formato de textura, exactamente de la misma manera que z se cuantifica en precisión del búfer de profundidad antes de Comparación de profundidad en la prueba de visibilidad de la fusión de salida. Esto incluye una fijación al intervalo de formato (por \[ ejemplo, 0..1 \] para un formato UNORM).

El componente Red del texel de origen se compara con el *valor srcReferenceValue cuantificado.* En el caso de los elementos de textura que están fuera del recurso, el valor del componente Rojo se determina aplicando los modos de dirección (y BorderColorR si se encuentra en modo de borde) desde sampler. La comparación respeta todas las reglas de comparación de punto flotante D3D11, en caso de que el formato de textura sea de punto flotante.

Cada comparación que pasa devuelve 1,0f como valor del componente Rojo para el elemento texel y cada comparación que produce un error devuelve 0,0f como valor rojo para la textura. A continuación, el filtrado se produce exactamente como se especifica en los estados sampler, funcionando solo en el componente Rojo y devolviendo un único resultado de filtro escalar al sombreador, replicado en todos los componentes *de dest* enmascarados.

El uso de **c de \_ ejemplo** es ortogonal para todos los demás controles de filtrado de uso general. **C \_ de ejemplo** funciona sin problemas con los otros modos de filtro de uso general. **El \_ ejemplo c** cambia el comportamiento de los filtros de uso general de forma que los valores que se filtran se convierten en 1.0f o 0.0f debido a los resultados de la comparación.

Al capturar desde una ranura de entrada que no tiene nada enlazado, se devuelve 0 para todos los componentes.

Para obtener más información, vea la [instrucción de](sample--sm4---asm-.md) ejemplo.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





