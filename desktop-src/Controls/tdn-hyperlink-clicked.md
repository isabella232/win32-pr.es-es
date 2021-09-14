---
title: TDN_HYPERLINK_CLICKED de notificación (Commctrl.h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en un hipervínculo en el contenido del cuadro de diálogo de la tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- TDN_HYPERLINK_CLICKED código de notificación Windows controles
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd79406eb59f9bafd93269f8982db6213ef882c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166074"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a>Código de notificación \_ CLICKED DE HIPERVÍNCULO DE TDN \_

Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en un hipervínculo en el contenido del cuadro de diálogo de la tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


```C++
TDN_HYPERLINK_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena de caracteres anchos que contiene la dirección URL del hipervínculo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





