---
title: ret (sm4 - asm)
description: Instrucción Return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7482c2c7351944824e2590f5c87dac63bde8f639a5ad42dffdfc71e4134603b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853755"
---
# <a name="ret-sm4---asm"></a>ret (sm4 - asm)

Instrucción Return.



| Ret |
|-----|



 

## <a name="remarks"></a>Comentarios

Si se encuentra dentro de una subrutina, vuelva a la instrucción después de la llamada. Si no está dentro de una subrutina, finalice la ejecución del programa.

En el ejemplo siguiente se muestra cómo usar esta instrucción.

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a>Restricciones

-   **ret** puede aparecer en cualquier lugar de un programa, cualquier número de veces.
-   Si una [instrucción de](label--sm4---asm-.md) etiqueta aparece en un sombreador, debe ir precedida de un **comando ret** que no esté anidado en ninguna instrucción de control de flujo.
-   Si hay subrutinas en un sombreador, la última instrucción del sombreador debe ser **un ret**.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




