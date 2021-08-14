---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Determina si el sistema operativo entiende [un valor DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: f8a42040ecd6c5667a3d33fb506fd97cfdfe53e8950c2e42b6068bbed6c19467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502586"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>IDXCoreAdapterList::IsAdapterPreferenceSupported (método)

## <a name="description"></a>Descripción

Determina si el sistema operativo (SO) actual entiende un valor [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado. Puede llamar a **IsAdapterPreferenceSupported antes** de llamar a [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Sintaxis

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a>Parámetros

### <a name="preference"></a>preference

Tipo: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**

Valor [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) que se comprobará para ver si es compatible con el sistema operativo.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve `true` si el sistema operativo actual entiende el tipo de ordenación. De lo contrario, devuelve `false`.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapterList,](./nn-dxcore_interface-idxcoreadapterlist.md) [referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)