---
title: Código de notificación de PGN_SCROLL (commctrl. h)
description: Notifica a la ventana primaria de un control de paginación que la ventana contenida está a punto de desplazarse. Esta notificación se envía en forma de mensaje de notificación de WM \_ .
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150189"
---
# <a name="pgn_scroll-notification-code"></a>Código de notificación de desplazamiento de PGN \_

Notifica a la ventana primaria de un control de paginación que la ventana contenida está a punto de desplazarse. Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) que contiene y recibe información sobre el código de notificación. El miembro **iDir** de esta estructura indica la dirección del desplazamiento. Los miembros **iXpos** y **iYpos** contienen la posición horizontal y vertical de la ventana contenida antes del desplazamiento. El miembro **iScroll** contiene la diferencia de desplazamiento predeterminada. Si lo desea, puede modificar este miembro a una cantidad de desplazamiento diferente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





