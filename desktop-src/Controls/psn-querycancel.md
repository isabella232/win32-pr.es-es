---
title: Código de notificación de PSN_QUERYCANCEL (Prsht. h)
description: Indica que el usuario ha cancelado la hoja de propiedades. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996283"
---
# <a name="psn_querycancel-notification-code"></a>Código de notificación de QUERYCANCEL de PSN \_

Indica que el usuario ha cancelado la hoja de propiedades. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades. El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para evitar la operación de cancelación o **false** para permitirlo.

## <a name="remarks"></a>Observaciones

Normalmente, este código de notificación se envía cuando un usuario hace clic en el botón **Cancelar** . También se envía cuando un usuario hace clic en el botón **X** de la esquina superior derecha de la hoja de propiedades o presiona la tecla escape. Una página de hoja de propiedades puede controlar este código de notificación para pedir al usuario que Compruebe la operación de cancelación.

Para establecer un valor devuelto, el procedimiento de cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT establecido en el valor devuelto. El procedimiento del cuadro de diálogo debe devolver **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

