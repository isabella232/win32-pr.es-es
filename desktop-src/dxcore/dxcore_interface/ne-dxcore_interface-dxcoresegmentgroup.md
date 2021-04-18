---
title: DXCoreSegmentGroup
description: Define constantes que especifican la agrupación de segmentos de memoria de un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720152"
---
# <a name="dxcoresegmentgroup-enum"></a>Enumeración DXCoreSegmentGroup

Define constantes que especifican la agrupación de segmentos de memoria de un adaptador.

## <a name="syntax"></a>Sintaxis

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a>Constantes

### <a name="local"></a>Local

Especifica una agrupación de segmentos que se considera que son locales para el adaptador y representa la memoria más rápida disponible para la GPU. La aplicación debe tener como destino el grupo de segmentos local como el tamaño de destino de su espacio de trabajo.

### <a name="nonlocal"></a>No locales

Especifica una agrupación de segmentos que se considera no local en el adaptador y puede tener un rendimiento más lento que el grupo de segmentos local.

## <a name="see-also"></a>Vea también

[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)