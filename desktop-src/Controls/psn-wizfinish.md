---
title: PSN_WIZFINISH de notificación (Prsht.h)
description: Notifica a una página que el usuario ha hecho clic en el botón Finalizar de un asistente. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH código de notificación Windows controles
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167422"
---
# <a name="psn_wizfinish-notification-code"></a>Código de notificación \_ WIZFINISH de PSN

Notifica a una página que el usuario ha hecho clic en **el botón** Finalizar de un asistente. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **hdr**. El **miembro hwndFrom** de esta **estructura NMHDR** contiene el identificador de la hoja de propiedades. El **miembro lParam** de la **estructura PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

-   Devuelve **TRUE para** evitar que el asistente termine.
-   [Versión 5.80.](common-control-versions.md) y versiones posteriores. Devuelve un identificador de ventana para evitar que el asistente termine. El asistente establecerá el foco en esa ventana. La ventana debe ser propiedad de la página del asistente.
-   Devuelve **FALSE** para permitir que finalice el asistente.

## <a name="remarks"></a>Observaciones

Para establecer el valor devuelto, el procedimiento del cuadro de diálogo de la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor MSGRESULT de DWL y el procedimiento del cuadro de diálogo debe \_ devolver **TRUE**.

[Versión 5.80.](common-control-versions.md) Si la aplicación devuelve **TRUE para** evitar que un asistente termine, no tiene control sobre qué ventana de la página recibe el foco. Las aplicaciones que necesitan detener la finalización de un asistente normalmente deben hacerlo devolviendo el identificador de la ventana en la página del asistente que va a recibir el foco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

