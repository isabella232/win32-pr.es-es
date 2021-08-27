---
title: movc (sm4 - asm)
description: Movimiento condicional por componente. | movc (sm4 - asm)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81da36b39f60929bdfbac3b4a37c379189cf358ed4844e1a4cc899f867970065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095365"
---
# <a name="movc-sm4---asm"></a>movc (sm4 - asm)

Movimiento condicional por componente.



| movc \[ \_ sat \] dest \[ .mask \] , src0 \[ .swzzle, \] \[ - \] src1 \[ \_ abs \] \[ .swzzle, \] \[ - \] src2 \[ \_ abs \] \[ .swzzle \] , |
|----------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación. <br/> Si *src0*, *dest*  =  *src1* else *dest*  =  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes en los que se va a probar la condición.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Componentes que se moverá. <br/>                                                                                     |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] Componentes que se moverá.<br/>                                                                                      |



 

## <a name="remarks"></a>Comentarios

En el ejemplo siguiente se muestra cómo usar esta instrucción.

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

Los modificadores de *src1* y *src2,* que no son swzzle, suponen que los datos son de punto flotante. La ausencia de modificadores simplemente mueve los datos sin modificar los bits.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 





