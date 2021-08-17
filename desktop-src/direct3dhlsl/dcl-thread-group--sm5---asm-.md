---
title: dcl_thread_group (sm5 - asm)
description: Declare el tamaño del grupo de subprocesos.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5402e53e2252d8019ba553c6a8ff449200625b1469ee923f3c26234f1faa292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515483"
---
# <a name="dcl_thread_group-sm5---asm"></a>grupo de subprocesos dcl \_ \_ (sm5 - asm)

Declare el tamaño del grupo de subprocesos.



| grupo de subprocesos dcl \_ \_ x, y, z |
|----------------------------|



 



| Elemento                                                   | Descripción                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] Un entero de 32 bits con signo. 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] Un entero de 32 bits con signo. 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*Z*<br/> | \[en \] Un entero de 32 bits con signo. 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>Comentarios

x \* y z <= \* 1024

Esta declaración de grupo de subprocesos debe aparecer una vez en un sombreador de proceso.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





