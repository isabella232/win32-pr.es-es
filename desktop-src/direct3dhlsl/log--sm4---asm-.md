---
title: registro (SM4-ASM)
description: Base de registro de componentes 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf99949e278ca302543437da346188b690789604
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077102"
---
# <a name="log-sm4---asm"></a>registro (SM4-ASM)

Base de registro de componentes 2.



| log \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle |
|----------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación.<br/> dest = LOG2 (src0)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el valor de la operación.<br/>                                             |



 

## <a name="remarks"></a>Observaciones

### <a name="restrictions"></a>Restricciones

-   Sigue la teoría de límites.
-   Tolerancia a errores: Si *src0* es \[ 0,5.. 2 \] , el error Absolue no debe ser superior a 2-21. Si *src0* es (0.. 0.5) o (2.. + inf \] , el error relativo no debe ser superior a 2-21.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento. F significa número finito-real.



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **src**  | **-INF** | **-F** | **-denormalización** | **-0** | **+0** | **+ denormalización** | **+ F** | **+ INF** | **NaN** |
| **dest** | NaN      | NaN    | -inf        | -inf   | -inf   | -inf        | F      | +inf     | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

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

 

 





