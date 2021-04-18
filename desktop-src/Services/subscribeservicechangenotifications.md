---
description: Se suscribe a las notificaciones de cambio de estado del servicio mediante una función de devolución de llamada.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Función SubscribeServiceChangeNotifications (Winsvcp. h)
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
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668186"
---
# <a name="subscribeservicechangenotifications-function"></a>SubscribeServiceChangeNotifications función)

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

*hService* \[ de\]
</dt> <dd>

Identificador del servicio o identificador del administrador de control de servicios (SCM) para supervisar los cambios.

Los identificadores de los servicios son devueltos por la función [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) y [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y deben tener el derecho de acceso de **Estado de \_ consulta \_ de servicio** . Los identificadores del administrador de control de servicios los devuelve la función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) y deben tener el derecho de enumerar de acceso de **\_ \_ \_ servicio SC Manager** .

</dd> <dt>

*eEventType* \[ de\]
</dt> <dd>

Especifica el tipo de cambios de estado que se deben informar. Este parámetro se establece en uno de los valores especificados en el [**\_ \_ tipo de evento SC**](sc-event-type.md). El comportamiento de esta función es diferente en función del tipo de evento que se indica a continuación.



| Value                                                                                                                                                                                                                                                   | Significado                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <dt>**SC \_ \_ \_ Cambio de base de datos de eventos**</dt> <dt>0</dt> </dl> | Se ha agregado o eliminado un servicio. El parámetro *hService* debe ser un identificador del SCM.<br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <dt>**SC \_ \_ \_ Cambio de propiedad de evento**</dt> <dt>1</dt> </dl> | Se han actualizado una o varias propiedades de servicio. El parámetro *hService* debe ser un identificador del servicio.<br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <dt>**SC \_ \_ \_ Cambio de estado de evento**</dt> <dt>2</dt> </dl>       | El estado de un servicio ha cambiado. El parámetro *hService* debe ser un identificador del servicio.<br/>              |



 

</dd> <dt>

*pCallback* \[ de\]
</dt> <dd>

Especifica la función de devolución de llamada. La devolución de llamada debe definirse como un tipo **de \_ devolución de \_ llamada de notificación SC**. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*pCallbackContext* \[ en, opcional\]
</dt> <dd>

Un puntero que representa el contexto para esta devolución de llamada de notificación.

</dd> <dt>

*pSubscription* \[ enuncia\]
</dt> <dd>

Devuelve un puntero a la suscripción resultante del registro de devolución de llamada de notificación. El autor de la llamada es responsable de llamar a [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) para dejar de recibir notificaciones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es **error \_ Success**.

Si se produce un error en la función, el valor devuelto es uno de los [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

## <a name="remarks"></a>Observaciones

La función de devolución de llamada se declara como sigue:


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



La función de devolución de llamada recibe un puntero al contexto proporcionado por el llamador. La devolución de llamada se invoca como resultado del evento de cambio de estado del servicio. Cuando se invoca la devolución de llamada, se proporciona con un valor de máscara de la **notificación de servicio \_ \_ * XXX*** que indica el tipo de cambio de estado del servicio. Cuando la devolución de llamada se proporciona con cero en lugar de un valor válido de **notificación de servicio \_ \_ * XXX***, la aplicación debe comprobar lo que se ha cambiado.

La función de devolución de llamada no debe bloquear la ejecución. Si espera que la ejecución de la función de devolución de llamada tarde tiempo, descargue el trabajo que realiza en la función de devolución de llamada en un subproceso independiente mediante la puesta en cola de un elemento de trabajo en un subproceso de un grupo de subprocesos. Algunos tipos de trabajo que pueden hacer que la función de devolución de llamada tarden tiempo incluyen realizar e/s de archivos, esperar en un evento y realizar llamadas a procedimientos remotos externos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

