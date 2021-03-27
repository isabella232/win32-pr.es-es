---
title: mul (SM4-ASM)
description: Multiplicación por componentes.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ae22bcb9344936f9bc63e9b4fddf72dd8f6570
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358499"
---
# <a name="mul-sm4---asm"></a>mul (SM4-ASM)

Multiplicación por componentes.



| mul \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                        |
|-----------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] el resultado de la operación. dest = src0 \* SRC1<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] multiplicando.<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] el multiplicador.<br/>                                  |



 

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.

F significa número finito-real.



|                     |          |        |          |             |        |        |            |          |        |          |         |
|---------------------|----------|--------|----------|-------------|--------|--------|------------|----------|--------|----------|---------|
| **src0 SRC1->** | **-INF** | **-F** | **-1,0** | **-denormalización** | **-0** | **+0** | **desnormativa** | **+ 1,0** | **+ F** | **+ INF** | **NaN** |
| **-INF**            | +inf     | +inf   | +inf     | NaN         | NaN    | NaN    | NaN        | -inf     | -inf   | -inf     | NaN     |
| **-F**              | +inf     | +F     | -src0    | +0          | +0     | -0     | -0         | src0     | -F     | -inf     | NaN     |
| **-1**              | +inf     | -SRC1  | + 1,0     | +0          | +0     | -0     | -0         | -1.0     | -SRC1  | -inf     | NaN     |
| **-denormalización**         | NaN      | +0     | +0       | +0          | +0     | -0     | -0         | -0       | -0     | NaN      | NaN     |
| **-0**              | NaN      | +0     | +0       | +0          | +0     | -0     | -0         | -0       | -0     | NaN      | NaN     |
| **+0**              | Una     | -0     | -0       | -0          | -0     | +0     | +0         | +0       | +0     | NaN      | NaN     |
| **+ denormalización**         | NaN      | -0     | -0       | -0          | -0     | +0     | +0         | +0       | +0     | NaN      | NaN     |
| **+ 1,0**            | -inf     | src1   | -1.0     | -0          | -0     | +0     | +0         | + 1,0     | src1   | +inf     | NaN     |
| **+ F**              | -inf     | -F     | -src0    | -0          | -0     | +0     | +0         | src0     | +F     | +inf     | NaN     |
| **+ INF**            | -inf     | -inf   | -inf     | NaN         | NaN    | NaN    | NaN        | +inf     | +inf   | +inf     | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN         | NaN    | NaN    | NaN        | NaN      | NaN    | NaN      | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





