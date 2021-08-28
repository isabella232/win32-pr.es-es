---
title: DTN_USERSTRING de notificación (Commctrl.h)
description: Enviado por un control selector de fecha y hora (DTP) cuando un usuario termina de editar una cadena en el control .
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING código de notificación Windows controles
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6eabae4ed5a4fbe9ff0652b77fb7b6fbaf709b9030e3aa982af486ad6b7ed0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062925"
---
# <a name="dtn_userstring-notification-code"></a>Código de notificación USERSTRING de DTN \_

Enviado por un control selector de fecha y hora (DTP) cuando un usuario termina de editar una cadena en el control . Este código de notificación solo se envía mediante controles DTP que están establecidos en el estilo [**\_ APPCANPARSE de DTS.**](date-and-time-picker-control-styles.md) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) que contiene información sobre la instancia del código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El propietario del control debe devolver cero.

## <a name="remarks"></a>Comentarios

El control de este código de notificación permite al propietario proporcionar respuestas personalizadas a las cadenas especificadas en el control por el usuario. El propietario debe estar preparado para analizar la cadena de entrada y tomar medidas si es necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DTN \_ USERSTRINGW** (Unicode) y **DTN \_ USERSTRINGA** (ANSI)<br/>             |



 

 





