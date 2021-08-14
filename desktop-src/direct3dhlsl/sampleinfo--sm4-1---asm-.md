---
title: sampleinfo (sm4.1 - asm)
description: Consulta el número de muestras en una vista de recursos de sombreador determinada o en el rasterizador.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2227afbf7a08a0010efc2efb8fcf87bae85c8f5775e596d92b761b556f8bfb93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510473"
---
# <a name="sampleinfo-sm41---asm"></a>sampleinfo (sm4.1 - asm)

Consulta el número de muestras en una vista de recursos de sombreador determinada o en el rasterizador.



| \[\_uint \] dest \[ .mask \] , srcResource \[ .swzzle\] |
|---------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] El recurso del sombreador.<br/>                         |



 

## <a name="remarks"></a>Comentarios

Esta instrucción devuelve el número de muestras para el recurso especificado o el rasterizador. Solo es válido para los recursos que se pueden cargar mediante [**ld2dms**](ld2dms--sm4-1---asm-.md) a menos que el rasterizador se especifique *como srcResource*. *srcResource podría* ser un registro t \# (una vista de recursos de sombreador) o un registro de rasterizador.

La instrucción calcula el vector (SampleCount,0,0,0).

Swzzle en *srcResource permite* que los valores devueltos se desdoleguen arbitrariamente antes de que se escriban en el destino. El valor devuelto es de punto flotante, a menos que se utilice el modificador uint, en cuyo caso el \_ valor devuelto es integer. Si no hay ningún recurso enlazado a la ranura especificada, se devuelve 0.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





