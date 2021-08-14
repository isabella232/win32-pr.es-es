---
title: switch (sm4 - asm)
description: Transfiere el control a un bloque de instrucciones diferente dentro del cuerpo del conmutador en función del valor de un selector.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39cb304c1ccf59c188a4e1f20f2b136897d833c80d6eb67cb0eb683d628ab9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724356"
---
# <a name="switch-sm4---asm"></a>switch (sm4 - asm)

Transfiere el control a un bloque de instrucciones diferente dentro del cuerpo del conmutador en función del valor de un selector.



| switch src0.selected \_ (componente) |
|---------------------------------|



 



| Elemento                                                            | Descripción                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el selector de la instrucción switch.<br/> |



 

## <a name="remarks"></a>Comentarios

Una construcción switch endswitch se comporta exactamente como una construcción switch en el lenguaje C, con la siguiente excepción: para las instrucciones predeterminadas del caso / [](endswitch--sm4---asm-.md) D3D11  que pasan al siguiente caso predeterminado sin una interrupción, no pueden tener código [](case--sm4---asm-.md) / [](default--sm4---asm-.md)  /  en ellas. [](break--sm4---asm-.md) Se permite que varias instrucciones **case,** incluido el valor predeterminado **,** aparezcan secuencialmente, compartiendo el mismo bloque de código.

La condición debe ser un componente de registro de 32 bits o una cantidad inmediata. La comparación de igualdad es bit a bit (entero).

Al igual que con cualquier instrucción shader en D3D11, el hardware puede implementar o no la construcción **del conmutador** directamente.

**Las** instrucciones Switch se pueden anidar. Cada **bloque** de modificador cuenta como un nivel con respecto al límite de profundidad de anidamiento del control de flujo de 64 por subrutina y principal, independientemente del número de instrucciones **case.** El compilador HLSL no generará subrutinas que superen este límite. El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad por subrutina no está definido.

En el ejemplo siguiente se muestra cómo usar esta instrucción.

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
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

 

 





