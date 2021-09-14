---
title: continuec (sm4 - asm)
description: Continúa la ejecución condicionalmente al principio del bucle actual.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264359"
---
# <a name="continuec-sm4---asm"></a>continuec (sm4 - asm)

Continúa la ejecución condicionalmente al principio del bucle actual.



| continuec{ \_ z\|\_Componente nz} src0.select \_ |
|---------------------------------------------|



 



| Término                                                            | Descripción                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Componente con el que se va a probar la condición.<br/> |



 

## <a name="remarks"></a>Observaciones

**continuec** solo se puede usar dentro de [un bucle](loop--sm4---asm-.md) o [endloop](endloop--sm4---asm-.md).

En el ejemplo siguiente se muestra cómo usar la **instrucción continuec.**


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



El formato del token contiene el desplazamiento de la instrucción de bucle correspondiente en el sombreador por comodidad.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





