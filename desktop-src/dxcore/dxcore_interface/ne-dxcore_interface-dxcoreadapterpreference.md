---
title: DXCoreAdapterPreference
description: Define constantes que especifican las preferencias del adaptador de DXCore que se usarán como criterios de ordenación de lista.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: a58f2c948751d5217a89e52bc862057ac6a67c85bdf2fabed96c2b5ad68364cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117735"
---
# <a name="dxcoreadapterpreference-enum"></a>Enumeración DXCoreAdapterPreference

## <a name="description"></a>Descripción

Define constantes que especifican las preferencias del adaptador de DXCore que se usarán como criterios de ordenación de lista. Puede ordenar una lista de adaptadores dxcore pasando una matriz **de DXCoreAdapterPreference** a [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Syntax

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

Especifica una preferencia para los adaptadores de hardware (en lugar de los adaptadores de software).

### <a name="minimumpower"></a>MinimumPower

Especifica una preferencia para la GPU de potencia mínima (como un procesador de gráficos integrado o iGPU).

### <a name="highperformance"></a>HighPerformance

Especifica una preferencia para la GPU de mayor rendimiento, como un procesador de gráficos externo (xGPU), si está disponible, o un procesador de gráficos discretos (dGPU) si está disponible.

## <a name="see-also"></a>Vea también

[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [REFERENCIA DE DXCore](../dxcore-reference.md), [Uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)