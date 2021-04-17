---
title: Código de notificación de PSN_TRANSLATEACCELERATOR (Prsht. h)
description: Notifica a una hoja de propiedades que se ha recibido un mensaje de teclado. Proporciona a la página una oportunidad para realizar la traducción del acelerador del teclado privado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656469"
---
# <a name="psn_translateaccelerator-notification-code"></a>\_Código de notificación PSN TRANSLATEACCELERATOR

Notifica a una hoja de propiedades que se ha recibido un mensaje de teclado. Proporciona a la página una oportunidad para realizar la traducción del acelerador del teclado privado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación. Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de la estructura **NMHDR** contiene el identificador de la hoja de propiedades. El miembro **lParam** de la estructura **PSHNOTIFY** es un puntero [**al mensaje del mensaje.**](/windows/win32/api/winuser/ns-winuser-msg) Se puede convertir en un tipo **LPMSG** para obtener acceso a los parámetros del mensaje que se va a traducir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve PSNRET \_ MESSAGEHANDLED para indicar que no es necesario ningún procesamiento adicional. Devuelve PSNRET \_ NoError para solicitar el procesamiento normal.

## <a name="remarks"></a>Observaciones

Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT. El procedimiento del cuadro de diálogo debe devolver **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

