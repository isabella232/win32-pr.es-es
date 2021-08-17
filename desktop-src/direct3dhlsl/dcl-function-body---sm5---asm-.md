---
title: dcl_function_body (sm5 - asm)
description: Declare un cuerpo de función.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339e7f5d7edb91f4f3405b328286a9ae32a8108efdaafaba1f212870be7ff8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727239"
---
# <a name="dcl_function_body-sm5---asm"></a>Cuerpo de \_ la \_ función dcl (sm5 - asm)

Declare un cuerpo de función.



| fb del cuerpo \_ de \_ la función dcl\# |
|--------------------------|



 



| Elemento                                                          | Descripción                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*Fb\#*<br/> | \[en \] La etiqueta del lugar donde aparecerá la función.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta instrucción declara un cuerpo de función único cuyo código aparecerá más adelante en el programa en la etiqueta fb \# .

Los cuerpos de función se usan en declaraciones de tabla de funciones. Para obtener más información, vea [tabla de funciones dcl \_ \_ ](dcl-function-table---sm5---asm-.md).

En el sombreador de casco y el sombreador de dominios, donde hay varias fases (fase de punto de control, fase de bifurcación y fase de combinación), todos los cuerpos de función (etiqueta fb) aparecen después de todas las fases, en lugar de agruparse \# por fase.

No hay ningún límite en el número de cuerpos de función que pueden estar presentes.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





