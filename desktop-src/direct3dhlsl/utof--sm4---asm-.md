---
title: utof (SM4-ASM)
description: Entero sin signo para conversión de punto flotante.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9283857df12a85819f0d191d13450e0311fdade
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077126"
---
# <a name="utof-sm4---asm"></a>utof (SM4-ASM)

Entero sin signo para conversión de punto flotante.



| utof dest \[ . Mask \] , src0 \[ . swizzle\] |
|--------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes que se van a convertir.<br/>                  |



 

## <a name="remarks"></a>Observaciones

*src0* debe contener un entero de una tupla de 4 bits 32 sin signo. Una vez ejecutada la instrucción, *dest* contendrá una tupla de 4 puntos flotantes. La conversión se realiza por componente.

Cuando un valor de entrada de tipo entero es demasiado grande para representarlo exactamente en el formato de punto flotante, se redondea al modo uniforme más cercano.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 





