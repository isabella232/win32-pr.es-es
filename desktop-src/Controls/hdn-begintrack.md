---
title: Código de notificación de HDN_BEGINTRACK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario ha empezado a arrastrar un divisor en el control (es decir, el usuario ha presionado el botón primario del mouse mientras el cursor se encuentra en un divisor del control de encabezado).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151287"
---
# <a name="hdn_begintrack-notification-code"></a>Código de notificación de BEGINTRACK de HDN \_

Notifica a la ventana primaria de un control de encabezado que el usuario ha empezado a arrastrar un divisor en el control (es decir, el usuario ha presionado el botón primario del mouse mientras el cursor se encuentra en un divisor del control de encabezado). Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento cuyo divisor se va a arrastrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **false** para permitir el seguimiento del divisor o **true** para evitar el seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ BEGINTRACKW** (Unicode) y **HDN \_ BEGINTRACKA** (ANSI)<br/>             |



 

 





