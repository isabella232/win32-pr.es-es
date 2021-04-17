---
title: Código de notificación de TVN_ITEMCHANGING (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento están a punto de cambiar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534210"
---
# <a name="tvn_itemchanging-notification-code"></a>Código de notificación de ITEMCHANGING de TVN \_

Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento están a punto de cambiar. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que describe el elemento que está cambiando. El miembro **uChanged** se establece en el \_ Estado TVIF.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **false** para aceptar el cambio o **true** para evitar el cambio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ ITEMCHANGINGW** (Unicode) y **TVN \_ ITEMCHANGINGA** (ANSI)<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TVN \_ ITEMCHANGED](tvn-itemchanged.md)
</dt> </dl>

 

 





