---
title: samplepos (SM 4.1-ASM)
description: Consulta la posición de una muestra en una vista de recursos de sombreador determinada o en el rasterizador.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419976"
---
# <a name="samplepos-sm41---asm"></a>samplepos (SM 4.1-ASM)

Consulta la posición de una muestra en una vista de recursos de sombreador determinada o en el rasterizador.



| samplepos dest \[ . Mask \] , srcResource \[ . swizzle \] , sampleIndex (operando escalar) |
|--------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección de los resultados de la operación.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] el recurso de sombreador.<br/>                         |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[en \] el índice del ejemplo.<br/>                     |



 

## <a name="remarks"></a>Observaciones

Esta instrucción devuelve la posición de ejemplo en 2D del *sampleIndex* de ejemplo para el recurso especificado. Solo es válido para los recursos que se pueden cargar mediante [**ld2dms**](ld2dms--sm4-1---asm-.md) a menos que el rasterizador se especifique como *srcResource*.

*srcResource* puede ser un registro de t \# (una vista de recursos del sombreador) o un registro de rasterizador.

La instrucción calcula el vector de punto flotante (XPosition, YPosition, 0,0).

Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino. La posición del ejemplo es relativa al centro del píxel, basado en el sistema de coordenadas de píxeles.

Si *sampleIndex* está fuera de los límites, se devuelve un vector de cero. Si no hay ningún recurso enlazado a la ranura especificada, se devuelve 0.

**samplepos** se puede usar para cosas como las resoluciones personalizadas en el código del sombreador.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





