---
title: div (SM4-ASM)
description: División por componentes.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d494adc2cc9bebe2e714b47ff2c5a6b299966
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077088"
---
# <a name="div-sm4---asm"></a>div (SM4-ASM)

División por componentes.



| div \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] el resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el dividendo.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] el divisor.<br/>                 |



 

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.

Tenga en cuenta las dos implementaciones permitidas de divide: a/b y a \* (1/b).

Un resultado de esto es que hay excepciones a la tabla siguiente para valores de denominador grandes (mayores que 8.5070592 e + 37), donde 1/denominador es una desnormativa. Dado que las implementaciones pueden realizar una división como \* (1/b), en lugar de a/b directamente, y \[ un valor de 1/grande \] es una desnormativa que se puede vaciar, algunos casos de la tabla generarán resultados diferentes. Por ejemplo, el valor de (+/-) INF/(+/-) \[ > 8.5070592 e + 37 \] puede producir Nan en algunas implementaciones, pero (+/-) inf en otras implementaciones

En esta tabla F se indica un número finito-real.



|                     |          |            |             |        |        |             |            |          |         |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **src0 SRC1->** | **-INF** | **-F**     | **-denormalización** | **-0** | **+0** | **+ denormalización** | **+ F**     | **+ INF** | **NError** |
| **-INF**            | -inf     | -inf       | -inf        | -inf   | -inf   | -inf        | -inf       | NaN      | NaN     |
| **-F**              | -inf     | -F         | src0        | src0   | src0   | src0        | +-F o +-0 | +inf     | NaN     |
| **-denormalización**         | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **-0**              | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **+0**              | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ denormalización**         | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ F**              | -inf     | +-F o +-0 | src0        | src0   | src0   | src0        | +F         | +inf     | NaN     |
| **+ INF**            | NaN      | +inf       | +inf        | +inf   | +inf   | +inf        | +inf       | +inf     | NaN     |
| **NaN**             | NaN      | NaN        | NaN         | NaN    | NaN    | NaN         | NaN        | NaN      | NaN     |



 

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

 

 





