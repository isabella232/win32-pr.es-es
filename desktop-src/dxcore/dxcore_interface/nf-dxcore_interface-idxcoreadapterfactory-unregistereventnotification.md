---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Anula el registro de una notificación a la que se registró anteriormente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421205"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>IDXCoreAdapterFactory:: UnregisterEventNotification (método)

Anula el registro de una notificación a la que se registró anteriormente. Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="eventcookie"></a>eventCookie

Tipo: **uint32_t**

El valor de cookie (que se devuelve cuando llamó a [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) que representa un registro anterior para el que desea anular el registro.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor devuelto|Descripción|
|-|-|
|E_INVALIDARG|El valor de *eventCookie* no es una cookie válida que representa un registro anterior.|

## <a name="remarks"></a>Observaciones

**UnregisterEventNotification** devuelve solo después de que se hayan completado todas las devoluciones de llamada pendientes o en curso para este registro. DXCore garantiza que no se producirán nuevas devoluciones de llamada para este registro después de que se devuelva **UnregisterEventNotification** . Sin embargo, para evitar un interbloqueo, si llama a **UnregisterEventNotification** desde dentro de la devolución de llamada, **UnregisterEventNotification** no espera a que se complete la devolución de llamada activa.

> [!IMPORTANT]
> Antes de destruir el objeto DXCore representado por el argumento *dxCoreObject* pasado a [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), debe usar el valor de cookie para anular el registro de ese objeto de las notificaciones mediante una llamada a **UnregisterEventNotification**. Si no lo hace, se produce una excepción grave cuando se detecta la situación.

Una vez que se anula el registro de un valor de cookie, ese valor se puede seleccionar para que lo devuelva un registro subsiguiente.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)