---
title: LOD (SM 4.1-ASM)
description: Devuelve el nivel de detalle (LOD) que se utilizaría para el filtrado de textura.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784948"
---
# <a name="lod-sm41---asm"></a>LOD (SM 4.1-ASM)

Devuelve el nivel de detalle (LOD) que se utilizaría para el filtrado de textura.



| LOD dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler |
|--------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección de los resultados.<br/>   |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] un conjunto de coordenadas de textura.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] un registro de textura.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] un registro de muestra.<br/>           |



 

## <a name="remarks"></a>Observaciones

Esto se comporta como la instrucción de [ejemplo](sample--sm4---asm-.md) , pero no se genera un ejemplo filtrado. La instrucción calcula el vector siguiente (ClampedLOD, NonClampedLOD, 0,0). NonClampedLOD es un valor de LOD calculado que omite cualquier fijación de la muestra o la textura (es decir, puede devolver valores negativos). ClampedLOD es un valor de LOD calculado que utilizaría la instrucción de **ejemplo** real. Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino.

Si no hay ningún recurso enlazado a la ranura especificada, se devuelve 0.

Si el muestreador usa el filtrado anisotrópico, el LOD debe corresponder al nivel de MIP fraccionario basado en el eje más pequeño de la superficie elíptica.

Esto es válido para los tipos de textura siguientes: Texture1D, Texture2D, Texture3D y TextureCube.

La instrucción **LOD** no se define cuando se usa con un muestreador que especifica el filtrado del punto MIP, en concreto, cualquier \_ enumeración de filtro D3D10 que termine en el \_ punto MIP. (Un ejemplo sería D3D10 \_ FILTRAr el \_ \_ \_ punto de MIP mínimo \_

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
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





