---
description: Define la función de devolución \# de llamada&8212; que se implementa en la aplicación&\# 8212; que se especificó para la función WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK función de devolución de llamada (Wfdsink. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667131"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>Función de devolución de llamada de devolución de llamada de \_ \_ notificación del receptor \_ \_ de WFD

La función de **devolución de llamada de notificación del receptor de visualización de WFD \_ \_ \_ \_** define la función de devolución de llamada, que se implementa en la aplicación, que se especificó para la función [**WFDStartDisplaySink**](wfdstartdisplaysink.md) .

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

*pvContext* \[ en, opcional\]
</dt> <dd>

Un puntero de contexto opcional que se pasa a la función de devolución de llamada.

</dd> <dt>

*pNotification* \[ de\]
</dt> <dd>

Puntero a una estructura que contiene datos sobre la notificación de presentación del receptor.

</dd> <dt>

*pNotificationResult* \[ in, out, opcional\]
</dt> <dd>

Un puntero a un struct que contiene los datos que la aplicación puede establecer opcionalmente para indicar el resultado de procesar la notificación de presentación del receptor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




