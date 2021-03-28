---
title: sample_c (SM4-ASM)
description: Realiza un filtro de comparación.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996880"
---
# <a name="sample_c-sm4---asm"></a>ejemplo \_ c (SM4-ASM)

Realiza un filtro de comparación.



| el ejemplo \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource. r,//debe ser. r swizzle srcSampler, srcReferenceValue//Single Component seleccionado |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[en \] la dirección de los resultados de la operación.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[en \] un conjunto de coordenadas de textura. Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[en \] un registro de textura. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[en \] un registro de muestra. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[en \] un registro con un componente único seleccionado, que se usa en la comparación.<br/>                            |



 

## <a name="remarks"></a>Observaciones

El propósito principal de esta instrucción es proporcionar un bloque de creación para Percentage-Closer filtrado de profundidad. La "c" en el **ejemplo \_ c** significa comparación.

Los operandos del **ejemplo \_ c** son idénticos a la instrucción de [ejemplo](sample--sm4---asm-.md) , salvo que hay un operando de origen float32 adicional, *srcReferenceValue*, que debe ser un registro con un solo componente seleccionado o un literal escalar.

El parámetro *srcResource* debe tener un swizzle. r (rojo). el **ejemplo \_ c** funciona exclusivamente en el componente rojo y devuelve un valor único. El swizzle. r en *srcResource* indica que el resultado escalar se replica en todos los componentes.

Cuando se establece un búfer de profundidad como textura de entrada, el valor de profundidad se muestra en el componente rojo.

Si esta instrucción se usa con un recurso que no es Texture1D/2D/2DArray/Cube/CubeArray, genera resultados no definidos.

Cuando se ejecuta esta instrucción, el hardware de muestreo usa el ComparisonFunction de la muestra actual para comparar *srcReferenceValue* con el valor de componente rojo del recurso de origen en cada "TAP" de la ubicación (textura) que el filtro de textura configurado actualmente cubre, en función de las coordenadas proporcionadas en *srcAddress*.

La comparación se produce después de que *srcReferenceValue* se haya cuantificado con la precisión del formato de textura, exactamente de la misma manera que z se cuantifica a la precisión del búfer de profundidad antes de la comparación de profundidad en la prueba de visibilidad de fusión de salida. Esto incluye una abrazadera al intervalo de formato (por ejemplo, \[ 0.. 1 \] para un formato UNORM).

El componente rojo del textura de origen se compara con el *srcReferenceValue* cuantificado. En el caso de textura que se encuentran fuera del recurso, el valor del componente rojo se determina aplicando los modos de dirección (y BorderColorR si está en el modo de borde) de la muestra. La comparación admite todas las reglas de comparación de punto flotante de D3D11, en el caso de que el formato de textura sea de punto flotante.

Cada comparación que pasa devuelve 1,0 f como el valor de componente rojo para textura, y cada comparación que produce un error devuelve 0,0 f como el valor rojo de la textura. A continuación, el filtrado se produce exactamente como lo especifican los Estados de muestra, funcionando solo en el componente rojo y devolver un único resultado de filtro escalar al sombreador, replicado en todos los componentes de *dest* enmascarados.

El uso del **ejemplo \_ c** es ortogonal a todos los demás controles de filtrado de uso general. el **ejemplo \_ c** funciona sin problemas con los demás modos de filtro de uso general. el **ejemplo \_ c** cambia el comportamiento de los filtros de uso general, de modo que los valores que se van a filtrar se convierten en 1,0 f o 0.0 f debido a los resultados de la comparación.

La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.

Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





