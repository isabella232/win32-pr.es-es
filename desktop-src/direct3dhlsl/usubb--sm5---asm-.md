---
title: usubb (sm5 - asm)
description: Entero sin signo resta con prestada.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c2f70f39729f5245f7044945e9d3b233ec4f0893be27c5143f5c55989693b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721829"
---
# <a name="usubb-sm5---asm"></a>usubb (sm5 - asm)

Entero sin signo resta con prestada.



| usubb dest0 \[ .mask \] , dest1 \[ .mask \] , src0 \[ .sw swzzle, \] src1 \[ .swzzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                               | Descripción                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[en \] Contiene los resultados de LSAB de la instrucción.<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[en \] el componente correspondiente de *dest0* que especifica si se produjo un préstamo.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[en \] El valor del que se va a restar.<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[en \] La cantidad que se va a restar de *src0.*<br/>                                             |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza una resta sin signo por componente de operandos de 32 bits *src1* de *src0,* colocando la parte LSB del resultado de 32 bits *en dest0*.

El componente correspondiente de *dest1* se escribe con 1 si se produce un préstamo, 0 en caso contrario.

*dest1* puede ser NULL si no se necesita el préstamo.

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

 

 





