---
title: RCP (SM5-ASM)
description: Recíproco de componentes.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbaa2ffc29a4c3373009d9dec1b895710186e67
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532896"
---
# <a name="rcp-sm5---asm"></a>RCP (SM5-ASM)

Recíproco de componentes.



| RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección de los resultados<br/> *dest*  =  **1,0 f**  /  *src0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el número del que se va a tomar el recíproco.<br/>                             |



 

## <a name="remarks"></a>Observaciones

Use esta instrucción para el uso de la precisión reducida, independientemente de los estrictos requisitos de la división.

El error relativo máximo es 2-21. (La tolerancia de errores solo coincide con RSQ)

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.



|        |          |        |             |        |        |             |        |          |         |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| *src*  | **-INF** | **-F** | **-denormalización** | **-0** | **+0** | **+ denormalización** | **+ F** | **+ INF** | **NaN** |
| *dest* | -0       | -F     | -inf        | -inf   | +inf   | +inf        | +F     | +0       | NaN     |



 

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

 

 





