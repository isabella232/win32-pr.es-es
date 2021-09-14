---
title: TDN_VERIFICATION_CLICKED de notificación (Commctrl.h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en la casilla de verificación del cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- TDN_VERIFICATION_CLICKED código de notificación Windows controles
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7887a4d696f5294ebffc6fc6cc7183ff2c0aed8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166058"
---
# <a name="tdn_verification_clicked-notification-code"></a>Código de notificación \_ CLICKED VERIFICATION DE TDN \_

Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en la casilla de verificación del cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **BOOL que** especifica el estado de la casilla de verificación. Es **TRUE si** la casilla de verificación está activada o **FALSE** si está desactivada.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

