---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Describe un grupo de segmentos de memoria para un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420857"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a>Estructura DXCoreAdapterMemoryBudgetNodeSegmentGroup

Describe un grupo de segmentos de memoria para un adaptador.

## <a name="syntax"></a>Sintaxis

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a>Miembros

### <a name="nodeindex"></a>nodeIndex

Tipo: **uint32_t**

Especifica el adaptador físico del dispositivo para el que se consulta la información de memoria del adaptador. En el caso de una operación de un solo adaptador, establezca este valor en cero. Si hay varios nodos de adaptador, establézcalo en el índice del nodo (el adaptador físico del dispositivo) para el que desea consultar la información de memoria del adaptador (consulte sistemas de [varios adaptadores](../../direct3d12/multi-engine.md)).

### <a name="segmentgroup"></a>segmentGroup

Tipo: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Especifica la agrupación de segmentos de memoria del adaptador que desea consultar.

## <a name="see-also"></a>Vea también

[Referencia de DXCore](../dxcore-reference.md)

[Uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)

[Sistemas de varios adaptadores](../../direct3d12/multi-engine.md)