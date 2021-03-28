---
title: dcl_thread_group (SM5-ASM)
description: Declare el tamaño del grupo de subprocesos.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077120"
---
# <a name="dcl_thread_group-sm5---asm"></a>\_grupo de subprocesos DCL \_ (SM5-ASM)

Declare el tamaño del grupo de subprocesos.



| \_grupo de subprocesos DCL \_ x, y, z |
|----------------------------|



 



| Elemento                                                   | Descripción                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] un entero de usigned 32 bits. 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[en \] un entero de usigned 32 bits. 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*z*<br/> | \[en \] un entero de usigned 32 bits. 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>Observaciones

x \* y \* z <= 1024

Esta declaración de grupo de subprocesos debe aparecer una vez en un sombreador de cálculo.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





