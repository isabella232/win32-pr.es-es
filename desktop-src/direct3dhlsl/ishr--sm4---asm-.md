---
title: ISHR (SM4-ASM)
description: Desplazamiento aritmético a la derecha (signo de extensión). | ISHR (SM4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998245"
---
# <a name="ishr-sm4---asm"></a>ISHR (SM4-ASM)

Desplazamiento aritmético a la derecha (signo de extensión).



| ISHR dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1. Select ( \_ componente) |
|--------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] contiene el resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] contiene el valor que se va a desplazar.<br/>     |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] contiene la cantidad de desplazamiento.<br/>            |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza un cambio aritmético en forma de componente de cada valor de 32 bits de *src0* a la derecha por un recuento de bits sin signo proporcionado por el LSB 5 bits (intervalo 0-31) del *\_ componente SRC1. Select*, replicando el valor de bit 31. El resultado de 32 bits por componente se coloca en el *destino*. El recuento es un valor escalar que se aplica a todos los componentes.

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

 

 





