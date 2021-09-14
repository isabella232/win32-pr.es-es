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
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069425"
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
| Encabezado<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl> |



 

 




