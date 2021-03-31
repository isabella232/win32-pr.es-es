---
title: Código de notificación de PSN_KILLACTIVE (Prsht. h)
description: Notifica a una página que está a punto de perder la activación porque se está activando otra página o porque el usuario ha haga clic en el botón Aceptar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996285"
---
# <a name="psn_killactive-notification-code"></a>Código de notificación de KILLACTIVE de PSN \_

Notifica a una página que está a punto de perder la activación porque se está activando otra página o porque el usuario ha haga clic en el botón Aceptar. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades. El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para evitar que la página pierda la activación o **false** para permitirlo.

## <a name="remarks"></a>Observaciones

Una aplicación controla este código de notificación para validar la información que el usuario ha escrito.

> [!Note]  
> La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación KILLACTIVE de PSN. No intente agregar, quitar o insertar páginas mientras controla este código de notificación. Si lo hace, tendrá resultados imprevisibles.

 

Para establecer un valor devuelto, el procedimiento de cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con un valor de DWL \_ MSGRESULT establecido en el valor devuelto. El procedimiento del cuadro de diálogo debe devolver **true**.

Si el procedimiento del cuadro de diálogo establece DWL \_ MSGRESULT en **true**, debería mostrar un cuadro de mensaje para explicar el problema al usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

