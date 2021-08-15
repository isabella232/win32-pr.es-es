---
description: Se suscribe a las notificaciones de cambio de estado del servicio mediante una función de devolución de llamada.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Función SubscribeServiceChangeNotifications (Winsvcp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: 83bd7bc3f937794f14cbe1d2877bc53ce7d347a8f45fd4f0ddb3e9d0ee9a52a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888461"
---
# <a name="subscribeservicechangenotifications-function"></a>Función SubscribeServiceChangeNotifications

Se suscribe a las notificaciones de cambio de estado del servicio mediante una función de devolución de llamada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hService* \[ En\]
</dt> <dd>

Un identificador para el servicio o un identificador para el administrador de control de servicios (SCM) para supervisar los cambios.

Las funciones [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) y [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) devuelven identificadores a los servicios y deben tener el derecho de acceso **SERVICE QUERY \_ \_ STATUS.** La función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) devuelve los identificadores al administrador de control de servicios y deben tener el derecho de acceso **\_ \_ ENUMERATE \_ SERVICE de SC MANAGER.**

</dd> <dt>

*eEventType* \[ En\]
</dt> <dd>

Especifica el tipo de cambios de estado que se deben notifica. Este parámetro se establece en uno de los valores especificados en [**SC \_ EVENT \_ TYPE**](sc-event-type.md). El comportamiento de esta función es diferente en función del tipo de evento como se muestra a continuación.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <dt>**SC \_ CAMBIO DE \_ LA BASE DE DATOS DE \_ EVENTOS**</dt> <dt>0</dt> </dl> | Se ha agregado o eliminado un servicio. El *parámetro hService* debe ser un identificador del SCM.<br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <dt>**SC \_ CAMBIO \_ DE PROPIEDAD DE \_ EVENTO**</dt> <dt>1</dt> </dl> | Se han actualizado una o varias propiedades de servicio. El *parámetro hService* debe ser un identificador del servicio.<br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <dt>**SC \_ CAMBIO \_ DE ESTADO DEL \_ EVENTO**</dt> <dt>2</dt> </dl>       | El estado de un servicio ha cambiado. El *parámetro hService* debe ser un identificador del servicio.<br/>              |



 

</dd> <dt>

*pCallback* \[ En\]
</dt> <dd>

Especifica la función de devolución de llamada. La devolución de llamada debe definirse como que tiene un tipo de DEVOLUCIÓN DE LLAMADA **DE NOTIFICACIÓN DE SC \_ \_**. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*pCallbackContext* \[ in, opcional\]
</dt> <dd>

Puntero que representa el contexto de esta devolución de llamada de notificación.

</dd> <dt>

*pSubscription* \[ out\]
</dt> <dd>

Devuelve un puntero a la suscripción resultante del registro de devolución de llamada de notificación. El autor de la llamada es responsable de [**llamar a UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) para dejar de recibir notificaciones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **ERROR \_ SUCCESS**.

Si se produce un error en la función, el valor devuelto es uno de los códigos [de error del sistema](/windows/desktop/Debug/system-error-codes).

## <a name="remarks"></a>Comentarios

La función de devolución de llamada se declara de la siguiente manera:


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



La función de devolución de llamada recibe un puntero al contexto proporcionado por el autor de la llamada. La devolución de llamada se invoca como resultado del evento de cambio de estado del servicio. Cuando se invoca la devolución de llamada, se proporciona con una máscara de bits de **valores SERVICE \_ NOTIFY \_ *XXX*** que indican el tipo de cambio de estado del servicio. Cuando la devolución de llamada se proporciona con cero en lugar de un valor **SERVICE \_ NOTIFY \_ *XXX*** válido, la aplicación debe comprobar lo que se ha cambiado.

La función de devolución de llamada no debe bloquear la ejecución. Si espera que la ejecución de la función de devolución de llamada lleve tiempo, descargue el trabajo que realiza en la función de devolución de llamada en un subproceso independiente mediante la cola de un elemento de trabajo en un subproceso de un grupo de subprocesos. Algunos tipos de trabajo que pueden hacer que la función de devolución de llamada lleve tiempo incluyen la realización de E/S de archivos, la espera de un evento y la realización de llamadas a procedimientos remotos externos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Winsvcp.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

