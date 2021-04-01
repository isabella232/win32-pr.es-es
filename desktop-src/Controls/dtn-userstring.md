---
title: Código de notificación de DTN_USERSTRING (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cuando un usuario termina de editar una cadena en el control.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING controles de código de notificación de Windows
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
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905062"
---
# <a name="dtn_userstring-notification-code"></a>DTN \_ código de notificación de USERSTRING

Se envía mediante un control de selector de fecha y hora (DTP) cuando un usuario termina de editar una cadena en el control. Este código de notificación solo lo envían los controles de DTP que se establecen en el estilo [**\_ APPCANPARSE de DTS**](date-and-time-picker-control-styles.md) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) que contiene información sobre la instancia del código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El propietario del control debe devolver cero.

## <a name="remarks"></a>Observaciones

El control de este código de notificación permite que el propietario proporcione respuestas personalizadas a las cadenas especificadas por el usuario en el control. El propietario debe estar preparado para analizar la cadena de entrada y tomar medidas si es necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DTN \_ USERSTRINGW** (Unicode) y **DTN \_ USERSTRINGA** (ANSI)<br/>             |



 

 





