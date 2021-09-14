---
title: PSN_TRANSLATEACCELERATOR de notificación (Prsht.h)
description: Notifica a una hoja de propiedades que se ha recibido un mensaje de teclado. Proporciona a la página una oportunidad para realizar la traducción del acelerador de teclado privado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR código de notificación Windows controles
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167433"
---
# <a name="psn_translateaccelerator-notification-code"></a>Código de notificación \_ DE PSN TRANSLATEACCELERATOR

Notifica a una hoja de propiedades que se ha recibido un mensaje de teclado. Proporciona a la página una oportunidad para realizar la traducción del acelerador de teclado privado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **hdr**. El **miembro hwndFrom** de la **estructura NMHDR** contiene el identificador de la hoja de propiedades. El **miembro lParam** de la **estructura PSHNOTIFY** es un puntero al [**mensaje MSG del mensaje.**](/windows/win32/api/winuser/ns-winuser-msg) Se puede convertir a un tipo **LPMSG** para obtener acceso a los parámetros del mensaje que se va a traducir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve PSNRET \_ MESSAGEHANDLED para indicar que no es necesario ningún procesamiento adicional. Devuelve PSNRET \_ NOERROR para solicitar el procesamiento normal.

## <a name="remarks"></a>Observaciones

Para establecer el valor devuelto, el procedimiento del cuadro de diálogo de la página debe usar la [**función SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor MSGRESULT de \_ DWL. El procedimiento del cuadro de diálogo debe devolver **TRUE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

