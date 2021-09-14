---
title: lod (sm4.1 - asm)
description: Devuelve el nivel de detalle (LOD) que se usaría para el filtrado de textura.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974267"
---
# <a name="lod-sm41---asm"></a>lod (sm4.1 - asm)

Devuelve el nivel de detalle (LOD) que se usaría para el filtrado de textura.



| lod dest \[ .mask \] , srcAddress \[ .swlinole \] , srcResource \[ .sw swzzle \] , srcSampler |
|--------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección de los resultados.<br/>   |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] Un conjunto de coordenadas de textura.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] Un registro de textura.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] Un registro de sampler.<br/>           |



 

## <a name="remarks"></a>Observaciones

Esto se comporta como la [instrucción de](sample--sm4---asm-.md) ejemplo, pero no se genera una muestra filtrada. La instrucción calcula el siguiente vector (ClampedLOD, NonClampedLOD, 0, 0). NonClampedLOD es un valor LOD calculado que omite cualquier fijación del muestreador o de la textura (es decir, puede devolver valores negativos). ClampedLOD es un valor de LOD calculado que se usaría en la instrucción de **ejemplo** real. Swzzle en *srcResource permite* que los valores devueltos se desdoleguen arbitrariamente antes de que se escriban en el destino.

Si no hay ningún recurso enlazado a la ranura especificada, se devuelve 0.

Si el muestreador usa filtrado anisotropico, el LOD debe corresponder al nivel de mip fraccionamiento en función del eje más pequeño de la superficie elíptica.

Esto es válido para los siguientes tipos de textura: Texture1D, Texture2D, Texture3D y TextureCube.

La **instrucción lod** no se define cuando se usa con un muestreador que especifica el filtrado de mip de punto, en concreto, cualquier enumeración FILTER D3D10 que termine en \_ MIP \_ POINT. (Un ejemplo de esto sería D3D10 \_ FILTRAR \_ MIN \_ MAG \_ MIP \_ POINT).)

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
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





