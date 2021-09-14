---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Describe un grupo de segmentos de memoria para un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964596"
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

## <a name="members"></a>Members

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