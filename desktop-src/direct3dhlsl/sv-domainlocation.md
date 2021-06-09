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
ms.openlocfilehash: fc39a71bcbfb6f3719ecfc7d0abe463a1fd127e4
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827054"
---
# <a name="sv_domainlocation"></a>SV \_ DomainLocation

Define la ubicación en el casco del punto de dominio actual que se está evaluando.

## <a name="type"></a>Tipo



| Tipo       | Topología de entrada               |
|--------|----------------|
| float2 | revisión quad     |
| float3 | revisión tri      |
| float2 | Isolínea        |



 

## <a name="remarks"></a>Comentarios

Este valor del sistema es obligatorio.

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      | x      |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Semántica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




