---
title: sample_b (sm4 - asm)
description: Muestrea datos del elemento o textura especificados mediante la dirección especificada y el modo de filtrado identificado por el muestreador especificado. | sample_b (sm4 - asm)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240819"
---
# <a name="sample_b-sm4---asm"></a>ejemplo \_ b (sm4 - asm)

Muestrea datos del elemento o textura especificados mediante la dirección especificada y el modo de filtrado identificado por el muestreador especificado.



| sample \_ b \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swprendle \] , srcResource \[ .sw sw swlinole, \] srcSampler, srcLODBias.select \_ component |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección del resultado de la operación.<br/>                                                              |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] Un conjunto de coordenadas de textura. Para más información, consulte la [instrucción de](sample--sm4---asm-.md) ejemplo.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] Un registro de textura. Para más información, consulte la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] Un registro de sampler. Para más información, consulte la **instrucción de** ejemplo.<br/>                                 |
| <span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*<br/>     | \[en \] Vea la sección **Comentarios** para obtener información sobre este parámetro.<br/>                                        |



 

## <a name="remarks"></a>Observaciones

Los datos de origen pueden provienen de cualquier tipo de recurso, que no sea Búferes. Se aplica un sesgo adicional al nivel de detalle calculado como parte de la ejecución de la instrucción.

Esta instrucción se [](sample--sm4---asm-.md) comporta como la instrucción de ejemplo con la adición de aplicar el valor *srcLODBias* especificado al nivel de valor de detalle calculado como parte de la ejecución de la instrucción antes de seleccionar los mapas mip. El valor *srcLODBias* se agrega al LOD calculado por píxel, junto con el valor mipLODBias del muestreador, antes de la fijación a MinLOD y MaxLOD.

### <a name="restrictions"></a>Restricciones

-   **el \_ ejemplo b** hereda las mismas restricciones que la instrucción [de](sample--sm4---asm-.md) ejemplo, además de restricciones adicionales para su parámetro adicional.
-   El intervalo *de srcLODBias* es (-16.0f a 15.99f); Los valores fuera de este intervalo producirán resultados no definidos.
-   *srcLODBias debe* usar un único selector de componentes si no es un valor escalar inmediato.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





