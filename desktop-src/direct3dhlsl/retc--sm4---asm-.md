---
title: retc (sm4 - asm)
description: Devolución condicional.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d68d65cf64c3c1fb7945f93053f280be3eb3bd9d5fe76e34f30102316b1f1e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853745"
---
# <a name="retc-sm4---asm"></a>retc (sm4 - asm)

Devolución condicional.



| retc{ \_ z\|\_Componente nz} src0.select \_ |
|----------------------------------------|



 



| Elemento                                                            | Descripción                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El registro con el que se probará la condición.<br/> |



 

## <a name="remarks"></a>Comentarios

Si se encuentra dentro de una subrutina, esta instrucción vuelve condicionalmente a la instrucción después de la llamada. Si no está dentro de una subrutina, esta instrucción finaliza la ejecución del programa.

En el ejemplo siguiente se muestra cómo usar esta instrucción.

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

-   **retc** puede aparecer en cualquier lugar de un programa, cualquier número de veces.
-   La última instrucción de un programa principal o subrutina no puede ser **un retc \_ z** o **retc \_ nz**. En su lugar, se [puede usar el ret](ret--sm4---asm-.md) incondicional.
-   El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits. Si cualquier bit es distinto de cero, **ret \_ nz** devolverá . Si todos los bits son cero, **se devolverá retc \_ z.**

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

 

 





