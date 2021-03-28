---
title: Switch (SM4-ASM)
description: Transfiere el control a un bloque de instrucciones distinto en el cuerpo del modificador en función del valor de un selector.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077096"
---
# <a name="switch-sm4---asm"></a>Switch (SM4-ASM)

Transfiere el control a un bloque de instrucciones distinto en el cuerpo del modificador en función del valor de un selector.



| cambiar src0. \_ componente seleccionado |
|---------------------------------|



 



| Elemento                                                            | Descripción                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el selector de la instrucción switch.<br/> |



 

## <a name="remarks"></a>Observaciones

Una construcción **Switch** / [endswitch](endswitch--sm4---asm-.md) se comporta exactamente como una construcción de **modificador** en el lenguaje C, con la siguiente excepción: para las [](case--sm4---asm-.md) / instrucciones [predeterminadas](default--sm4---asm-.md) de D3D11 case que pasen al siguiente **caso** / **predeterminado** sin [interrupción](break--sm4---asm-.md) no puede tener código en ellas. Se permite que varias instrucciones **Case** , como **default**, aparezcan secuencialmente, compartiendo el mismo bloque de código.

La condición debe ser un componente de registro de 32 bits o una cantidad inmediata. La comparación de igualdad es bit a bit (entero).

Como con cualquier instrucción del sombreador en el D3D11, el hardware puede o no implementar directamente la construcción **Switch** .

Las instrucciones **Switch** pueden estar anidadas. Cada bloque **Switch** cuenta como 1 nivel en el límite de profundidad de anidamiento del control de flujo de 64 por subrutina y principal, independientemente del número de instrucciones **Case** . El compilador de HLSL no generará subrutinas que superen este límite. El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad por subrutina es indefinido.

En el ejemplo siguiente se muestra cómo utilizar esta instrucción.

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

 

 





