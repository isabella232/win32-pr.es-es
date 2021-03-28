---
title: sampleinfo (SM 4.1-ASM)
description: Consulta el número de muestras en una vista de recursos de sombreador determinada o en el rasterizador.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904307"
---
# <a name="sampleinfo-sm41---asm"></a>sampleinfo (SM 4.1-ASM)

Consulta el número de muestras en una vista de recursos de sombreador determinada o en el rasterizador.



| \[\_uint \] dest \[ . Mask \] , srcResource \[ . swizzle\] |
|---------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección de los resultados de la operación.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] el recurso de sombreador.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Esta instrucción devuelve el número de muestras para el recurso o el rasterizador especificados. Solo es válido para los recursos que se pueden cargar mediante [**ld2dms**](ld2dms--sm4-1---asm-.md) a menos que el rasterizador se especifique como *srcResource*. *srcResource* podría ser un registro de t \# (una vista de recursos del sombreador) o un registro de rasterizador.

La instrucción calcula el vector (SampleCount, 0, 0,0).

Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino. El valor devuelto es el punto flotante, a menos que \_ se use el modificador uint, en cuyo caso el valor devuelto es Integer. Si no hay ningún recurso enlazado a la ranura especificada, se devuelve 0.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





