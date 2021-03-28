---
title: sample_c_lz (SM4-ASM)
description: Realiza un filtro de comparación. Esta instrucción se comporta como ejemplo \_ c, excepto el valor de LOD es 0 y se omiten los derivados.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419923"
---
# <a name="sample_c_lz-sm4---asm"></a>ejemplo \_ \_ de c LZ (SM4-ASM)

Realiza un filtro de comparación. Esta instrucción se comporta como [ejemplo \_ c](sample-c--sm4---asm-.md), excepto el valor de LOD es 0 y se omiten los derivados.



| Sample \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource. r,//debe ser. r swizzle srcSampler, srcReferenceValue//Single Component seleccionado |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[en \] la dirección de los resultados de la operación.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[en \] un conjunto de coordenadas de textura. Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[en \] un registro de textura. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[en \] un registro de muestra. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[en \] un registro con un componente único seleccionado, que se usa en la comparación.<br/>                            |



 

## <a name="remarks"></a>Observaciones

"LZ" representa el nivel cero. Dado que se omiten los derivados, esta instrucción está disponible en los sombreadores distintos del sombreador de píxeles.

Si esta instrucción se usa con una textura de mipmapped, se muestra el valor de LOD 0, a menos que la muestra tenga una abrazadera LOD que coloque el LOD en alguna otra parte, o bien, si hay una diferencia de LOD, que simplemente afectaría a partir de 0. Dado que se omiten los derivados, el filtrado anisotrópico se comporta como filtro anisotrópico.

En los sombreadores de píxeles, esta instrucción se puede usar dentro del control de flujo variable cuando las coordenadas de textura se derivan en el sombreador, a diferencia del **ejemplo \_ c**.

La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.

Esta instrucción está disponible en todos los sombreadores, no solo en el sombreador de píxeles, por coherencia.



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

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

 

 





