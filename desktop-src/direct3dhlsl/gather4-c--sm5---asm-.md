---
title: gather4_c (sm5 - asm)
description: Igual que gather4, excepto que esta instrucción realiza una comparación en los elementos de textura, de forma similar a la del ejemplo \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b300e27743d08f3bbdf813de200b5a749a4ac25f16ab10458968731b9918c493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488695"
---
# <a name="gather4_c-sm5---asm"></a>gather4 \_ c (sm5 - asm)

Igual que [**gather4**](gather4--sm5---asm-.md), excepto que esta instrucción realiza una comparación en los elementos de textura, de forma similar a [**la del ejemplo \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ c \[ \_ aoffimmi(u,v) \] dest \[ .mask , \] srcAddress \[ .swzzle \] , srcResource \[ .swlinole \] , srcSampler \[ . R \] , srcReferenceValue |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descripción                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[en \] La dirección del resultado de la operación<br/>                                    |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[en \] Un conjunto de coordenadas de textura.<br/>                                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[en \] Un registro de textura.<br/>                                                           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[en \] Un registro de sampler.<br/>                                                           |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[en \] Un registro con un único componente seleccionado, que se usa en la comparación.<br/> |



 

## <a name="remarks"></a>Comentarios

Vea [**el \_ ejemplo c**](sample-c--sm4---asm-.md) para obtener una descripción de cómo se compara *srcReferenceValue* con cada texel obtenido. A **diferencia del ejemplo \_ c**, **gather4 \_ c** devuelve cada resultado de comparación, en lugar de filtrarlos.

En el caso de las esquinas de TextureCube, donde hay tres elementos texel reales y se debe sintetizar un cuarto, la síntesis debe producirse después del paso de comparación. Esto significa que el resultado de comparación devuelto para el texel sin formato puede ser 0, 0,33, 0,66 o 1. Algunas implementaciones solo pueden devolver 0 o 1 para el texel sintetizado. Aparte de esta lista de posibles resultados, no se especifica el método para sintetizar el texel.

En el caso de los formatos con componentes float32, si el valor que se captura se normaliza o +-INF, se usa en la operación de comparación sin tocar. NaN se usa en la operación de comparación como NaN, pero se puede cambiar la representación de bits exacta del NaN. Los desnormas se vacían a cero en la comparación. Para TextureCubes, se debe producir alguna síntesis del 4.º texel que falta en las esquinas, por lo que no se aplica la noción de devolver bits sin modificar para el texel sintetizado.

Los formatos admitidos *para gather4 \_ c* son los mismos que los admitidos para *el ejemplo \_ c*. Se trata de formatos de componente único, por lo que es . R en *srcSampler,* en lugar de un swzzle arbitrario. **gather4 \_ c** en un recurso sin enlazar devuelve 0.

Use esta instrucción para el filtrado de mapas de sombra personalizados.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





