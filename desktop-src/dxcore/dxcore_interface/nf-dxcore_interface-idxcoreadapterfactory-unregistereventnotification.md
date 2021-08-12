---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Anula el registro de una notificación para la que se registró anteriormente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 64fb54226f1fad0d1d36f8f4260c9c9172b105dc6239ea5cb805c32b57a938ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278886"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>IDXCoreAdapterFactory::UnregisterEventNotification (método)

Anula el registro de una notificación para la que se registró anteriormente. Para obtener instrucciones de programación y ejemplos de código, vea [Uso de DXCore para enumerar adaptadores.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="eventcookie"></a>eventCookie

Tipo: **uint32_t**

Valor de cookie (devuelto al llamar a [IDXCoreAdapterFactory::RegisterEventNotification)](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)que representa un registro anterior para el que ahora desea anular el registro.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|E_INVALIDARG|El valor de *eventCookie* no es una cookie válida que representa un registro anterior.|

## <a name="remarks"></a>Comentarios

**UnregisterEventNotification** devuelve solo después de que se hayan completado todas las devoluciones de llamada pendientes o en curso para este registro. DXCore garantiza que no se producirá ninguna devolución de llamada nueva para este registro después de que se haya devuelto **UnregisterEventNotification.** Sin embargo, para evitar un interbloqueo, si llama a **UnregisterEventNotification** desde dentro de la devolución de llamada, **UnregisterEventNotification** no espera a que se complete la devolución de llamada activa.

> [!IMPORTANT]
> Antes de destruir el objeto DXCore representado por el argumento *dxCoreObject* pasado a [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), debe usar el valor de cookie para anular el registro de ese objeto de las notificaciones llamando a **UnregisterEventNotification**. Si no lo hace, se produce una excepción grave cuando se detecta la situación.

Una vez anulado el registro de un valor de cookie, ese valor es apto para que lo devuelva un registro posterior.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)