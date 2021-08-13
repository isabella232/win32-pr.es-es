---
description: Define la función de devolución&8212; que implementa en la aplicación&8212; que se especificó para la \# \# función WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK de devolución de llamada (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: 7066f45b714c28b53747d0d0f1851bd94ac2ac902e5b4adba1d0746e8328b3b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619980"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>Función de devolución \_ de llamada WFD DISPLAY \_ SINK \_ NOTIFICATION \_ CALLBACK

La **función WFD \_ DISPLAY SINK \_ NOTIFICATION \_ \_ CALLBACK** define la función de devolución de llamada (que se implementa en la aplicación) que se especificó para la [**función WFDStartDisplaySink.**](wfdstartdisplaysink.md)

## <a name="syntax"></a>Sintaxis


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pvContext* \[ in, opcional\]
</dt> <dd>

Puntero de contexto opcional pasado a la función de devolución de llamada.

</dd> <dt>

*pNotification* \[ En\]
</dt> <dd>

Puntero a una estructura que contiene datos sobre la notificación del receptor de pantalla.

</dd> <dt>

*pNotificationResult* \[ in, out, optional\]
</dt> <dd>

Puntero a una estructura que contiene datos que la aplicación puede establecer opcionalmente para indicar el resultado del procesamiento de la notificación del receptor de pantalla.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




