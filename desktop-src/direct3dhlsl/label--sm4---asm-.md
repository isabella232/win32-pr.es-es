---
title: etiqueta (SM4-ASM)
description: Indica el principio de una subrutina.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784954"
---
# <a name="label-sm4---asm"></a>etiqueta (SM4-ASM)

Indica el principio de una subrutina.



| etiqueta l\# |
|-----------|



 



| Elemento                                                       | Descripción                         |
|------------------------------------------------------------|-------------------------------------|
| <span id="l_"></span><span id="L_"></span>*CG\#*<br/> | \[en \] el número de etiqueta.<br/> |



 

## <a name="remarks"></a>Observaciones

Una **etiqueta** solo puede aparecer directamente después de una instrucción [**RET**](ret--sm4---asm-.md) que no está anidada en las instrucciones de control de flujo.

El código anterior a la primera **etiqueta** de un programa es el programa principal. Todas las subrutinas aparecen al final del programa, indicadas por las instrucciones de **etiqueta** .

En el ejemplo siguiente se muestra cómo utilizar esta instrucción.

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
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

 

 





