---
title: dcl_function_body (SM5-ASM)
description: Declarar un cuerpo de función.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104149009"
---
# <a name="dcl_function_body-sm5---asm"></a>\_ \_ cuerpo de la función DCL (SM5-ASM)

Declarar un cuerpo de función.



| cuerpo de la función de DCL \_ \_ FB\# |
|--------------------------|



 



| Elemento                                                          | Descripción                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*FB\#*<br/> | \[en \] la etiqueta del lugar donde aparecerá la función.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción declara un cuerpo de función único cuyo código aparecerá más adelante en el programa en la etiqueta FB \# .

Los cuerpos de función se utilizan en las declaraciones de tabla de función. Para obtener más información, consulte la [ \_ \_ tabla de funciones DCL](dcl-function-table---sm5---asm-.md).

En el sombreador de casco y el sombreador de dominios, donde hay varias fases (fase de punto de control, fase de bifurcación y fase de combinación), todos los cuerpos de función (etiqueta FB \# ) aparecen después de todas las fases, en lugar de agruparse por fase.

No hay ningún límite en el número de cuerpos de función que pueden estar presentes.

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

 

 





