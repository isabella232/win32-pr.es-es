---
title: ddiv (sm5 - asm)
description: Calcula una división de precisión doble por componente.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999162"
---
# <a name="ddiv-sm5---asm"></a>ddiv (sm5 - asm)

Calcula una división de precisión doble por componente.



| ddiv \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swdivle \] \[ - \] src1 \[ \_ abs \] \[ .swdivle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación. El valor del resultado debe ser preciso a 0,5 ULP. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El dividendo.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] el divisor.<br/>                                                                |



 

## <a name="remarks"></a>Comentarios

El compilador HLSL emitirá la instrucción DDIV cada vez que se utilice el operador de división con doubles. La precisión de esta instrucción será de 0,5 ULP.

Los sombreadores que usan esta instrucción se marcarán con una marca de sombreador que hará que no se enlacen a menos que se cumplen todas las condiciones siguientes.

-   El sistema admite DirectX 11.1.
-   El sistema incluye un controlador WDDM 1.2.
-   El controlador informa de la compatibilidad con esta instrucción a través de **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** establecido en **TRUE.**

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzcan desbordamientos ni subdesbordes.

En esta tabla, F significa número finito-real.



| **src0 src1 ->** | **-inf** | **-F** | **-1.0** | **-0** | **+0** | **+1.0** | **+F** | **+inf** | **NaN** |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **-inf**            | NaN      | +inf   | +inf     | +inf   | -inf   | -inf     | -inf   | NaN      | NaN     |
| **-F**              | +0       | +F     | -src0    | +inf   | -inf   | src0     | -F     | -0       | NaN     |
| **-0**              | +0       | +0     | +0       | NaN    | NaN    | -0       | -0     | -0       | NaN     |
| **+0**              | -0       | -0     | -0       | NaN    | NaN    | +0       | +0     | +0       | NaN     |
| **+F**              | -0       | -F     | -src0    | -inf   | +inf   | src0     | +F     | +0       | NaN     |
| **+inf**            | NaN      | -inf   | -inf     | -inf   | +inf   | +inf     | +inf   | NaN      | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





