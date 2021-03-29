---
title: dcl_function_table (SM5-ASM)
description: Declare una tabla de función.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996993"
---
# <a name="dcl_function_table-sm5---asm"></a>\_ \_ tabla de funciones DCL (SM5-ASM)

Declare una tabla de función.



| \_ \_ tabla ft de la función DCL \# = {FB \# , FB \# ,...} |
|-----------------------------------------------|



 



| Elemento                                                      | Descripción                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span id="ft"></span><span id="FT"></span>*tolerancia*<br/> | \[en \] las entradas de la tabla de funciones.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta función declara una tabla de funciones como un conjunto de cuerpos de función que se han declarado anteriormente.

Esto es como una vtable de C++, salvo que hay una entrada por cada sitio de llamada para una interfaz en lugar de por método.

No hay ningún límite en el número de cuerpos de función que se pueden enumerar en una tabla de función.

Es válido para que \# se haga referencia varias veces a un cuerpo de función FB en una o varias tablas de funciones, como una manera de compartir código común.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





