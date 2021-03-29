---
title: Código de notificación de HDN_TRACK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario está arrastrando un divisor en el control de encabezado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK controles de código de notificación de Windows
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
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905403"
---
# <a name="hdn_track-notification-code"></a>Código de notificación de seguimiento de HDN \_

Notifica a la ventana primaria de un control de encabezado que el usuario está arrastrando un divisor en el control de encabezado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


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

Devuelve **false** para seguir realizando el seguimiento del divisor o en **true** para finalizar el seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ TRACKW** (Unicode) y **HDN \_ TRACKA** (ANSI)<br/>                       |



 

 





