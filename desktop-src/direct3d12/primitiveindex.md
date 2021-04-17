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
ms.openlocfilehash: d6d1e8ba338a3fb567b583b42074210b514ef360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705344"
---
# <a name="primitiveindex-function"></a>PrimitiveIndex función)

Recupera el índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de la estructura de aceleración de nivel inferior.

## <a name="syntax"></a>Sintaxis

```
uint PrimitiveIndex();
```

## <a name="remarks"></a>Observaciones

En el caso de los **\_ \_ \_ \_ triángulos del tipo de geometría D3D12 RAYTRACING**, es el índice del triángulo dentro del objeto Geometry.

Para **el \_ tipo de geometría D3D12 RAYTRACING \_ \_ \_ AABBS de procedimiento \_ primitivo \_**, es el índice de la matriz AABB que define el objeto Geometry.

Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)

## <a name="see-also"></a>Vea también

* [Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
