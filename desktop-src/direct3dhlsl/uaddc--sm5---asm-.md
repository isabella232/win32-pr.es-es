---
title: uaddc (sm5 - asm)
description: Entero sin signo que se agrega con carry.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f649ed68626e5b3351ee1b3c7d5848c8e42f7ec175b4b76c929571056f48e0c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722193"
---
# <a name="uaddc-sm5---asm"></a>uaddc (sm5 - asm)

Entero sin signo que se agrega con carry.



| uaddc dest0 \[ \] .mask, dest1 \[ \] .mask, src0 \[ .swzzle, \] src1 \[ .swzzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                               | Descripción                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[en \] Dirección del resultado.<br/>               |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[en \] 1 si se produce el transporte. De lo contrario, 0.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[en \] el operando de 32 bits que se va a agregar.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[en \] el operando de 32 bits que se va a agregar.<br/>          |



 

## <a name="remarks"></a>Comentarios

*dest1* puede ser NULL si no se necesita el transporte.

Use esta instrucción para aritmética de alta precisión.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
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

 

 





