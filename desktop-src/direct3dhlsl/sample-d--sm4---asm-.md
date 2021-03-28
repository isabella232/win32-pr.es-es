---
title: sample_d (SM4-ASM)
description: Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada. | sample_d (SM4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998185"
---
# <a name="sample_d-sm4---asm"></a>ejemplo \_ d (SM4-ASM)

Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada.



| SSample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcXDerivatives \[ . swizzle \] , srcYDerivatives \[ . swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                               | Descripción                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                    | \[en \] la dirección de los resultados de la operación.<br/>                                                                  |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                     | \[en \] un conjunto de coordenadas de textura. Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .<br/>      |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                 | \[en \] un registro de textura. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                      |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                     | \[en \] un registro de muestra. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                      |
| <span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*<br/> | \[en \] los derivados de la dirección de origen en la dirección x. Para más información, vea la sección **Comentarios**.<br/> |
| <span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*<br/> | \[en \] los derivados de la dirección de origen en la dirección y. Para más información, vea la sección **Comentarios**.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción se comporta como la instrucción de [ejemplo](sample--sm4---asm-.md) , con la excepción de que los derivados de la dirección de origen en la dirección x y la dirección y se proporcionan mediante parámetros adicionales, *srcXDerivatives* y *srcYDerivatives*, respectivamente. Estos derivados se encuentran en un espacio normalizado de coordenadas de textura.

Los componentes r, g y b de *srcXDerivatives* (pos-swizzle) proporcionan du/DX, DV/DX y DW/DX. Se omite el componente ' a ' (POS-swizzle).

Los componentes r, g y b de *srcYDerivatives* (pos-swizzle) proporcionan du/DY, DV/DY y DW/DY. Se omite el componente ' a ' (POS-swizzle).

A diferencia de la instrucción de **ejemplo** , que puede compartir un único cálculo de LOD en una marca de 2x2, el **ejemplo \_ d** debe calcular el LOD completamente de forma independiente y por píxel cuando se usa en el sombreador de píxeles.

Si las entradas derivadas del **ejemplo \_ d** proceden de instrucciones de cálculo derivadas en el sombreador de píxeles y los valores incluyen INF/Nan, el comportamiento del **ejemplo \_ d** podría no coincidir con la instrucción de **ejemplo** , que calcula implícitamente el derivado. Los valores INF/NaN pueden afectar al cálculo de LOD de manera diferente.

La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.

### <a name="restrictions"></a>Restricciones

-   el **ejemplo \_ d** hereda las mismas restricciones que la instrucción de **ejemplo** , además de una restricción adicional a continuación para sus parámetros adicionales.
-   *srcXDerivatives* y *srcYDerivatives* deben ser Temp (r \# /x \# ), constantBuffer (CB \# ), registros de entrada (v \# ) o valores inmediatos.

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

 

 





