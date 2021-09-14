---
description: Recupera el índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de estructura de aceleración de nivel inferior.
ms.assetid: ''
title: PrimitiveIndex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrimitiveIndex
api_type:
- NA
ms.openlocfilehash: d6d1e8ba338a3fb567b583b42074210b514ef360
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072925"
---
# <a name="primitiveindex-function"></a>Función PrimitiveIndex

Recupera el índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de estructura de aceleración de nivel inferior.

## <a name="syntax"></a>Sintaxis

```
uint PrimitiveIndex();
```

## <a name="remarks"></a>Observaciones

Para **D3D12 \_ RAYTRACING \_ GEOMETRY TYPE \_ \_ TRIANGLES**, este es el índice de triángulo dentro del objeto geometry.

Para **D3D12 \_ RAYTRACING \_ GEOMETRY TYPE PROCEDURAL PRIMITIVE \_ \_ \_ \_ AABBS**, este es el índice de la matriz AABB que define el objeto geometry.

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)

## <a name="see-also"></a>Consulte también

* [Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
