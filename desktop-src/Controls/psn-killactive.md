---
title: PSN_KILLACTIVE de notificación (Prsht.h)
description: Notifica a una página que está a punto de perder la activación porque se está activando otra página o porque el usuario ha hecho clic en el botón Aceptar. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE código de notificación Windows controles
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167450"
---
# <a name="psn_killactive-notification-code"></a>Código de notificación KILLACTIVE de PSN \_

Notifica a una página que está a punto de perder la activación porque se está activando otra página o porque el usuario ha hecho clic en el botón Aceptar. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **hdr**. El **miembro hwndFrom** de esta **estructura NMHDR** contiene el identificador de la hoja de propiedades. El **miembro lParam** de la **estructura PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para evitar que la página pierda la activación o **FALSE** para permitirla.

## <a name="remarks"></a>Observaciones

Una aplicación controla este código de notificación para validar la información que el usuario ha especificado.

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando se envía el código de notificación \_ KILLACTIVE de PSN. No intente agregar, quitar ni insertar páginas mientras administra este código de notificación. Si lo hace, tendrá resultados impredecibles.

 

Para establecer un valor devuelto, el procedimiento del cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un valor MSGRESULT de DWL establecido \_ en el valor devuelto. El procedimiento del cuadro de diálogo debe devolver **TRUE**.

Si el procedimiento del cuadro de diálogo establece DWL MSGRESULT en TRUE, debe mostrar un cuadro de mensaje para \_ explicar el problema al usuario. 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

