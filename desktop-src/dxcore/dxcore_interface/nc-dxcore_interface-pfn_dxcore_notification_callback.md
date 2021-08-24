---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Función de devolución de llamada (implementada por la aplicación), a la que llama un objeto DXCore para eventos de notificación.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f86bef2d2183562b322cdc0b01ffb64d25b23bb64dd8967e09e2dd761f7654b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787105"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>PFN_DXCORE_NOTIFICATION_CALLBACK devolución de llamada

Función de devolución de llamada (implementada por la aplicación), a la que llama un objeto DXCore para eventos de notificación.

## <a name="syntax"></a>Sintaxis

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a>Parámetros

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Tipo de notificación que representa esta invocación. Consulte la tabla de [DXCoreNotificationType para](./ne-dxcore_interface-dxcorenotificationtype.md) obtener información sobre qué tipos son válidos con qué tipos de objetos.

### <a name="object"></a>object

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Objeto [IDXCoreAdapter o](./nn-dxcore_interface-idxcoreadapter.md) [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) que genera la notificación.

### <a name="context-in"></a>context [in]

Tipo: **\* void**

Puntero, que puede ser , a `nullptr` un objeto que contiene información de contexto.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [IDXCoreAdapterList,](./nn-dxcore_interface-idxcoreadapterlist.md) [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)