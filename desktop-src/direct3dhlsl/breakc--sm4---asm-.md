---
title: breakc (sm4 - asm)
description: Mueve condicionalmente el punto de ejecución a la instrucción después del siguiente endloop o endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eff9be2428db0d0df24879f50964ce14f6831e235c54655958d9401224d7225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626475"
---
# <a name="breakc-sm4---asm"></a>breakc (sm4 - asm)

Mueve condicionalmente el punto de ejecución a la instrucción después del [siguiente endloop](endloop--sm4---asm-.md) o [endswitch](endswitch--sm4---asm-.md).



| breakc{ \_ z\|\_Componente nz} src0.select \_ |
|------------------------------------------|



 



| Elemento                                                            | Descripción                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El componente en el que se va a probar la condición.<br/> |



 

## <a name="remarks"></a>Comentarios

El formato del token contiene el desplazamiento de la instrucción **endloop** correspondiente en el sombreador por comodidad.

En el ejemplo siguiente se muestra **la instrucción breakc.**


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



Esta instrucción debe aparecer dentro de **un** / **bucle endloop** o **switch** / **endswitch**.

El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits. Si algún bit es distinto de cero, **breakc \_ nz** realizará la interrupción. Si todos los bits son cero, **breakc \_ z** realizará la interrupción.

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

 

 





