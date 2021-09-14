---
title: PSN_QUERYCANCEL de notificación (Prsht.h)
description: Indica que el usuario ha cancelado la hoja de propiedades. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL código de notificación Windows controles
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167442"
---
# <a name="psn_querycancel-notification-code"></a>PSN QUERYCANCEL notification code (Código de notificación DE PSN \_ QUERYCANCEL)

Indica que el usuario ha cancelado la hoja de propiedades. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **hdr**. El **miembro hwndFrom** de esta **estructura NMHDR** contiene el identificador de la hoja de propiedades. El **miembro lParam** de la **estructura PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para evitar la operación de cancelación o **FALSE** para permitirla.

## <a name="remarks"></a>Observaciones

Este código de notificación se envía normalmente cuando un usuario hace clic en **el botón** Cancelar. También se envía cuando un usuario hace clic en el botón **X** de la esquina superior derecha de la hoja de propiedades o presiona la tecla ESCAPE. Una página de hoja de propiedades puede controlar este código de notificación para pedir al usuario que compruebe la operación de cancelación.

Para establecer un valor devuelto, el procedimiento del cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT establecido en el valor devuelto. El procedimiento del cuadro de diálogo debe devolver **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

