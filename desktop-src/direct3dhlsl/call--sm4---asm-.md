---
title: call (sm4 - asm)
description: Llama a una subrutina marcada por donde aparece la etiqueta l\ en el programa.
ms.assetid: D6B7C52D-2CF7-44DB-81E3-2945477EF94A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c55ce1c0005014928c006e29c9d7d08c3cadc3d11fee870ea1c9fa39df514fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516658"
---
# <a name="call-sm4---asm"></a>call (sm4 - asm)

Llama a una subrutina marcada por donde aparece la etiqueta **l \#** en el programa.



| llamar a l\# |
|----------|



 



| Elemento                                                       | Descripción                                    |
|------------------------------------------------------------|------------------------------------------------|
| <span id="l_"></span><span id="L_"></span>*L\#*<br/> | \[en \] La etiqueta de la subrutina.<br/> |



 

## <a name="remarks"></a>Comentarios

Cuando se [encuentra un ret,](ret--sm4---asm-.md) devuelve la ejecución a la instrucción después de esta llamada.

El formato del token contiene el desplazamiento de la etiqueta correspondiente en el sombreador por comodidad.

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

-   Las subrutinas pueden anidar 32 profundidades.
-   La implementación administra la pila de direcciones de devolución de forma transparente.
-   Si ya hay 32 entradas en la  pila de direcciones de devolución y se emite una llamada, se omite la llamada.
-   No hay ninguna pila de parámetros automática. La aplicación puede usar una matriz de registro temporal indexable (x \# \[ \] ) para implementar manualmente una pila. Sin embargo, las direcciones de devolución de llamadas de subrutina no son visibles y son ortogonales para cualquier administración manual de pila realizada por la aplicación.
-   No se permite la indexación del parámetro *l. \#*
-   No se permite la recursividad.

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

 

 





