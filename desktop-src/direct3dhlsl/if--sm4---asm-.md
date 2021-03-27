---
title: if (SM4-ASM)
description: Bifurcación basada en la lógica o en el resultado.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996849"
---
# <a name="if-sm4---asm"></a>if (SM4-ASM)

Bifurcación basada en la lógica o en el resultado.



| Si { \_ z \|\_NZ} src0. Select ( \_ componente) |
|--------------------------------------|



 



| Elemento                                                            | Descripción                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] contiene el componente en el que se va a probar la condición.<br/> |



 

## <a name="remarks"></a>Observaciones

El formato de token contiene el desplazamiento de la instrucción de endif correspondiente en el sombreador como una comodidad.

En el ejemplo siguiente se muestra cómo utilizar esta instrucción.

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a>Restricciones

-   Los operandos de origen (si 4 vectores de componente) deben utilizar un selector de componente único.
-   El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits. Si un bit es distinto de cero, **si \_ z** será true. Si todos los bits son cero, **si \_ NZ** será true.
-   Los bloques de control de flujo pueden anidar hasta 64 de profundidad por subrutina (y Main). El compilador de HLSL no generará subrutinas que superen este límite. El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad (por subrutina) es indefinido.

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

 

 





