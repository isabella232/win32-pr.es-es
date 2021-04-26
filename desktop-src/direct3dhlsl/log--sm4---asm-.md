---
title: log (sm4 - asm)
description: Base de registro 2 por componentes.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998322"
---
# <a name="log-sm4---asm"></a>log (sm4 - asm)

Base de registro 2 por componentes.



| log \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle |
|----------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> dest = log2(src0)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El valor de la operación.<br/>                                             |



 

## <a name="remarks"></a>Comentarios

### <a name="restrictions"></a>Restricciones

-   Sigue la teoría del límite.
-   Tolerancia a errores: si *src0* es \[ 0.5..2, el error absolue no debe ser superior a \] 2-21. Si *src0* es (0..0.5) o (2..+INF), el error relativo no debe ser superior a \] 2-21.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento. F significa número finito-real.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | NaN      | NaN    | -inf        | -inf   | -inf   | -inf        | F      | +inf     | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





