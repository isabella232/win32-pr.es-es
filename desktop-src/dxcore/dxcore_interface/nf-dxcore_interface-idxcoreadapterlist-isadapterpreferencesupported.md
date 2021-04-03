---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Determina si el sistema operativo entiende un valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792178"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>IDXCoreAdapterList:: IsAdapterPreferenceSupported (método)

## <a name="description"></a>Descripción

Determina si el sistema operativo (OS) actual entiende el valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado. Puede llamar a **IsAdapterPreferenceSupported** antes de llamar a [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Sintaxis

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a>Parámetros

### <a name="preference"></a>preference

Tipo: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**

Un valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) que se comprobará para ver si es compatible con el sistema operativo.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve `true` si el tipo de ordenación lo entiende el sistema operativo actual. De lo contrario, devuelve `false`.

## <a name="see-also"></a>Vea también

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)