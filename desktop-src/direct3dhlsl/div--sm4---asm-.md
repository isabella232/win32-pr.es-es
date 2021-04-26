---
title: div (sm4 - asm)
description: División por componente.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d406c5e61b4615990b445abe169619227d22124c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999102"
---
# <a name="div-sm4---asm"></a>div (sm4 - asm)

División por componente.



| div \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] \[ - \] src1 \[ \_ abs \] \[ .swzzle\] |
|-------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El dividendo.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] el divisor.<br/>                 |



 

## <a name="remarks"></a>Comentarios

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento.

Debe tener en cuenta las dos implementaciones permitidas de divide: a/b y a \* (1/b).

Un resultado de esto es que hay excepciones en la tabla siguiente para valores denominadores grandes (mayor que 8,5070592e+37), donde 1/denominador es un desnormado. Dado que las implementaciones pueden realizar la división como (1/b), en lugar de a/b directamente, y un valor grande de 1/ es un \* \[ desnorma que podría vaciarse, algunos casos de la tabla producirían resultados \] diferentes. Por ejemplo, el valor (+/-)INF / (+/-) \[ > 8.5070592e+37 puede generar NaN en algunas implementaciones, pero \] (+/-)INF en otras implementaciones

En esta tabla, F significa número finito-real.



| **src0 src1 ->** | **-inf** | **-F**     | **-denorm** | **-0** | **+0** | **+denorm** | **+F**     | **+inf** | **Nan** |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **-inf**            | -inf     | -inf       | -inf        | -inf   | -inf   | -inf        | -inf       | NaN      | NaN     |
| **-F**              | -inf     | -F         | src0        | src0   | src0   | src0        | +-F o +-0 | +inf     | NaN     |
| **-denorm**         | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **-0**              | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **+0**              | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+denorm**         | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+F**              | -inf     | +-F o +-0 | src0        | src0   | src0   | src0        | +F         | +inf     | NaN     |
| **+inf**            | NaN      | +inf       | +inf        | +inf   | +inf   | +inf        | +inf       | +inf     | NaN     |
| **NaN**             | NaN      | NaN        | NaN         | NaN    | NaN    | NaN         | NaN        | NaN      | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





