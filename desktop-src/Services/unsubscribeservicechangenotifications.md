---
description: Cancela la suscripción a las notificaciones de cambio de estado del servicio.
ms.assetid: 8c04ebf7-4d61-4617-b120-dbe26b2f9ad2
title: Función UnsubscribeServiceChangeNotifications (Winsvcp.h)
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
ms.openlocfilehash: 3e37f2b786d32ab9f42738e6a8522c6f4593aa6b21a490a6fdd969233b4a6dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888174"
---
# <a name="unsubscribeservicechangenotifications-function"></a>Función UnsubscribeServiceChangeNotifications

Cancela la suscripción a las notificaciones de cambio de estado del servicio. Esta función usa las suscripciones devueltas [**por SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md).

## <a name="syntax"></a>Sintaxis


```C++
 VOID WINAPI UnsubscribeServiceChangeNotifications(
  _In_ PSC_NOTIFICATION_REGISTRATION pSubscription
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSubscription* \[ En\]
</dt> <dd>

Puntero a la suscripción a la que se va a cancelar la suscripción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

**UnsubscribeServiceChangeNotifications** no se devuelve hasta que se completan las devoluciones de llamada pendientes en proceso. Por lo tanto, no puede llamar **a UnsubscribeServiceChangeNotifications** dentro de la devolución de llamada sin provocar un interbloqueo.

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

[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

 




