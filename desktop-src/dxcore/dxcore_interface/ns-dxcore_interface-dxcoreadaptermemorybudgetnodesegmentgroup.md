---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Describe un grupo de segmentos de memoria para un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b39557226034e9462e8d51c79aa9b8276659cfe296138df2a3a57f279106f5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118659"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a>DXCoreAdapterMemoryBudgetNodeSegmentGroup (estructura)

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

Especifica el adaptador físico del dispositivo para el que se consulta la información de memoria del adaptador. Para la operación de adaptador único, establezca esta opción en cero. Si hay varios nodos de adaptador, establezca esta opción en el índice del nodo (el adaptador físico del dispositivo) para el que desea consultar la información de memoria del adaptador (consulte [Sistemas multi-adaptador](../../direct3d12/multi-engine.md)).

### <a name="segmentgroup"></a>segmentGroup

Tipo: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**

Especifica la agrupación de segmentos de memoria del adaptador sobre la que desea consultar.

## <a name="see-also"></a>Consulte también

[Referencia de DXCore](../dxcore-reference.md)

[Uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)

[Sistemas de varios adaptadores](../../direct3d12/multi-engine.md)