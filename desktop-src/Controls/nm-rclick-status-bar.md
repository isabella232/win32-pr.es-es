---
title: NM_RCLICK de notificación (barra de estado) (Commctrl.h)
description: Notifica a la ventana primaria de un control de barra de estado que el usuario ha hecho clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- NM_RCLICK (barra de estado) código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8a42be8d41552173ef458d2f2c4e6232aa033aebfccd878142ac21b7f69f01b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799055"
---
# <a name="nm_rclick-status-bar-notification-code"></a>Código de notificación de NM \_ RCLICK (barra de estado)

Notifica a la ventana primaria de un control de barra de estado que el usuario ha hecho clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para indicar que el sistema controló el clic del mouse y suprime el procesamiento predeterminado. Devuelve **FALSE** para permitir el procesamiento predeterminado del clic.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





