---
title: bucle (SM4-ASM)
description: Especifica un bucle que recorre en iteración hasta que se encuentra una instrucción de salto.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996920"
---
# <a name="loop-sm4---asm"></a>bucle (SM4-ASM)

Especifica un bucle que recorre en iteración hasta que se encuentra una instrucción de salto.



| bucle |
|------|



 

## <a name="remarks"></a>Observaciones

**Loop** puede iterar indefinidamente, aunque se puede forzar la finalización de la ejecución general del sombreador después de que se ejecute un número indefinido de instrucciones.

Los bloques de control de flujo pueden anidar hasta 64 de profundidad por subrutina y principal. El compilador de HLSL no generará subrutinas que superen este límite. El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad por subrutina es indefinido.

El formato de token contiene el desplazamiento de la instrucción [ENDLOOP](endloop--sm4---asm-.md) correspondiente en el sombreador como una comodidad.

En el ejemplo siguiente se muestra cómo usar la instrucción de bucle.

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

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

 

 




