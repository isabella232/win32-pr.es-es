---
title: Código de notificación de PSN_WIZFINISH (Prsht. h)
description: Notifica a una página que el usuario ha pulsado el botón Finalizar en un asistente. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491783"
---
# <a name="psn_wizfinish-notification-code"></a>Código de notificación de WIZFINISH de PSN \_

Notifica a una página que el usuario ha pulsado el botón **Finalizar** en un asistente. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades. El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

-   Devuelve **true** para evitar que finalice el asistente.
-   [Versión 5,80.](common-control-versions.md) y versiones posteriores. Devuelve un identificador de ventana para evitar que finalice el asistente. El asistente establecerá el foco en esa ventana. La ventana debe pertenecer a la página del asistente.
-   Devuelve **false** para permitir que el asistente finalice.

## <a name="remarks"></a>Observaciones

Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT y el procedimiento de cuadro de diálogo debe devolver **true**.

[Versión 5,80.](common-control-versions.md) Si la aplicación devuelve **true** para impedir que un asistente finalice, no tiene ningún control sobre qué ventana de la página recibe el foco. Las aplicaciones que necesitan detener el final del asistente normalmente deberían hacerlo devolviendo el identificador de la ventana en la página del asistente que va a recibir el foco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

