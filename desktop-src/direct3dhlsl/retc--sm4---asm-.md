---
title: RETC (SM4-ASM)
description: Devolución condicional.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983882"
---
# <a name="retc-sm4---asm"></a>RETC (SM4-ASM)

Devolución condicional.



| RETC { \_ z \|\_NZ} src0. Select ( \_ componente) |
|----------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el registro en el que se va a probar la condición.<br/> |



 

## <a name="remarks"></a>Observaciones

Si se encuentra dentro de una subrutina, esta instrucción devuelve condicionalmente a la instrucción después de la llamada. Si no está dentro de una subrutina, esta instrucción finaliza la ejecución del programa.

En el ejemplo siguiente se muestra cómo utilizar esta instrucción.

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a>Restricciones

-   **RETC** puede aparecer en cualquier parte de un programa, en cualquier número de veces.
-   La última instrucción de un programa o subrutina principal no puede ser **RETC \_ z** ni **RETC \_ NZ**. En su lugar, se puede usar el [RET](ret--sm4---asm-.md) incondicional.
-   El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits. Si un bit es distinto de cero, **RET \_ NZ** devolverá. Si todos los bits son cero, **RETC \_ z** devolverá.

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

 

 





