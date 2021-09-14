---
title: IDXCoreAdapterFactory::RegisterEventNotification
description: Se registra para recibir notificaciones de condiciones específicas de una lista de adaptadores o adaptadores de DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3643fbb01fc955049c297a577f18d4d276e73f46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966343"
---
# <a name="idxcoreadapterfactoryregistereventnotification-method"></a>IDXCoreAdapterFactory::RegisterEventNotification (método)

Se registra para recibir notificaciones de condiciones específicas de una lista de adaptadores o adaptadores de DXCore. Para obtener instrucciones de programación y ejemplos de código, [vea Uso de DXCore para enumerar adaptadores.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintaxis

```cpp
virtual HRESULT STDMETHODCALLTYPE RegisterEventNotification(
  _In_ IUnknown *dxCoreObject,
  DXCoreNotificationType notificationType,
  _In_ PFN_DXCORE_NOTIFICATION_CALLBACK callbackFunction,
  _In_opt_ void *callbackContext,
  _Out_ uint32_t *eventCookie) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="dxcoreobject-in"></a>dxCoreObject [in]

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

El objeto DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)) a cuyas notificaciones se está suscribiendo.

### <a name="notificationtype"></a>notificationType

Tipo: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Tipo de notificación para la que se va a registrar. Consulte la tabla de [DXCoreNotificationType para](./ne-dxcore_interface-dxcorenotificationtype.md) obtener información sobre qué tipos son válidos con qué tipos de objetos.

### <a name="callbackfunction-in"></a>callbackFunction [in]

Tipo: **[PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)**

Puntero a una función de devolución de llamada (implementada por la aplicación), a la que llama el objeto DXCore para eventos de notificación. Para obtener la firma de la función, [vea PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md).

### <a name="callbackcontext-in"></a>callbackContext [in]

Tipo: **\* void**

Puntero opcional a un objeto que contiene información de contexto. Este objeto se pasa a la función de devolución de llamada cuando se genera la notificación.

### <a name="eventcookie-out"></a>eventCookie [out]

Tipo: **uint32_t \***

Puntero a un valor **uint32_t.** Si se realiza correctamente, la función desreferencia el puntero y establece el valor en un valor de cookie distinto de cero que representa este registro. Use este valor de cookie para anular el registro de la notificación mediante una llamada [a IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Vea **Comentarios**.

Si no se realiza correctamente, la función desreferencia el puntero y establece el valor en cero, que representa un valor de cookie no válido.

## <a name="returns"></a>Devoluciones

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](../../com/structure-of-com-error-codes.md) error [HRESULT](../../com/com-error-codes-10.md).

|Valor devuelto|Descripción|
|-|-|
|DXGI_ERROR_INVALID_CALL|*notificationType* no es compatible con el sistema operativo (SO).|
|E_INVALIDARG|`nullptr` se proporcionó para *dxCoreObject* o si se proporcionó una combinación *de notificationType* y *dxCoreObject* no válida.|
|E_POINTER|`nullptr` se proporcionó para *callbackFunction o* *eventCookie*.|

## <a name="remarks"></a>Observaciones

Use **RegisterEventNotification para registrar** los eventos generados por las interfaces [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) e [IDXCoreAdapter.](./nn-dxcore_interface-idxcoreadapter.md) Se admiten estos tipos de notificación.

|[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)|*DxCoreObject compatible*|Notas|
|-|-|-|
|AdapterListStale|**IDXCoreAdapterList**|Indica que la lista de adaptadores que cumplen los criterios de filtro ha cambiado. Si la lista de adaptadores está obsoleta en el momento del registro, se llama inmediatamente a la devolución de llamada. Esta devolución de llamada se produce como máximo una vez por registro.|
|AdapterNoLongerValid|**IDXCoreAdapter**|Indica que el adaptador ya no es válido. Si el adaptador no es válido en el momento del registro, se llama inmediatamente a la devolución de llamada.|
|AdapterBudgetChange|**IDXCoreAdapter**|Indica que se ha producido un evento de presupuesto de memoria y que debe llamar a [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (con [DXCoreAdapterState::AdapterMemoryBudget)](./ne-dxcore_interface-dxcoreadapterstate.md)para evaluar el estado del presupuesto de memoria actual. Tras el registro, siempre se producirá una devolución de llamada inicial para permitirle consultar el estado inicial.|
|AdapterHardwareContentProtectionTeardown|**IDXCoreAdapter**|Indica que debe volver a evaluar el estado actual de la sesión de criptografía; Por ejemplo, mediante una llamada a [ID3D11VideoContext1::CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) para determinar el impacto de la cancelación de hardware para una interfaz [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) específica. Tras el registro, siempre se producirá una devolución de llamada inicial para permitirle consultar el estado inicial.|

DXCore realiza de forma asincrónica una llamada a la función que se proporciona en *callbackFunction* en un subproceso en segundo plano cuando se produce el evento detectado. No se garantiza el orden o el tiempo de las devoluciones de llamada que pueden producirse varias devoluciones de llamada en cualquier orden, o &mdash; incluso simultáneamente. Incluso es posible que la devolución de llamada se invoque antes **de que se complete RegisterEventNotification.** En ese caso, DXCore garantiza que *eventCookie* se establece antes de llamar a la devolución de llamada. Se serializarán varias devoluciones de llamada para un registro específico en orden.

Las devoluciones de llamada pueden producirse en cualquier momento hasta que llame a [UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)y se complete. Las devoluciones de llamada se producen en sus propios subprocesos y puede realizar llamadas a la API DXCore en esos subprocesos, incluido **UnregisterEventNotification**. Sin embargo, no debe liberar la última referencia a *dxCoreObject* en este subproceso.

> [!IMPORTANT]
> Antes de destruir el objeto DXCore representado por el argumento *dxCoreObject* pasado a **RegisterEventNotification**, debe usar el valor de cookie para anular el registro de ese objeto de las notificaciones mediante una llamada a [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Si no lo hace, se produce una excepción grave cuando se detecta la situación.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [IDXCoreAdapterList,](./nn-dxcore_interface-idxcoreadapterlist.md) [IDXCoreAdapterFactory::UnregisterEventNotification,](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md) [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)