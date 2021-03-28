---
title: DFMA (SM5-ASM)
description: Realiza una adición con fusibles-Multiply.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358479"
---
# <a name="dfma-sm5---asm"></a>DFMA (SM5-ASM)

Realiza una adición con fusibles-Multiply.



| DFMA \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación. El valor del resultado debe ser preciso para 0,5 ULP.<br/> *dest*  =  *src0* \* *SRC1*  +  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes que se van a multiplicar por *SRC1*.<br/>                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] los componentes que se van a multiplicar por *src0*.<br/>                                                                                                 |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] los componentes que se van a agregar a *src0* \* *SRC1*.<br/>                                                                                               |



 

## <a name="remarks"></a>Observaciones

Los sombreadores que usan esta instrucción se marcarán con una marca de sombreador que hará que no se puedan enlazar a menos que se cumplan todas las condiciones siguientes.

-   El sistema admite DirectX 11,1.
-   El sistema incluye un controlador WDDM 1,2.
-   El controlador informa de la compatibilidad con esta instrucción a través de **\_ las opciones de D3D11 de datos de características de D3D11 \_ \_ \_ . ExtendedDoublesShaderInstructions** establecido en **true**.

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

 

 





