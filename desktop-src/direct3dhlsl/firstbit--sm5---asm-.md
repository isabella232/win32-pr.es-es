---
title: firstbit (sm5 - asm)
description: Busca el primer conjunto de bits en un número, ya sea desde LSB o MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ea47c8e0674db5dc0349e5d6a8a041fa7d3623e6578eee542edeb1749577d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511949"
---
# <a name="firstbit-sm5---asm"></a>firstbit (sm5 - asm)

Busca el primer conjunto de bits en un número, ya sea desde LSB o MSB.



| firstbit{ \_ hi\|\_lo\|\_shi} dest \[ .mask \] , src0 \[ .swzzle\] |
|-------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en La posición entera del primer conjunto de bits en src0 a partir del LSB para el primer bit lo o \]  \_ MSB para firstbit \_ hi.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El entero de entrada.<br/>                                                                                                  |



 

## <a name="remarks"></a>Comentarios

Esta operación devuelve la posición entera del primer conjunto de bits en la entrada de 32 bits a partir del LSB para el primer bit lo o \_ MSB para el primer bit \_ hi. Por ejemplo, firstbit \_ lo en 0x00000001 devuelve 0. firstbit \_ hi on 0x10000000 devuelve 3.

firstbit shi (s para signed) devuelve el primer 0 del MSB si el número es negativo; de lo contrario, devuelve el primer 1 del \_ MSB.

Todas las variantes de la instrucción devuelven ~0 (0xffffffff en el registro de 32 bits) si no se encuentra ninguna coincidencia.

Use esta instrucción para enumerar rápidamente los bits establecidos en un campo de bits o buscar la potencia más grande de 2 en un número.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="mimimum-shader-model"></a>Modelo de sombreador de Mimimum

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





