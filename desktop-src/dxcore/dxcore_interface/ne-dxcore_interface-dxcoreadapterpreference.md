---
title: DXCoreAdapterPreference
description: Define constantes que especifican las preferencias del adaptador de DXCore que se van a usar como criterios de ordenación de lista.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421142"
---
# <a name="dxcoreadapterpreference-enum"></a>Enumeración DXCoreAdapterPreference

## <a name="description"></a>Descripción

Define constantes que especifican las preferencias del adaptador de DXCore que se van a usar como criterios de ordenación de lista. Puede ordenar una lista de adaptadores de DXCore pasando una matriz de **DXCoreAdapterPreference** a [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Sintaxis

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>Campos de enumeración

### <a name="hardware"></a>Hardware

Especifica una preferencia para los adaptadores de hardware (en contraposición a los adaptadores de software).

### <a name="minimumpower"></a>MinimumPower

Especifica una preferencia para la GPU con alimentación mínima (como un procesador de gráficos integrado o iGPU).

### <a name="highperformance"></a>HighPerformance

Especifica una preferencia para la GPU de mayor rendimiento, como un procesador de gráficos externo (xGPU), si está disponible, o el procesador de gráficos discretos (dGPU) si está disponible.

## <a name="see-also"></a>Vea también

[IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)