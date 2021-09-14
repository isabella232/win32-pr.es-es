---
title: TTN_NEEDTEXT de notificación (Commctrl.h)
description: Enviado por un control de información sobre herramientas para recuperar la información necesaria para mostrar una ventana de información sobre herramientas. Este código de notificación es idéntico a TTN \_ GETDISPINFO. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT código de notificación Windows controles
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165805"
---
# <a name="ttn_needtext-notification-code"></a>Código de notificación NEEDTEXT de TTN \_

Enviado por un control de información sobre herramientas para recuperar la información necesaria para mostrar una ventana de información sobre herramientas. Este código de notificación es idéntico a [TTN \_ GETDISPINFO.](ttn-getdispinfo.md) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) que identifica la herramienta que necesita texto y recibe la información solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="remarks"></a>Observaciones

Rellene los miembros adecuados de la estructura para devolver la información solicitada al control de información sobre herramientas. Si el controlador de mensajes establece el miembro **uFlags** de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) en TTF DI SETITEM, el control de información sobre herramientas almacena la información y no la \_ \_ volverá a solicitar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTN \_ NEEDTEXTW** (Unicode) y **TTN \_ NEEDTEXTA** (ANSI)<br/>                 |



 

 





