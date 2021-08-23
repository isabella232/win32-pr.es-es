---
title: sample_l (sm4 - asm)
description: Muestrea los datos del elemento o textura especificados mediante la dirección especificada y el modo de filtrado identificado por el muestreador especificado. | sample_l (sm4 - asm)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbd65be095476cdac16ee95009994041af0b1812101b1d0d0b9a33a315ed58d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671815"
---
# <a name="sample_l-sm4---asm"></a>sample \_ l (sm4 - asm)

Muestrea los datos del elemento o textura especificados mediante la dirección especificada y el modo de filtrado identificado por el muestreador especificado.



| sample \_ l \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swzzle, \] srcResource \[ .swzzle, \] srcSampler, srcLOD.select \_ component |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección de los resultados de la operación.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] Un conjunto de coordenadas de textura. Para obtener más información, vea la [instrucción de](sample--sm4---asm-.md) ejemplo.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] Un registro de textura. Para obtener más información, vea la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] Un registro de sampler. Para obtener más información, vea la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*<br/>                     | \[en \] el LOD.<br/>                                                                                                 |



 

## <a name="remarks"></a>Comentarios

Esta instrucción es idéntica a [la del](sample--sm4---asm-.md)ejemplo , salvo que la aplicación proporciona el LOD directamente como un valor escalar, que no representa ninguna anisotropía. Esta instrucción está disponible en todas las fases de sombreador progammable.

**ejemplo \_ l** muestra la textura *mediante srcLOD* para que sea el LOD. Si el valor de LOD es <= 0, se elige el cero (mapa más grande), con el filtro de lupa aplicado (si procede en función del modo de filtro). Dado *que srcLOD* es un valor de punto flotante, el valor fraccionrio se usa para interpolar entre dos niveles de mip, si el filtro de minify es LINEAR o con filtrado anisotropo.

**en \_ el ejemplo l** se omiten los derivados de la dirección, por lo que el comportamiento de filtrado es puramente isotropo. Dado que se omiten los derivados, el filtrado anisotropico se comporta como filtrado isotropico.

Se respetan los estados de muestreo MIPLODBIAS y MAX/MINMIPLEVEL.

Cuando se usa en el sombreador de píxeles, el ejemplo **\_ l** implica que la elección del LOD es por píxel, sin ningún efecto en píxeles vecinos, por ejemplo, en la misma marca 2x2.

Al capturar desde una ranura de entrada que no tiene nada enlazado, se devuelve 0 para todos los componentes.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





