---
title: TTN_NEEDTEXT de notificación (Commctrl.h)
description: Enviado por un control de información sobre herramientas para recuperar la información necesaria para mostrar una ventana de información sobre herramientas. Este código de notificación es idéntico al TTN \_ GETDISPINFO. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
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
ms.openlocfilehash: 7dae1ac1eb721d918acf38745f19c7e6dee4a6a296c7fa8003f516717ece6cf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967805"
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

## <a name="remarks"></a>Comentarios

Rellene los miembros adecuados de la estructura para devolver la información solicitada al control de información sobre herramientas. Si el controlador de mensajes establece el miembro **uFlags** de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) en TTF DI SETITEM, el control de información sobre herramientas almacena la información y no la volverá \_ \_ a solicitar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTN \_ NEEDTEXTW** (Unicode) y **TTN \_ NEEDTEXTA** (ANSI)<br/>                 |



 

 





