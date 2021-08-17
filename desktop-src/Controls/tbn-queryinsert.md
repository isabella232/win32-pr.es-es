---
title: TBN_QUERYINSERT de notificación (Commctrl.h)
description: Notifica a la ventana primaria de la barra de herramientas si se puede insertar un botón a la izquierda del botón especificado mientras el usuario personaliza una barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f741fd7cfa5c6f72405b10ba9678aed71f7cb2359743593f117b17c8ad1c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166965"
---
# <a name="tbn_queryinsert-notification-code"></a>Código de \_ notificación QUERYINSERT de TBN

Notifica a la ventana primaria de la barra de herramientas si se puede insertar un botón a la izquierda del botón especificado mientras el usuario personaliza una barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) El miembro **iItem** contiene el índice basado en cero del botón que se va a insertar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para permitir que se inserte un botón delante del botón dado o **FALSE** para evitar que se inserte el botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





