---
description: Define el tipo de notificación que se pasa a la \_ función de devolución de llamada de notificación de receptor de visualización de WFD \_ \_ \_ .
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: Enumeración WFD_DISPLAY_SINK_NOTIFICATION_TYPE (Wfdsink. h)
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
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667129"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a>\_ \_ \_ Enumeración de tipo de notificación de receptor de visualización de WFD \_

El tipo enumerado tipo de notificación de receptor de visualización de WFD define el tipo de notificación que se pasa a la función de devolución de llamada de [**notificación del receptor de visualización de WFD \_ \_ \_ \_**](wfd-display-sink-notification-callback.md) . **\_ \_ \_ \_**

## <a name="syntax"></a>Sintaxis


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



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




