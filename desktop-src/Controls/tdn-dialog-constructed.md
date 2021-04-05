---
title: Código de notificación de TDN_DIALOG_CONSTRUCTED (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea después de crear el cuadro de diálogo y antes de que se muestre. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: e8556039-a74d-4e33-931d-a63ad5b2d4b0
keywords:
- TDN_DIALOG_CONSTRUCTED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_DIALOG_CONSTRUCTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d3360a8cee3542037ea927363de8cab69977e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997105"
---
# <a name="tdn_dialog_constructed-notification-code"></a>TDN \_ cuadro de diálogo \_ construido código de notificación

Enviado por un cuadro de diálogo de tarea después de crear el cuadro de diálogo y antes de que se muestre. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_DIALOG_CONSTRUCTED
     
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

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





