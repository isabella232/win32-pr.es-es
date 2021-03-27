---
title: sample_b (SM4-ASM)
description: Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada. | sample_b (SM4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280129"
---
# <a name="sample_b-sm4---asm"></a>ejemplo \_ b (SM4-ASM)

Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada.



| ejemplo \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcLODBias. Select ( \_ componente) |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección del resultado de la operación.<br/>                                                              |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] un conjunto de coordenadas de textura. Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] un registro de textura. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] un registro de muestra. Para obtener más información, vea la instrucción de **ejemplo** .<br/>                                 |
| <span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*<br/>     | \[en, \] vea la sección **comentarios** para obtener información sobre este parámetro.<br/>                                        |



 

## <a name="remarks"></a>Observaciones

Los datos de origen pueden provienen de cualquier tipo de recurso, que no sea de búferes. Se aplica una desviación adicional al nivel de detalle calculado como parte de la ejecución de la instrucción.

Esta instrucción se comporta como la instrucción de [ejemplo](sample--sm4---asm-.md) con la adición de la aplicación del valor de *srcLODBias* especificado al nivel de valor detallado calculado como parte de la ejecución de la instrucción antes de seleccionar los mapas MIP. El valor *srcLODBias* se agrega al LOD calculado en cada píxel, junto con el valor MipLODBias de muestra, antes de la abrazadera a MinLOD y MaxLOD.

### <a name="restrictions"></a>Restricciones

-   el **ejemplo \_ b** hereda las mismas restricciones que la instrucción de [ejemplo](sample--sm4---asm-.md) , además de restricciones adicionales para su parámetro adicional.
-   El intervalo de *srcLODBias* es (-16,0 f a 15.99 f); los valores fuera de este intervalo producirán resultados no definidos.
-   *srcLODBias* debe usar un selector de componente único si no es un escalar inmediato.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





