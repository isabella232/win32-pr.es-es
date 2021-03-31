---
title: Código de notificación de DTN_WMKEYDOWN (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario escribe en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149984"
---
# <a name="dtn_wmkeydown-notification-code"></a>Código de notificación de WMKEYDOWN de DTN \_

Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario escribe en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) que contiene información sobre esta instancia del código de notificación. La estructura incluye información sobre la clave que el usuario ha escrito, la subcadena que define el campo de devolución de llamada y la fecha y hora actuales del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El propietario del control debe devolver cero.

## <a name="remarks"></a>Observaciones

El control de este código de notificación permite que el propietario del control proporcione respuestas específicas a las pulsaciones de teclas dentro de los campos de devolución de llamada del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DTN \_ WMKEYDOWNW** (Unicode) y **DTN \_ WMKEYDOWNA** (ANSI)<br/>               |



 

 





