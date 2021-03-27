---
title: Mad (SM4-ASM)
description: Agregar multiplicación por componentes.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d34823cdb3545f29426117b35903c97c08c5807
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077081"
---
# <a name="mad-sm4---asm"></a>Mad (SM4-ASM)

Multiplicar por componentes & agregar.



| : Mad \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] el resultado de la operación.<br/> *dest*  =  *src0* \* *SRC1*  +  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] multiplicando.<br/>                                                          |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] el multiplicador.<br/>                                                            |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] addend.<br/>                                                                |



 

## <a name="remarks"></a>Observaciones

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

 

 





