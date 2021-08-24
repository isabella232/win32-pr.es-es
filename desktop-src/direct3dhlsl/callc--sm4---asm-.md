---
title: callc (sm4 - asm)
description: Llama condicionalmente a una subrutina marcada por donde aparece la etiqueta l\ en el programa.
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb751b57a09704a2fec7a9c3afb69362873e3a1d2b43091efd984f67623188a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727165"
---
# <a name="callc-sm4---asm"></a>callc (sm4 - asm)

Llama condicionalmente a una subrutina marcada por donde aparece la **etiqueta l \#** en el programa.



| callc{ \_ z\|\_nz} src0.select \_ component, l\# |
|----------------------------------------------|



 



| Elemento                                                            | Descripción                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Componente en el que se va a probar la condición.<br/> |
| <span id="l_"></span><span id="L_"></span>*L\#*<br/>      | \[en \] La etiqueta de la subrutina.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Cuando se [encuentra un ret,](ret--sm4---asm-.md) devuelve la ejecución a la instrucción después de esta llamada.

El formato del token contiene el desplazamiento de la etiqueta correspondiente en el sombreador por comodidad.

En el ejemplo siguiente se muestra la instrucción de llamada.


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
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
-   Si ya hay 32 entradas en la  pila de direcciones de devolución y se emite una llamada, la llamada se omite.
-   No hay ninguna pila de parámetros automática. La aplicación puede usar una matriz de registro temporal indexable (x \# \[ \] ) para implementar manualmente una pila. Sin embargo, las direcciones de devolución de llamadas de subrutina no son visibles y son ortogonales para cualquier administración manual de la pila realizada por la aplicación.
-   No se permite la indexación del parámetro *l. \#*
-   El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits. Si algún bit es distinto de cero, **callc \_ nz** realizará la llamada. Si todos los bits son cero, **callc \_ z** realizará la llamada.
-   No se permite la recursividad.

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

 

 





