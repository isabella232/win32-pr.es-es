---
title: RET (SM4-ASM)
description: Instrucción return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784918"
---
# <a name="ret-sm4---asm"></a>RET (SM4-ASM)

Instrucción return.



| direcc |
|-----|



 

## <a name="remarks"></a>Observaciones

Si se encuentra dentro de una subrutina, vuelva a la instrucción después de la llamada. Si no está dentro de una subrutina, finalice la ejecución del programa.

En el ejemplo siguiente se muestra cómo utilizar esta instrucción.

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

-   **RET** puede aparecer en cualquier parte de un programa, en cualquier número de veces.
-   Si aparece una instrucción de [etiqueta](label--sm4---asm-.md) en un sombreador, debe ir precedida de un comando **RET** que no esté anidado en las instrucciones de control de flujo.
-   Si hay subrutinas en un sombreador, la última instrucción del sombreador debe ser un **RET**.

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

 

 




