---
title: descartar (SM4-ASM)
description: Marca condicionalmente los resultados del sombreador de píxeles que se descartan cuando se alcanza el final del programa.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994827"
---
# <a name="discard-sm4---asm"></a>descartar (SM4-ASM)

Marca condicionalmente los resultados del sombreador de píxeles que se descartan cuando se alcanza el final del programa.



| descartar { \_ z \|\_NZ} src0. Select ( \_ componente) |
|-------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el valor que determina si se va a descartar el píxel actual que se está procesando.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción marca el píxel actual como terminado, mientras continúa la ejecución, de modo que otros píxeles que se ejecuten en paralelo puedan obtener derivados si es necesario. Aunque la ejecución continúa, se descartan todos los resultados del sombreador de píxeles antes o después de la instrucción de **descarte** .

Para **descartar \_ z**, si todos los bits del *\_ componente src0. Select* son cero, se descarta el píxel.

Para **descartar \_ NZ**, si algún bit del *\_ componente src0. Select* es distinto de cero, se descarta el píxel.

Además, la instrucción **discard** puede estar presente dentro de cualquier construcción de control de flujo.

Pueden existir varias instrucciones de **descarte** en un sombreador y, si se ejecuta alguna, se termina el píxel.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





