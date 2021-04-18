---
title: IDXCoreAdapterList::IsStale
description: Determina si los cambios en este sistema han dado lugar a que este objeto de lista de adaptadores de DXCore esté obsoleto.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720172"
---
# <a name="idxcoreadapterlistisstale-method"></a>IDXCoreAdapterList:: IsStale (método)

Determina si los cambios en este sistema han dado lugar a que este objeto de lista de adaptadores de DXCore esté obsoleto. Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve  `true`   si, desde que se genera la lista, se han producido cambios en las condiciones del sistema que podrían provocar que esta lista de adaptadores se quedara obsoleta. De lo contrario, devuelve  `false` .

## <a name="remarks"></a>Observaciones

Puede sondear **IsStale** para determinar si el cambio de condiciones del sistema ha provocado que esta lista no esté actualizada. Si **IsStale** devuelve `true` una vez, devuelve `true` para la duración restante del objeto de lista de adaptadores de DXCore. Un objeto de lista obsoleto se sigue considerando obsoleto aunque las condiciones del sistema vuelvan a un estado que coincida con la lista (las mismas condiciones se obtienen ahora como cuando se generó la lista por primera vez).

## <a name="see-also"></a>Vea también

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)