---
description: Cancela las suscripciones de las notificaciones de cambio de estado del servicio.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Función UnsubscribeServiceChangeNotifications (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnsubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: ebecfb133172c9c7a56ed6d28f7ad6b395d8afce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911245"
---
# <a name="unsubscribeservicechangenotifications-function"></a>UnsubscribeServiceChangeNotifications función)

Cancela las suscripciones de las notificaciones de cambio de estado del servicio. Esta función usa las suscripciones devueltas por [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).

## <a name="syntax"></a>Sintaxis


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSubscription* \[ de\]
</dt> <dd>

Un puntero a la suscripción a la que se va a cancelar la suscripción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

**UnsubscribeServiceChangeNotifications** no devuelve hasta que se completen las devoluciones de llamada en curso pendientes. Por lo tanto, no se puede llamar a **UnsubscribeServiceChangeNotifications** dentro de la devolución de llamada sin que se produzca un interbloqueo.

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

[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




