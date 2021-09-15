---
title: sample_c (sm4 - asm)
description: Realiza un filtro de comparación.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465651"
---
# <a name="sample_c-sm4---asm"></a>ejemplo \_ c (sm4 - asm)

Realiza un filtro de comparación.



| sample \_ c \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swzzle \] , srcResource.r, // must be .r swlinole srcSampler, srcReferenceValue // single component selected |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[en \] La dirección de los resultados de la operación.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[en \] Un conjunto de coordenadas de textura. Para obtener más información, vea la [instrucción de](sample--sm4---asm-.md) ejemplo.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[en \] Un registro de textura. Para obtener más información, vea la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[en \] Un registro de sampler. Para obtener más información, vea la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[en \] Un registro con un único componente seleccionado, que se usa en la comparación.<br/>                            |



 

## <a name="remarks"></a>Observaciones

El propósito principal de esta instrucción es proporcionar un bloque de creación para el filtrado Percentage-Closer profundidad. La "c" del **ejemplo \_ c significa** Comparación.

Los operandos de la muestra [](sample--sm4---asm-.md) **\_ c** son idénticos a la instrucción de ejemplo, salvo que hay un operando de origen float32 adicional, *srcReferenceValue*, que debe ser un registro con un solo componente seleccionado o un literal escalar.

El *parámetro srcResource* debe tener un swzzle .r (rojo). **El \_ ejemplo c** funciona exclusivamente en el componente rojo y devuelve un valor único. El swzzle de .r en *srcResource* indica que el resultado escalar se replica en todos los componentes.

Cuando un búfer de profundidad se establece como una textura de entrada, el valor de profundidad se muestra en el componente rojo.

Si esta instrucción se usa con un recurso que no es texture1D/2D/2DArray/Cube/CubeArray, genera resultados indefinidos.

Cuando se ejecuta esta instrucción, el hardware de muestreo usa el elemento ComparisonFunction del sampler actual para comparar *srcReferenceValue* con el valor del componente Rojo del recurso de origen en cada ubicación de "pulsar" (texel) de filtro que cubre el filtro de textura configurado actualmente, en función de las coordenadas proporcionadas *en srcAddress*.

La comparación se produce después de *que srcReferenceValue* se haya cuantificado en la precisión del formato de textura, exactamente de la misma manera que z se cuantifica en precisión de búfer de profundidad antes de Comparación de profundidad en la prueba de visibilidad de fusión de salida. Esto incluye una fijación al intervalo de formato (por \[ ejemplo, 0..1 \] para un formato UNORM).

El componente rojo del elemento de textura de origen se compara con el *valor de srcReferenceValue cuantificado.* En el caso de los elementos de textura que están fuera del recurso, el valor del componente Rojo se determina aplicando los modos de dirección (y BorderColorR si está en modo de borde) del sampler. La comparación respeta todas las reglas de comparación de punto flotante D3D11, en caso de que el formato de textura sea de punto flotante.

Cada comparación que pasa devuelve 1,0f como valor del componente Rojo para el elemento de textura y cada comparación que produce un error devuelve 0,0f como valor rojo para la textura. A continuación, el filtrado se produce exactamente como se especifica en los estados sampler, funciona solo en el componente Red y devuelve un único resultado de filtro escalar al sombreador, replicado en todos los componentes *dest* enmascarados.

El uso de **c de \_ ejemplo es** ortogonal para todos los demás controles de filtrado de uso general. **C \_ de ejemplo** funciona sin problemas con los demás modos de filtro de uso general. **El \_ ejemplo c** cambia el comportamiento de los filtros de uso general para que los valores que se filtran se conviertan en 1.0f o 0.0f debido a los resultados de la comparación.

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
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





