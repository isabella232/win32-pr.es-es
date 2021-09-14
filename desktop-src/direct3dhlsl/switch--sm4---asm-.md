---
title: switch (sm4 - asm)
description: Transfiere el control a un bloque de instrucciones diferente dentro del cuerpo del conmutador en función del valor de un selector.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966539"
---
# <a name="switch-sm4---asm"></a>switch (sm4 - asm)

Transfiere el control a un bloque de instrucciones diferente dentro del cuerpo del conmutador en función del valor de un selector.



| switch src0.selected \_ (componente) |
|---------------------------------|



 



| Elemento                                                            | Descripción                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el selector de la instrucción switch.<br/> |



 

## <a name="remarks"></a>Observaciones

Una construcción **switch** endswitch se comporta exactamente como una construcción switch en el lenguaje C, con la siguiente excepción: en el caso D3D11, las instrucciones predeterminadas del caso / [](endswitch--sm4---asm-.md) D3D11  que pasan al siguiente caso predeterminado sin una interrupción no pueden tener código [](case--sm4---asm-.md) / [](default--sm4---asm-.md)  /  en ellas. [](break--sm4---asm-.md) Se permite que varias instrucciones **case,** incluido el valor predeterminado **,** aparezcan secuencialmente, compartiendo el mismo bloque de código.

La condición debe ser un componente de registro de 32 bits o una cantidad inmediata. La comparación de igualdad es bit a bit (entero).

Al igual que con cualquier instrucción shader en D3D11, el hardware puede implementar o no la **construcción del** conmutador directamente.

**Las** instrucciones Switch se pueden anidar. Cada **bloque de** modificador cuenta como un nivel con respecto al límite de profundidad de anidamiento del control de flujo de 64 por subrutina y principal, independientemente del número de instrucciones **case.** El compilador HLSL no generará subrutinas que superen este límite. El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad por subrutina no está definido.

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
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





