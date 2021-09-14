---
title: sample_c_lz (sm4 - asm)
description: Realiza un filtro de comparación. Esta instrucción se comporta como el ejemplo \_ c, excepto que LOD es 0 y se omiten los derivados.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358854"
---
# <a name="sample_c_lz-sm4---asm"></a>ejemplo \_ de c \_ lz (sm4 - asm)

Realiza un filtro de comparación. Esta instrucción se comporta como [c de \_ ejemplo,](sample-c--sm4---asm-.md)excepto que LOD es 0 y se omiten los derivados.



| sample \_ c \_ lz \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swzzle \] , srcResource.r, // must be .r swlinole srcSampler, srcReferenceValue // single component selected |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[en \] La dirección de los resultados de la operación.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[en \] Un conjunto de coordenadas de textura. Para obtener más información, vea la [instrucción de](sample--sm4---asm-.md) ejemplo.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[en \] Un registro de textura. Para obtener más información, vea la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[en \] Un registro de sampler. Para obtener más información, vea la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[en \] Un registro con un único componente seleccionado, que se usa en la comparación.<br/>                            |



 

## <a name="remarks"></a>Observaciones

"lz" significa level-zero. Dado que se omiten los derivados, esta instrucción está disponible en sombreadores que no sean el sombreador de píxeles.

Si esta instrucción se usa con una textura mipmapped, se muestrea LOD 0, a menos que el muestreador tenga una fijación lod que coloca el LOD en otro lugar, o si hay un sesgo de LOD, que simplemente sesgo a partir de 0. Dado que se omiten los derivados, el filtrado anisotropico se comporta como filtrado isotropico.

En sombreadores de píxeles, esta instrucción se puede usar dentro de un control de flujo variable cuando las coordenadas de textura se derivan en el sombreador, a diferencia del **ejemplo \_ c**.

Al capturar desde una ranura de entrada que no tiene nada enlazado, se devuelve 0 para todos los componentes.

Esta instrucción está disponible en todos los sombreadores, no solo en el sombreador de píxeles, por coherencia.



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

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

 

 





