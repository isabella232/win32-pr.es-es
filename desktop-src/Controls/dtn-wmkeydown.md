---
title: DTN_WMKEYDOWN de notificación (Commctrl.h)
description: Enviado por un control selector de fecha y hora (DTP) cuando el usuario tipos en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce2e7d0761308805746278d2f542f5e9458b56d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246932"
---
# <a name="dtn_wmkeydown-notification-code"></a>Código de notificación \_ WMKEYDOWN de DTN

Enviado por un control selector de fecha y hora (DTP) cuando el usuario tipos en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) que contiene información sobre esta instancia del código de notificación. La estructura incluye información sobre la clave que el usuario ha especificado, la subcadena que define el campo de devolución de llamada y la fecha y hora actuales del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El propietario del control debe devolver cero.

## <a name="remarks"></a>Observaciones

El control de este código de notificación permite al propietario del control proporcionar respuestas específicas a las pulsaciones de tecla dentro de los campos de devolución de llamada del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DTN \_ WMKEYDOWNW** (Unicode) y **DTN \_ WMKEYDOWNA** (ANSI)<br/>               |



 

 





