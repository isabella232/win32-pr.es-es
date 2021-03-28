---
title: exp (SM4-ASM)
description: 2exponent de los componentes.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 774be1230bdb02a6179ea5662ca2237c2cefc200
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077070"
---
# <a name="exp-sm4---asm"></a>exp (SM4-ASM)

2exponent de los componentes.



| EXP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] el resultado de la operación.<br/> *dest* = 2 *src0*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el exponente.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

Esta instrucción sigue la teoría del límite. El error relativo máximo es 2-21.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento. En esta tabla F se indica un número finito-real.



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **src**  | **-INF** | **-F** | **-denormalización** | **-0** | **+0** | **+ denormalización** | **+ F** | **+ INF** | **NaN** |
| **dest** | 0        | +F     | 1           | 1      | 1      | 1           | +F     | +inf     | NaN     |



 

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

 

 





