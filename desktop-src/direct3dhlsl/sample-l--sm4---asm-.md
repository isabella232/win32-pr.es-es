---
title: sample_l (SM4-ASM)
description: Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada. | sample_l (SM4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362271"
---
# <a name="sample_l-sm4---asm"></a>ejemplo \_ l (SM4-ASM)

Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada.



| Sample \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcLOD. Select ( \_ componente) |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección de los resultados de la operación.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] un conjunto de coordenadas de textura. Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] un registro de textura. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] un registro de muestra. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                 |
| <span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*<br/>                     | \[en \] LOD.<br/>                                                                                                 |



 

## <a name="remarks"></a>Observaciones

Esta instrucción es idéntica a [Sample](sample--sm4---asm-.md), salvo que la aplicación proporciona directamente el LOD como un valor escalar, que no representa ningún anisotropía. Esta instrucción está disponible en todas las etapas del sombreador de progammable.

**ejemplos \_ l muestra** la textura mediante *srcLOD* para que sea el LOD. Si el valor de LOD es <= 0, se elige zero'th (el mapa más grande), con el filtro de ampliación aplicado (si procede según el modo de filtro). Dado que *srcLOD* es un valor de punto flotante, el valor fraccionario se usa para interpolar entre dos niveles de MIP, si el filtro minimizar es lineal o con filtrado anisotrópico.

el **ejemplo \_ l** omite las derivadas de la dirección, por lo que el comportamiento del filtrado es puramente anisotrópico. Dado que se omiten los derivados, el filtrado anisotrópico se comporta como filtro anisotrópico.

Se respetan los Estados de muestra MIPLODBIAS y MAX/MINMIPLEVEL.

Cuando se usa en el sombreador de píxeles, **Sample \_ l** implica que la elección de LOD es por píxel, sin ningún efecto de los píxeles adyacentes, por ejemplo en la misma marca de 2x2.

La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.

Esta instrucción se aplica a las siguientes fases del sombreador:



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

 

 





