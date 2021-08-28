---
title: dcl_function_table (sm5 - asm)
description: Declare una tabla de funciones.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549653ee7316a664b628d5cdc692c091bdf042ad24e89b983c0fd3aac8a67ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490895"
---
# <a name="dcl_function_table-sm5---asm"></a>tabla de \_ funciones dcl \_ (sm5 - asm)

Declare una tabla de funciones.



| dcl \_ function table ft = \_ \# {fb , fb , \# \# ...} |
|-----------------------------------------------|



 



| Elemento                                                      | Descripción                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span id="ft"></span><span id="FT"></span>*Pies*<br/> | \[en \] Las entradas de la tabla de funciones.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta función declara una tabla de funciones como un conjunto de cuerpos de función que se han declarado anteriormente.

Esto es como una tabla virtual de C++, salvo que hay una entrada por sitio de llamada para una interfaz en lugar de por método.

No hay ningún límite en el número de cuerpos de función que se pueden enumerar en una tabla de funciones.

Es válido que se haga referencia a un determinado cuerpo de función fb varias veces en una o varias tablas de funciones, como una manera de \# compartir código común.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





