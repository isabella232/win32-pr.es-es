---
title: break (sm4 - asm)
description: Mueve el punto de ejecución a la instrucción después del siguiente endloop o endswitch.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17ca99b0e16da016145f7f23fe6e4ce6bd410325ff98d4c6dd1387943fbc718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983345"
---
# <a name="break-sm4---asm"></a>break (sm4 - asm)

Mueve el punto de ejecución a la instrucción después del [siguiente endloop](endloop--sm4---asm-.md) o [endswitch](endswitch--sm4---asm-.md).



| break |
|-------|



 

## <a name="remarks"></a>Comentarios

El formato del token contiene el desplazamiento de la instrucción **endloop** o **endswitch** correspondiente en el sombreador por comodidad.

En el ejemplo siguiente se muestra la **instrucción break.**


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



Esta instrucción debe aparecer dentro de **un** / **bucle endloop** o en un **caso en** un **conmutador** / **endswitch**.

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

 

 




