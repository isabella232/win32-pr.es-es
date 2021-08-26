---
title: dfma (sm5 - asm)
description: Realiza una suma de multiplicación fusionada.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84952ed594ba8541223df072fa59550aded581e5517dee3d6f4168b7661a87aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068395"
---
# <a name="dfma-sm5---asm"></a>dfma (sm5 - asm)

Realiza una suma de multiplicación fusionada.



| dfma \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle, \] \[ - \] src1 \[ \_ abs \] \[ .sw swzzle , \] \[ - \] src2 abs \[ \_ \] \[ .sw swzzle\] |
|----------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación. El valor del resultado debe ser preciso a 0,5 ULP.<br/> *dest*  =  *src0* \* *src1*  +  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Componentes que se va a multiplicar por *src1*.<br/>                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Componentes que se va a multiplicar por *src0*.<br/>                                                                                                 |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] Componentes que se agregarán a *src0* \* *src1*.<br/>                                                                                               |



 

## <a name="remarks"></a>Comentarios

Los sombreadores que usan esta instrucción se marcarán con una marca de sombreador que hará que no se enlacen a menos que se cumplen todas las condiciones siguientes.

-   El sistema admite DirectX 11.1.
-   El sistema incluye un controlador WDDM 1.2.
-   El controlador notifica la compatibilidad con esta instrucción a través de **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** establecido en **TRUE.**

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

 

 





