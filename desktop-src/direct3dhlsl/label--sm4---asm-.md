---
title: label (sm4 - asm)
description: Indica el principio de una subrutina.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9075aa14d72893d7c7862361b44ff636dd9bb6fda62563087ca2404bd1d70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986465"
---
# <a name="label-sm4---asm"></a>label (sm4 - asm)

Indica el principio de una subrutina.



| etiqueta l\# |
|-----------|



 



| Elemento                                                       | Descripción                         |
|------------------------------------------------------------|-------------------------------------|
| <span id="l_"></span><span id="L_"></span>*L\#*<br/> | \[en \] El número de etiqueta.<br/> |



 

## <a name="remarks"></a>Comentarios

Una **etiqueta** solo puede aparecer directamente después de una [**instrucción ret**](ret--sm4---asm-.md) que no está anidada en ninguna instrucción de control de flujo.

El código anterior a la **primera etiqueta** de un programa es el programa principal. Todas las subrutinas aparecen al final del programa, indicadas por instrucciones **de** etiqueta.

En el ejemplo siguiente se muestra cómo usar esta instrucción.

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

 

 





