---
title: SV_InsideTessFactor
description: Define la cantidad de teselación dentro de una superficie de revisión.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 043d1a43186623e81cb529d2906d4475291547d326bf2d75758c8ee696a812b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285511"
---
# <a name="sv_insidetessfactor"></a>SV \_ InsideTessFactor

Define la cantidad de teselación dentro de una superficie de revisión.

## <a name="type"></a>Tipo



|  Tipo          | Topología de entrada               |
|------------|----------------|
| float \[ 2\] | revisión quad     |
| FLOAT      | revisión tri      |
| unused     | Isolínea        |



 

Los factores de teselación deben declararse como matriz; no se pueden empaquetar en un solo vector.

## <a name="remarks"></a>Comentarios

Este valor debe definirse durante la función de constante de revisión del sombreador de casco.

Valor de salida requerido para el sombreador de casco si se usan revisiones quad o tri. Este valor es una entrada necesaria para el sombreador de dominio con el fin de que el hardware coincida con las firmas a través del teselador.

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




