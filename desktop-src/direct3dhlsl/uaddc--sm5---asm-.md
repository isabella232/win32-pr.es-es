---
title: uaddc (SM5-ASM)
description: Entero sin signo agregar con transporte.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532866"
---
# <a name="uaddc-sm5---asm"></a>uaddc (SM5-ASM)

Entero sin signo agregar con transporte.



| uaddc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                               | Descripción                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[en \] la dirección del resultado.<br/>               |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[en \] 1 si se produce el transporte. De lo contrario, es 0.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[en \] el operando de 32 bits que se va a agregar.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/>    | \[en \] el operando de 32 bits que se va a agregar.<br/>          |



 

## <a name="remarks"></a>Observaciones

*dest1* puede ser null si no se necesita el transporte.

Use esta instrucción para la aritmética de alta precisión.

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

 

 





