---
title: TBN_QUERYINSERT de notificación (Commctrl.h)
description: Notifica a la ventana primaria de la barra de herramientas si se puede insertar un botón a la izquierda del botón especificado mientras el usuario personaliza una barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT de notificación Windows controles
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
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166325"
---
# <a name="tbn_queryinsert-notification-code"></a>Código de notificación \_ QUERYINSERT de TBN

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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





