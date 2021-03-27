---
title: firstbit (SM5-ASM)
description: Busca el primer bit establecido en un número, ya sea de LSB o MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358509"
---
# <a name="firstbit-sm5---asm"></a>firstbit (SM5-ASM)

Busca el primer bit establecido en un número, ya sea de LSB o MSB.



| firstbit { \_ HI \|\_lo|\_Shi} dest \[ . Mask \] , src0 \[ . swizzle\] |
|-------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la posición entera del primer bit establecido en *src0* a partir de LSB para FIRSTBIT lo \_ o MSB para firstbit \_ HI.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el entero de entrada.<br/>                                                                                                  |



 

## <a name="remarks"></a>Observaciones

Esta operación devuelve la posición entera del primer bit establecido en la entrada de 32 bits a partir de LSB para firstbit lo \_ o MSB para firstbit \_ HI. Por ejemplo, firstbit \_ en 0x00000001 devuelve 0. firstbit \_ HI on 0x10000000 devuelve 3.

firstbit \_ Shi (s para signed) devuelve el primer 0 del MSB si el número es negativo; de lo contrario, devuelve el primer 1 del MSB.

Todas las variantes de la instrucción devuelven ~ 0 (0xFFFFFFFF en el registro de 32 bits) si no se encuentra ninguna coincidencia.

Use esta instrucción para enumerar rápidamente los bits establecidos en un campo de bits o buscar la potencia más grande de 2 en un número.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="mimimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





