---
title: gather4_po_c (sm5 - asm)
description: Se comporta igual que gather4 po, salvo que realiza la comparación \_ en los elementos de textura, de forma similar a la del ejemplo \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361567"
---
# <a name="gather4_po_c-sm5---asm"></a>gather4 \_ po \_ c (sm5 - asm)

Se comporta igual que [**gather4 \_ po**](gather4-po--sm5---asm-.md), excepto que realiza la comparación en los elementos de textura, de forma similar a [**la muestra \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ po \_ c dest \[ .mask , \] srcAddress \[ .swzzle \] , srcOffset \[ .swcela, \] srcResource \[ .swlinole \] , srcSampler \[ . R \] , srcReferenceValue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descripción                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[en \] Un conjunto de coordenadas de textura.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>                                 | \[en \] Desplazamiento.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[en \] Un registro de textura.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[en \] Un registro de sampler.<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[en \] Componente único seleccionado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Vea [**el \_ ejemplo c**](sample-c--sm4---asm-.md) para obtener información sobre cómo se compara *srcReferenceValue* con cada texel capturado. A **diferencia del ejemplo \_ c**, *gather4 po \_ \_ c* devuelve cada resultado de comparación, en lugar de filtrarlos.

Esta instrucción, como **gather4 \_ po,** solo funciona con texturas 2D. Esto es diferente de [**gather4 \_ c**](gather4-c--sm5---asm-.md), que también funciona con TextureCubes.

En el caso de los formatos con componentes float32, si el valor que se captura se normaliza o +-INF, se usa en la operación de comparación sin tocar. NaN se usa en la operación de comparación como NaN, pero se puede cambiar la representación de bits exacta del NaN. Los desnormas se vacían a cero en la comparación. Para TextureCubes, se debe producir alguna síntesis del 4.º texel que falta en las esquinas, por lo que no se aplica la noción de devolver bits sin modificar para el texel sintetizado.

Los formatos admitidos **para gather4 \_ po \_ c** son los mismos que los admitidos para **el ejemplo \_ c**. Se trata de formatos de componente único, por lo que es . R en srcSampler, en lugar de un swzzle arbitrario.

**gather4 \_ po \_ c** en un recurso sin enlazar devuelve 0.

Use este método para el filtrado del mapa de sombras.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





