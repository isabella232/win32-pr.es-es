---
title: DXCoreSegmentGroup
description: Define constantes que especifican la agrupación de segmentos de memoria de un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2474f8084035ddb67f7081ea45cd1d1743c053415a7bbade68ecff3d4527636c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279627"
---
# <a name="dxcoresegmentgroup-enum"></a>Enumeración DXCoreSegmentGroup

Define constantes que especifican la agrupación de segmentos de memoria de un adaptador.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a>Constantes

### <a name="local"></a>Local

Especifica una agrupación de segmentos que se considera local para el adaptador y representa la memoria más rápida disponible para la GPU. La aplicación debe tener como destino el grupo de segmentos local como el tamaño de destino de su conjunto de trabajo.

### <a name="nonlocal"></a>NonLocal

Especifica una agrupación de segmentos que se considera no local para el adaptador y puede tener un rendimiento más lento que el grupo de segmentos local.

## <a name="see-also"></a>Consulte también

[Referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)