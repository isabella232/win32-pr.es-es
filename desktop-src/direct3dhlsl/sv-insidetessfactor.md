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
ms.openlocfilehash: 4a05cabbb9410136d2bd82ee272ad92ff1b1f430
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104983766"
---
# <a name="sv_insidetessfactor"></a>VP \_ InsideTessFactor

Define la cantidad de teselación dentro de una superficie de revisión.

## <a name="type"></a>Tipo



|            |                |
|------------|----------------|
| Tipo       | Topología de entrada |
| Float \[ 2\] | revisión cuádruple     |
| FLOAT      | Tri patch      |
| unused     | isolínea        |



 

Los factores de teselación se deben declarar como una matriz; no se pueden empaquetar en un único vector.

## <a name="remarks"></a>Observaciones

Este valor debe definirse durante la función constante patch del sombreador de casco.

Valor de salida necesario para el sombreador de casco si se usan cuatro o tres revisiones. Este valor es una entrada necesaria para el sombreador de dominios con el fin de que el hardware coincida con las firmas a través de del teselador.

Esta función se admite en los siguientes tipos de sombreadores:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




