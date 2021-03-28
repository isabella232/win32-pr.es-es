---
title: gather4_po_c (SM5-ASM)
description: Se comporta igual que gather4 \_ Po, excepto que realiza una comparación en textura, de forma similar al ejemplo \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419964"
---
# <a name="gather4_po_c-sm5---asm"></a>\_po gather4 \_ c (SM5-ASM)

Se comporta igual que [**gather4 \_ po**](gather4-po--sm5---asm-.md), excepto que realiza una comparación en textura, de forma similar al [**ejemplo \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ po \_ c dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcOffset \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . R \] , srcReferenceValue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descripción                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[en \] la dirección del resultado de la operación.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[en \] un conjunto de coordenadas de textura.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>                                 | \[en \] el desplazamiento.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[en \] un registro de textura.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[en \] un registro de muestra.<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[en \] componente único seleccionado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Vea el [**ejemplo \_ c**](sample-c--sm4---asm-.md) para obtener información sobre cómo se compara *srcReferenceValue* con cada textura capturado. A diferencia del **ejemplo \_ c**, *gather4 \_ po \_ c* devuelve cada resultado de comparación, en lugar de filtrarlos.

Esta instrucción, como **gather4 \_ po**, solo funciona con texturas 2D. Esto no es lo mismo que [**gather4 \_ c**](gather4-c--sm5---asm-.md), que también funciona con TextureCubes.

En el caso de los formatos con componentes float32, si el valor que se va a capturar es normalizado o +-INF, se usa en la operación de comparación sin tocar. NaN se usa en la operación de comparación como NaN, pero se puede cambiar la representación de bits exacta del NaN. Las desnormaciones se vacían en cero entrando en la comparación. En el caso de TextureCubes, algunas síntesis de la cuarta textura que faltan deben aparecer en las esquinas, por lo que no se aplica la noción de devolver bits sin modificar para la textura sintetizada.

Los formatos admitidos para **\_ po gather4 \_ c** son los mismos que los que se admiten para el **ejemplo \_ c**. Son formatos de un solo componente, por lo tanto,. R en srcSampler, en lugar de un swizzle arbitrario.

**gather4 \_ po \_ c** en un recurso sin enlazar devuelve 0.

Use este método para el filtrado de mapas de instantáneas.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





