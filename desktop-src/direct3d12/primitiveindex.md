---
description: Recupera el índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de la estructura de aceleración de nivel inferior.
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
ms.openlocfilehash: 809fda35a63addebfa95764e91d09996834a5911a3634976810d42917a035c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912347"
---
# <a name="primitiveindex-function"></a>Función PrimitiveIndex

Recupera el índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de la estructura de aceleración de nivel inferior.

## <a name="syntax"></a>Sintaxis

```
uint PrimitiveIndex();
```

## <a name="remarks"></a>Comentarios

Para **D3D12 \_ RAYTRACING \_ GEOMETRY TYPE \_ \_ TRIANGLES**, este es el índice de triángulo dentro del objeto geometry.

Para **D3D12 \_ RAYTRACING \_ GEOMETRY TYPE PROCEDURAL PRIMITIVE \_ \_ \_ \_ AABBS**, este es el índice de la matriz AABB que define el objeto geometry.

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)

## <a name="see-also"></a>Vea también

* [Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
