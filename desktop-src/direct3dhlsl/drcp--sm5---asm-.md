---
title: drcp (sm5 - asm)
description: Calcula un recíproco de precisión doble por componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264196"
---
# <a name="drcp-sm5---asm"></a>drcp (sm5 - asm)

Calcula un recíproco de precisión doble por componente.



| rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados<br/> *dest*  =  **1.0**  /  *src0*. El valor del resultado debe ser preciso en 1,0 ULP<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El número del que se debe tomar el recíproco.<br/>                                                                         |



 

## <a name="remarks"></a>Observaciones

El compilador HLSL emite la instrucción DRCP solo cuando se llama explícitamente a través del intrínseco rcp(), cuando se usa double como argumento. La precisión de esta instrucción debe ser 1.0 ULP.

Los sombreadores que usan esta instrucción se marcarán con una marca de sombreador que hará que no se enlacen a menos que se cumplen todas las condiciones siguientes.

-   El sistema admite DirectX 11.1.
-   El sistema incluye un controlador WDDM 1.2.
-   El controlador notifica la compatibilidad con esta instrucción a través de **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** establecido en **TRUE.**

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzcan desbordamientos ni subdesbordes.

En esta tabla, F significa número finito-real.



| **Fuente**->  | **-inf** | **-F** | **-0** | **+0** | **+F** | **+inf** | **NaN** |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| **Dest**-> | -0       | -F     | -inf   | +inf   | +F     | +0       | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





