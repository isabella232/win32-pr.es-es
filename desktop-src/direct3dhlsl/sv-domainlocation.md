---
title: SV_DomainLocation
description: Define la ubicación en el casco del punto de dominio actual que se está evaluando.
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 481d4def3d13ee69138f31adaae3c7d90c2e27ab11702fe3191db94540d9835c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067535"
---
# <a name="sv_domainlocation"></a>SV \_ DomainLocation

Define la ubicación en el casco del punto de dominio actual que se está evaluando.

## <a name="type"></a>Tipo



| Tipo       | Topología de entrada               |
|--------|----------------|
| float2 | revisión quad     |
| float3 | tri patch      |
| float2 | Isolínea        |



 

## <a name="remarks"></a>Comentarios

Este valor del sistema es obligatorio.

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      | x      |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




