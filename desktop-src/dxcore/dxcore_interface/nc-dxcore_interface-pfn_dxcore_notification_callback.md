---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Función de devolución de llamada (implementada por la aplicación), a la que llama un objeto DXCore para eventos de notificación.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995507"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>Devolución de llamada PFN_DXCORE_NOTIFICATION_CALLBACK

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

El tipo de notificación que representa esta invocación. Vea la tabla en [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) para obtener información sobre los tipos válidos con qué tipos de objetos.

### <a name="object"></a>object

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

El objeto [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) que genera la notificación.

### <a name="context-in"></a>contexto [in]

Tipo: **void \***

Un puntero, que puede ser `nullptr` , a un objeto que contiene información de contexto.

## <a name="see-also"></a>Vea también

[Referencia](../dxcore-reference.md)de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [usar DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)