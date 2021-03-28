---
title: ftou (SM4-ASM)
description: Conversión de punto flotante a entero sin signo.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358475"
---
# <a name="ftou-sm4---asm"></a>ftou (SM4-ASM)

Conversión de punto flotante a entero sin signo.



| ftou dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|----------------------------------------------------|



 



| ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|----------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el valor que se va a convertir.<br/>                        |



 

## <a name="remarks"></a>Observaciones

La conversión se realiza por componente. El redondeo siempre se realiza hacia cero, siguiendo la Convención de C para las conversiones de Float a int.

Las aplicaciones que requieren una semántica de redondeo diferente pueden invocar las instrucciones **Round** antes de la conversión a un entero.

Las entradas se fijan en el intervalo \[ 0.0 f... 4294967295.999 f \] antes de la conversión y los valores Nan de entrada producen un resultado cero.

Los modificadores de valor absoluto y de negación opcionales se aplican a los valores de origen antes de la conversión.

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

 

 





