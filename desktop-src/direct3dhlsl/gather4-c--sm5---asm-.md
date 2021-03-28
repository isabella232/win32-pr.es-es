---
title: gather4_c (SM5-ASM)
description: Igual que gather4, salvo que esta inestación realiza una comparación en textura, similar al ejemplo \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996936"
---
# <a name="gather4_c-sm5---asm"></a>gather4 \_ c (SM5-ASM)

Igual que [**gather4**](gather4--sm5---asm-.md), salvo que esta inestación realiza una comparación en textura, similar al [**ejemplo \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ c \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . R \] , srcReferenceValue |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descripción                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[en \] la dirección del resultado de la operación<br/>                                    |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[en \] un conjunto de coordenadas de textura.<br/>                                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[en \] un registro de textura.<br/>                                                           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[en \] un registro de muestra.<br/>                                                           |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[en \] un registro con un componente único seleccionado, que se usa en la comparación.<br/> |



 

## <a name="remarks"></a>Observaciones

Vea el [**ejemplo \_ c**](sample-c--sm4---asm-.md) para obtener una descripción de cómo se compara *srcReferenceValue* con cada textura capturado. A diferencia del **ejemplo \_ c**, **gather4 \_ c** devuelve cada resultado de comparación, en lugar de filtrarlos.

En el caso de las esquinas TextureCube, donde hay tres textura reales y un cuarto se deben sintetizar, la síntesis debe aparecer después del paso de comparación. Esto significa que el resultado de la comparación devuelto para syntesized textura puede ser 0, 0,33, 0,66 o 1. Algunas implementaciones solo pueden devolver 0 o 1 para el textura sintetizado. Además de esta lista de resultados posibles, no se especifica el método para sintetizar el textura.

En el caso de los formatos con componentes float32, si el valor que se va a capturar es normalizado o +-INF, se usa en la operación de comparación sin tocar. NaN se usa en la operación de comparación como NaN, pero se puede cambiar la representación de bits exacta del NaN. Las desnormaciones se vacían en cero entrando en la comparación. En el caso de TextureCubes, algunas síntesis de la cuarta textura que faltan deben aparecer en las esquinas, por lo que no se aplica la noción de devolver bits sin modificar para la textura sintetizada.

Los formatos admitidos para *gather4 \_ c* son los mismos que los que se admiten para el *ejemplo \_ c*. Son formatos de un solo componente, por lo tanto,. R en *srcSampler*, en lugar de un swizzle arbitrario. **gather4 \_ c** en un recurso sin enlazar devuelve 0.

Use esta instrucción para el filtrado de mapa de instantáneas personalizado.

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

 

 





