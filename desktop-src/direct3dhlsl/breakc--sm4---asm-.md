---
title: breakc (SM4-ASM)
description: Mueve condicionalmente el punto de ejecución a la instrucción después del siguiente ENDLOOP o endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419943"
---
# <a name="breakc-sm4---asm"></a>breakc (SM4-ASM)

Mueve condicionalmente el punto de ejecución a la instrucción después del siguiente [ENDLOOP](endloop--sm4---asm-.md) o [endswitch](endswitch--sm4---asm-.md).



| breakc { \_ z \|\_NZ} src0. Select ( \_ componente) |
|------------------------------------------|



 



| Elemento                                                            | Descripción                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el componente en el que se va a probar la condición.<br/> |



 

## <a name="remarks"></a>Observaciones

El formato de token contiene el desplazamiento de la instrucción **ENDLOOP** correspondiente en el sombreador como una comodidad.

En el ejemplo siguiente se muestra la instrucción **breakc** .


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



Esta instrucción debe aparecer dentro de un **bucle** / **ENDLOOP** o **Switch** / **endswitch**.

El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits. Si algún bit es distinto de cero, **breakc \_ NZ** realizará la interrupción. Si todos los bits son cero, **breakc \_ z** llevará a cabo la interrupción.

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

 

 





