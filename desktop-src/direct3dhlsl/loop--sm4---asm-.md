---
title: loop (sm4 - asm)
description: Especifica un bucle que recorre en iteración hasta que se encuentra una instrucción de interrupción.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dfc3090e71c1101e2c2748924de24f5443363ede76b86130cf63c3a319c76ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043773"
---
# <a name="loop-sm4---asm"></a>loop (sm4 - asm)

Especifica un bucle que recorre en iteración hasta que se encuentra una instrucción de interrupción.



| bucle |
|------|



 

## <a name="remarks"></a>Comentarios

**Loop** puede iterar indefinidamente, aunque la ejecución general del sombreador se puede forzar a finalizar después de ejecutar un número de instrucciones.

Flow bloques de control pueden anidar hasta 64 profundidades por subrutina y principal. El compilador HLSL no generará subrutinas que superen este límite. El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad por subrutina no está definido.

El formato del token contiene el desplazamiento de la instrucción [endloop](endloop--sm4---asm-.md) correspondiente en el sombreador por comodidad.

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



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




