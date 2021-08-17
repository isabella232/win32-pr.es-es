---
title: HDN_TRACK de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario está arrastrando un divisor en el control de encabezado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb32a553c85c8fb1bc8321dae5e85b3e7832cf90e4a6652ad163511ad4420d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435225"
---
# <a name="hdn_track-notification-code"></a>Código de notificación DE HDN \_ TRACK

Notifica a la ventana primaria de un control de encabezado que el usuario está arrastrando un divisor en el control de encabezado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento cuyo divisor se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **FALSE** para continuar el seguimiento del divisor o **TRUE** al seguimiento final.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ TRACKW** (Unicode) y **HDN \_ TRACKA** (ANSI)<br/>                       |



 

 





