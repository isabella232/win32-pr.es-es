---
title: RSQ (SM4-ASM)
description: Raíz cuadrada recíproca de los componentes.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc274f927151938be055150d5b17287f9be0004d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077118"
---
# <a name="rsq-sm4---asm"></a>RSQ (SM4-ASM)

Raíz cuadrada recíproca de los componentes.



| RSQ \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] contiene los resultados de la operación.<br/> *dest* = 1.0 f/sqrt (*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes de la operación.<br/>                                              |



 

## <a name="remarks"></a>Observaciones

El error relativo máximo es 2-21.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.

F significa número finito-real.



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **src**  | **-INF** | **-F** | **-denormalización** | **-0** | **+0** | **+ denormalización** | **+ F** | **+ INF** | **NaN** |
| **dest** | NaN      | NaN    | -inf        | -inf   | +inf   | +inf        | +F     | +0       | NaN     |



 

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

 

 





