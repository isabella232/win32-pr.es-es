---
title: llamada (SM4-ASM)
description: Llama a una subrutina marcada por donde aparece la etiqueta l \ en el programa.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dac86fa52140968443f01050cebc57718fea420
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784936"
---
# <a name="call-sm4---asm"></a>llamada (SM4-ASM)

Llama a una subrutina marcada por donde aparece la etiqueta **l \#** en el programa.



| llamar a l\# |
|----------|



 



| Elemento                                                       | Descripción                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span id="l_"></span><span id="L_"></span>*CG\#*<br/> | \[en \] la etiqueta de la subrutina.<br/> |



 

## <a name="remarks"></a>Observaciones

Cuando se encuentra un [RET](ret--sm4---asm-.md) , se devuelve la ejecución a la instrucción después de esta llamada.

El formato de token contiene el desplazamiento de la etiqueta correspondiente en el sombreador para mayor comodidad.

En el ejemplo siguiente se muestra la instrucción de llamada.


```
                ...
                call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret
```



### <a name="restrictions"></a>Restricciones

-   Las subrutinas pueden anidar 32 profundidad.
-   La pila de direcciones devueltas se administra de forma transparente en la implementación.
-   Si ya hay 32 entradas en la pila de direcciones devueltas y se emite una **llamada** , se omite la llamada.
-   No hay ninguna pila de parámetros automática. La aplicación puede usar una matriz de registro temporal indexable (x \# \[ \] ) para implementar manualmente una pila. Sin embargo, las direcciones de devolución de llamada de subrutina no son visibles y son ortogonales a cualquier administración de pila manual realizada por la aplicación.
-   No se permite la indexación del parámetro *l \#* .
-   No se permite la recursividad.

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

 

 





