---
description: Define el tipo de notificación que se pasa a la función WFD \_ DISPLAY \_ SINK NOTIFICATION \_ \_ CALLBACK.
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: WFD_DISPLAY_SINK_NOTIFICATION_TYPE enumeración (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: ca16197da0137e40c25a75c139773b02674b6bf7c90bcae2b94ae0845d201e71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800615"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a>Enumeración \_ WFD DISPLAY \_ SINK NOTIFICATION \_ \_ TYPE

El **tipo enumerado \_ WFD DISPLAY SINK NOTIFICATION \_ \_ \_ TYPE** define el tipo de notificación que se pasa a la función [**WFD DISPLAY SINK NOTIFICATION \_ \_ \_ \_ CALLBACK.**](wfd-display-sink-notification-callback.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**
</dt> <dd>

La notificación es una solicitud de aprovisionamiento.

</dd> <dt>

<span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**
</dt> <dd>

La notificación es una solicitud de reconexión.

</dd> <dt>

<span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**
</dt> <dd>

La notificación es una notificación conectada.

</dd> <dt>

<span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**
</dt> <dd>

La notificación es una notificación desconectada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




