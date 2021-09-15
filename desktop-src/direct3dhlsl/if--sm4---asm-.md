---
title: if (sm4 - asm)
description: Rama basada en el resultado or lógico.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568932"
---
# <a name="if-sm4---asm"></a>if (sm4 - asm)

Rama basada en el resultado or lógico.



| if{ \_ z\|\_Componente nz} src0.select \_ |
|--------------------------------------|



 



| Elemento                                                            | Descripción                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Contiene el componente en el que se va a probar la condición.<br/> |



 

## <a name="remarks"></a>Observaciones

El formato del token contiene el desplazamiento de la instrucción endif correspondiente en el sombreador por comodidad.

En el ejemplo siguiente se muestra cómo usar esta instrucción.

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a>Restricciones

-   Los operandos de origen (si son 4 vectores de componente) deben usar un único selector de componentes.
-   El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits. Si algún bit es distinto de cero, **si \_ z** será true. Si todos los bits son cero, **\_ si nz** será true.
-   Flow bloques de control pueden anidar hasta 64 profundidades por subrutina (y main). El compilador HLSL no generará subrutinas que superen este límite. El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad (por subrutina) no está definido.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





